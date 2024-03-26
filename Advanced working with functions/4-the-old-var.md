# Advanced working with functions: Variable scope, closure

This article is about the old var in JavaScript.

## No block scope
`var` variables are either function-scope or global-scope as it ignores block-scope.

## Tolerates redeclarations
`var` variables can be declarated many times.

## Declaration below their use
There is a mechanism called hoisting (raising), because all the `var`s are hoisted to the top of the function.

**Declarations are hoisted but assignments are not.**

```javascript
function sayHi() {
  var phrase; // declaration works at the start...

  alert(phrase); // undefined

  phrase = "Hello"; // ...assignment - when the execution reaches it.
}

sayHi();
```

## IIFE
*Function Expression*:
* immediately created and called
* has its own private variables
* has no name

## Questions
1. What are the `var` scopes?
2. What happens when we redeclare the var variable?
3. What does it mean that `var` variables are hoisted?
4. What is the IIFE?