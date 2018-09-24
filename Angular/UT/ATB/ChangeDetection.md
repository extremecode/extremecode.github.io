# Jasmine
## Testing Change Detection
Trying to test whether changes in the state of our application trigger changes in the view without
the Angular Test Bed is complicated. However with the ATB it’s much simple
* How to inspect a components view.
* How to trigger change detection so a components view updates based on state changes in our
Application

## component to test
```markdown
@Component({
selector: 'app-login',
template: `
<a>
<span *ngIf="needsLogin()">Login</span>
<span *ngIf="!needsLogin()">Logout</span>
</a>
`
})
export class LoginComponent {
constructor(private auth: AuthService) {
}
needsLogin() {
return !this.auth.isAuthenticated();
}
}
```
## Test Specs
```markdown
import {TestBed, async, ComponentFixture} from '@angular/core/testing';
import {LoginComponent} from './login.component';
import {AuthService} from "./auth.service";
import {DebugElement} from "@angular/core"; ①
import {By} from "@angular/platform-browser"; ①
describe('Component: Login', () => {
let component: LoginComponent;
let fixture: ComponentFixture<LoginComponent>;
let authService: AuthService;
let el: DebugElement; ②
beforeEach(() => {
// refine the test module by declaring the test component
TestBed.configureTestingModule({
declarations: [LoginComponent],
providers: [AuthService]
});
// create component and test fixture
fixture = TestBed.createComponent(LoginComponent);
// get test component from the fixture
component = fixture.componentInstance;
// UserService provided to the TestBed
authService = TestBed.get(AuthService);
// get the "a" element by CSS selector (e.g., by class name)
el = fixture.debugElement.query(By.css('a')); ③
});
it('login button hidden when the user is authenticated', () => {
// To being with Angular has not done any change detection so the content is
blank.
expect(el.nativeElement.textContent.trim()).toBe('');
// Trigger change detection and this lets the template update to the initial value
which is Login since by
// default we are not authenticated
fixture.detectChanges();
expect(el.nativeElement.textContent.trim()).toBe('Login');
// Change the authetication state to true
spyOn(authService, 'isAuthenticated').and.returnValue(true);
// The label is still Login! We need changeDetection to run and for angular to
update the template.
expect(el.nativeElement.textContent.trim()).toBe('Login');
// Which we can trigger via fixture.detectChange()
fixture.detectChanges();
// Now the label is Logout
expect(el.nativeElement.textContent.trim()).toBe('Logout');
});
});
```
1. We’ve imported a few more classes that are needed when interacting with a components view,
DebugElement and By. <br/>
2. We have another variable called el which holds something called a DebugElement. <br/>
3 .We store a reference to a DOM element in our el variable. <br/>
The fixture as well as holding an instance of the component also holds a reference to something
called a DebugElement, this is a wrapper to the low level DOM element that represents the
components view, via the debugElement property. <br/>
We can get references to other child nodes by querying this debugElement with a By class. The By
class lets us query using a a number of methods, one is via a css class like we have in our example
another way is to request by a type of directive like By.directive(MyDirective).
