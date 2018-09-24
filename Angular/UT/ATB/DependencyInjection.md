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
TestBed.overrideComponent(
LoginComponent,
{set: {providers: [{provide: AuthService, useClass: MockAuthService}]}}
);
```

```markdown
```

```markdown
```
