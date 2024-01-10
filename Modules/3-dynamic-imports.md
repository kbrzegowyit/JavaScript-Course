# Modules: Dynamic imports

This article is about dynamic imports in JavaScript.

## The import() expression
The expression loads the module and returns a promise that resolves into a module object that contains all its exports.

We can import its variables in the following way.

- named exports
```
let {hi, bye} = await import('./say.js');
```
- default export
```
let obj = await import('./say.js');
let say = obj.default;
// or, in one line: let {default: say} = await import('./say.js');

say();
```

## Questions
1. What are dynamic imports?
2. How can we import named and default export?