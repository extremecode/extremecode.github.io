# Testing Asynchronous Code
## Test setup
* async service to test
```markdown
export class AuthService {
isAuthenticated(): Promise<boolean> {
return Promise.resolve(!!localStorage.getItem('token'));
}
}
```
* component to test
```markdown
export class LoginComponent implements OnInit {
needsLogin: boolean = true;
constructor(private auth: AuthService) {
}
ngOnInit() {
this.auth.isAuthenticated().then((authenticated) => {
this.needsLogin = !authenticated;
})
}
}
```
## test change detection
```markdown
it('Button label via jasmine.done', () => {
fixture.detectChanges(); ①
expect(el.nativeElement.textContent.trim()).toBe('Login'); ②
spyOn(authService, 'isAuthenticated').and.returnValue(Promise.resolve(true)); ③
component.ngOnInit(); ④
fixture.detectChanges(); ⑤
expect(el.nativeElement.textContent.trim()).toBe('Logout'); ⑥
});
```
1 We issue our first change detection run so the view does it’s initial update.<br/>
2 We expect the button text to display Login <br/>
3 We change our AuthService so it returns a promise resolved to true. <br/>
4 We call component.ngOnInit(). <br/>
5 We issue our second change detection run. <br/>
6 We now expect the button text to read Logout. <br/>
If we ran the above code we would see it doesn’t pass -- response is still not resolved
<br/>It’s failing on the last expectation. By the time we run the last expectation the
AuthService.isAuthenticated() function hasn’t yet resolved to a value. Therefore the needsLogin
property on the LoginComponent hasn’t been updated.
## ways tto write asynchronous test
* Jasmines done function
* async and whenStable
* fakeAsync and tick
### Jasmines done function
Jasmine has a built-in way to handle async code and that’s by the passed in done function in the test
specs.<br/>
So far we’ve been defining our test specs without any parameters but it can take a parameter, a
done function which we call when all the async processing is complete <br/>
```markdown
it('Button label via jasmine.done', (done) => { ①
fixture.detectChanges();
expect(el.nativeElement.textContent.trim()).toBe('Login');
let spy = spyOn(authService,
'isAuthenticated').and.returnValue(Promise.resolve(true));
component.ngOnInit();
spy.calls.mostRecent().returnValue.then(() => { ②
fixture.detectChanges();
expect(el.nativeElement.textContent.trim()).toBe('Logout');
done(); ③
});
});
```
1 The jasmine test spec function is passed a function as the first param, we usually call this
parameter done.<br/>
2 We can add a callback function (using the spy) which is called when the promise returned from
isAuthenticated function resolved. In this function we know that the component has the new
value of needsLogin and we can add our additional expectation here. <br/>
3 When we are done with our asynchronous tasks we tell Jasmine via the done function <br/>
Jasmine lets us create asynchronous tests by giving us an explict done function which we call when
the test is complete.
### async and whenStable
```markdown
it('Button label via async() and whenStable()', async(() => { ①
fixture.detectChanges();
expect(el.nativeElement.textContent.trim()).toBe('Login');
spyOn(authService, 'isAuthenticated').and.returnValue(Promise.resolve(true));
fixture.whenStable().then(() => { ②
fixture.detectChanges();
expect(el.nativeElement.textContent.trim()).toBe('Logout');
});
component.ngOnInit();
}));
```
1. We wrap our test spec function in another function called async. <br/>
2. We place the tests we need to run after the isAuthenticated promise resolves inside this
function. <br/>
This async function executes the code inside it’s body in a special async test zone. This intercepts
and keeps track of all promises created in it’s body. <br/>
Only when all of those pending promises have been resolved does it then resolves the promise
returned from whenStable. <br/>
So by using the async and whenStable functions we now don’t need to use the Jasmine spy
mechanism of detecting when the isAuthenticated promise has been resolved<br/>
### fakeAsync and tick
```markdown
it('Button label via fakeAsync() and tick()', fakeAsync(() => { ①
expect(el.nativeElement.textContent.trim()).toBe('');
fixture.detectChanges();
expect(el.nativeElement.textContent.trim()).toBe('Login');
spyOn(authService, 'isAuthenticated').and.returnValue(Promise.resolve(true));
component.ngOnInit();
tick(); ②
fixture.detectChanges();
expect(el.nativeElement.textContent.trim()).toBe('Logout');
}));
```
1 Like async we wrap the test spec function in a function called fakeAsync.<br/>
2 We call tick() when there are pending asynchronous activities we want to complete <br/>
Like the async function the fakeAsync function executes the code inside it’s body in a special fake
async test zone. This intercepts and keeps track of all promises created in it’s body.<br/>
The tick() function blocks execution and simulates the passage of time until all pending
asynchronous activities complete.<br/>
So when we call tick() the application sits and waits for the promise returned from
isAuthenticated to be resolved and then lets execution move to the next line.<br/>
### what to use when
* The jasmine done function and spy callbacks. We attach specific callbacks to spies so we know when
promises are resolves, we add our test code to thos callbacks and then we call the done function.
This works but means we need to know about all the promises in our application and be able to
hook into them.<br/>
* We can use the Angular async and whenStable functions, we don’t need to track the promises
ourselves but we still need to lay our code out via callback functions which can be hard to read.<br/>
* We can use the Angular fakeAsync and tick functions, this additionally lets us lay out our async test
code as if it were synchronous.<br/>
