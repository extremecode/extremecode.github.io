# JAsmine and karma
When to use ATB
We will continue to use ATB for the rest of this section because: <br/>
* It allows us to test the interaction of a directive or component with it’s template.
* It allows us to easily test change detection.
* It allows us to test and use Angulars DI framework,
* It allows us to test using the NgModule configuration we use in our application.
* It allows us to test user interaction via clicks & input fields
```markdown
import {TestBed, ComponentFixture} from '@angular/core/testing';
import {LoginComponent} from './login.component';
import {AuthService} from "./auth.service";
describe('Component: Login', () => {
let component: LoginComponent;
let fixture: ComponentFixture<LoginComponent>;
let authService: AuthService;
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
});
it('canLogin returns false when the user is not authenticated', () => {
spyOn(authService, 'isAuthenticated').and.returnValue(false);
expect(component.needsLogin()).toBeTruthy();
expect(authService.isAuthenticated).toHaveBeenCalled();
});
it('canLogin returns false when the user is not authenticated', () => {
spyOn(authService, 'isAuthenticated').and.returnValue(true);
expect(component.needsLogin()).toBeFalsy();
expect(authService.isAuthenticated).toHaveBeenCalled();
});
});
```
