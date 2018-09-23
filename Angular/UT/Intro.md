# Jasmine <br /> 
_Jasmine is a javascript testing framework that supports a software development practice called
Behaviour Driven Development, or BDD for short. It’s a specific flavour of Test Driven Development
(TDD).<br />
Jasmine, and BDD in general, attempts to describe tests in a human readable format so that nontechnical
people can understand what is being tested. However even if you are technical reading
tests in BDD format makes it a lot easier to understand what’s going on_ <br/>

## method to test
```markdown
function helloWorld() {
return 'Hello world!';
}
```
## test case
```markdown
describe('Hello world', () => { ①
it('says hello', () => { ②
expect(helloWorld()) ③
.toEqual('Hello world!'); ④
});
});
```
## Description
```markdown
① The describe(string, function) function defines what we call a Test Suite, a collection of
individual Test Specs.<br/>
② The it(string, function) function defines an individual Test Spec, this contains one or more
Test Expectations.<br/>
③ The expect(actual) expression is what we call an Expectation. In conjunction with a Matcher it
describes an expected piece of behaviour in the application.<br/>
④ The matcher(expected) expression is what we call a Matcher. It does a boolean comparison with
the expected value passed in vs. the actual value passed to the expect function, if they are false
the spec fails.<br/>
```

