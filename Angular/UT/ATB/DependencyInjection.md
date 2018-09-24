# Depenedency Inection
## how we test earlier
* Resolving via TestBed
The TestBed acts as a dummy Angular Module and we can configure it like one including with a set
of providers
```markdown
TestBed.configureTestingModule({
providers: [AuthService]
});
```
We can then ask the TestBed to resolve a token into a dependency using it’s internal injector
```markdown
testBedService = TestBed.get(AuthService);
```
## inject function
The inject function wraps the test spec function but lets us also inject dependencies using the
parent injector in the TestBed
```markdown
inject(
[token1, token2, token2],
(dep1, dep2, dep3) => { }
)
```
The first param is an array of tokens we want to resolve dependencies for, the second parameter is
a function whose arguments are the resolved dependencies.
Using the inject function:<br/>
• Makes it clear what dependencies each spec function uses. <br/>
• If each test spec requires different mocks and spys this is a better solution that resolving it once
per test suite.<br/>
_this will eventually become a decorator_
```markdown
@Inject (dep1: Token1, dep2: Token2) => { ... }
```
### Overriding the components providers
Before we create a component via the TestBed we can override it’s providers. Lets imagine we have
a mock AuthService
```markdown
class MockAuthService extends AuthService {
isAuthenticated() {
return 'Mocked';
}
}
```
We can override the components providers to use this mocked AuthService
```markdown
TestBed.overrideComponent(LoginComponent,
  {set:{providers:[{provide:AuthService,useClass:MockAuthService}]}});
});
```
### Resolving via the component injector
Now our component has been configured with it’s own providers it will therefore have a child
injector. <br/>
When the component is created since it has it’s own injector it will resolve the AuthService itself
and not forward the request to it’s parent TestBed injector. <br/>
If we wanted to get the same instance of dependency that was passed to the component constructor
we need to resolve using the component injector, we can do that through the component fixture <br/>
```markdown
componentService = fixture.debugElement.injector.get(AuthService);
```

```markdown
import {TestBed, ComponentFixture, inject} from '@angular/core/testing';
import {LoginComponent} from './login.component';
import {AuthService} from "./auth.service";
class MockAuthService extends AuthService {
isAuthenticated() {
return 'Mocked';
}
}
describe('Component: Login', () => {
let component: LoginComponent;
let fixture: ComponentFixture<LoginComponent>;
let testBedService: AuthService;
let componentService: AuthService;
beforeEach(() => {
// refine the test module by declaring the test component
TestBed.configureTestingModule({
declarations: [LoginComponent],
providers: [AuthService]
});
// Configure the component with another set of Providers
TestBed.overrideComponent(
LoginComponent,
{set: {providers: [{provide: AuthService, useClass: MockAuthService}]}}
);
// create component and test fixture
fixture = TestBed.createComponent(LoginComponent);
// get test component from the fixture
component = fixture.componentInstance;
// AuthService provided to the TestBed
testBedService = TestBed.get(AuthService);
// AuthService provided by Component, (should return MockAuthService)
componentService = fixture.debugElement.injector.get(AuthService);
});
it('Service injected via inject(...) and TestBed.get(...) should be the same
instance',
inject([AuthService], (injectService: AuthService) => {
expect(injectService).toBe(testBedService);
})
);
it('Service injected via component should be and instance of MockAuthService', () =>
{
expect(componentService instanceof MockAuthService).toBeTruthy();
});
});
```
### key points
* We can resolve dependencies in our tests using a number of methods.<br/>
* We can resolve using the the test bed itself, usually in the beforeEach function and store the
* resolved dependencies for use in our test specs.<br/>
* We can resolve using the inject function at the start of each test spec.<br/>
* We can also override the default providers for our components using the TestBed.<br/>
* We can then also use the components child injector to resolve tokens.<br/>
