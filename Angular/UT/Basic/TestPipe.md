# Jasmine and karma
_Whenever we create files using the CLI as well as creating the main code file it also creates simple
jasmine spec file named the same as the main code file but ending in .spec.ts_
```markdown
ng generate pipe my
```
This would create two files:<br\>
* my-pipe.ts - This is the main code file where we put the code for the pipe.
* my-pipe.spec.ts - This is the jasmine test suite for the pipe.
```markdown
import { TestBed, async } from '@angular/core/testing';
import { MyPipe } from './my.pipe';
describe('Pipe: My', () => {
it('create an instance', () => {
let pipe = new MyPipe();
expect(pipe).toBeTruthy();
});
});
```
to run test we need to do ng test on cli
```markdown
```
```markdown
```
```markdown
```
