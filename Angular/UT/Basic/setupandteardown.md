# Jasmine and karma
## inbuilt matchers
```markdown
expect(array).toContain(member);
expect(fn).toThrow(string);
expect(fn).toThrowError(string);
expect(instance).toBe(instance);
expect(mixed).toBeDefined();
expect(mixed).toBeFalsy();
expect(mixed).toBeNull();
expect(mixed).toBeTruthy();
expect(mixed).toBeUndefined();
expect(mixed).toEqual(mixed);
expect(mixed).toMatch(pattern);
expect(number).toBeCloseTo(number, decimalPlaces);
expect(number).toBeGreaterThan(number);
expect(number).toBeLessThan(number);
expect(number).toBeNaN();
expect(spy).toHaveBeenCalled();
expect(spy).toHaveBeenCalledTimes(number);
expect(spy).toHaveBeenCalledWith(...arguments);
```
## setup and teardown
Sometimes in order to test a feature we need to perform some setup, perhaps it’s creating some test
objects. Also we may need to perform some cleanup activities after we have finished testing,
perhaps we need to delete some files from the hard drive.<br/>
These activities are called setup and teardown (for cleaning up) and Jasmine has a few functions we
can use to make this easier:<br/>
beforeAll<br/>
This function is called once, before all the specs in describe test suite are run.<br/>
afterAll<br/>
This function is called once after all the specs in a test suite are finished.<br/>
beforeEach<br/>
This function is called before each test specification, it function, has been run.<br/>
afterEach<br/>
This function is called after each test specification has been run.<br/>
```markdown
describe('Hello world', () => {
let expected = "";
beforeEach(() => {
expected = "Hello World";
});
afterEach(() => {
expected = "";
});
it('says hello', () => {
expect(helloWorld())
.toEqual(expected);
});
});
```
## Karma
Manually running Jasmine tests by refreshing a browser tab repeatedly in different browsers
every-time we edit some code can become tiresome.<br/>
Karma is a tool which lets us spawn browsers and run jasmine tests inside of them all from the
command line. The results of the tests are also displayed on the command line.<br/>
Karma can also watch your development files for changes and re-run the tests automatically.
