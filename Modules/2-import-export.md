# Modules: Export and Import

This article is about export and import in JavaScript modules.

## Export before and apart from declaration
- We can place `export` before a variable, function or a class. 
``` 
// export an array
export let months = ['Jan', 'Feb', 'Mar'];

// export a constant
export const MODULES_BECAME_STANDARD_YEAR = 2015;

// export a class
export class User {
  constructor(name) {
    this.name = name;
  }
}
```
- We can place `export` separately.
```
// say.js
function sayHi(user) {
  alert(`Hello, ${user}!`);
}

function sayBye(user) {
  alert(`Bye, ${user}!`);
}

export {sayHi, sayBye}; // a list of exported variables
```

## Import everything
- import * - if there is a lot to import, we can import everything as an object.
```
// 📁 main.js
import * as say from './say.js';
```

## import / export "as"
- import "as" - we can import under different names.
```
// 📁 main.js
import {sayHi as hi, sayBye as bye} from './say.js';
```
- export "as" - similar syntax exists for export.
```
// 📁 say.js
...
export {sayHi as hi, sayBye as bye};
```

## Export default
- one per file
- export without naming (possibly)
- import without curly braces
- export default separately from its definition
```
function sayHi(user) {
  alert(`Hello, ${user}!`);
}

export {sayHi as default}
```
- import the default export along with a named one
```
// 📁 main.js
import {default as User, sayHi} from './user.js';
```

> There is a rule that imported variables should correspond to file names

## Re-export
It's useful when we want to export other modules from one place - one module.
```
// 📁 auth/index.js
// re-export login/logout
export {login, logout} from './helpers.js';

// re-export the default export as User
export {default as User} from './user.js';
```

If we want to export named exports and default we need to use two statemetns.

```
export * from './user.js'; // to re-export named exports
export {default} from './user.js'; // to re-export the default export
```

## Questions
1. Where can we place `export` when we want to export a variable, function or a class?
2. How can we import evertying at once?
3. How can we change names of exported and imported elements?
4. List the main features of `export default`.
5. How can we export default separately from its definition?
6. How should we name imported variables as default?
7. How we can re-export named variables, default and both?
