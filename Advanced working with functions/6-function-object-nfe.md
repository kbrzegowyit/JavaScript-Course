# Advanced working with functions: Function Object, NFE

This article is about the function object, NFE in JavaScript.

## Function object
A function in JavaScript is a value. Its type is an object.

The properties of the function:
* *name* - contains function's name,
* *length* - contains a number of function arugments (the rest parameter is not counted),

We can also add custom properties if needed.

## Named Function Expression
Referes to FEs that have names.

```javascript
let sayHi = function func(who) {
  alert(`Hello, ${who}`);
};
```

What are the adventages:
* allows function to reference itself internally,
* not visible outside of the function.

## Questions
1. What is a function in JS?
2. Describe the parameters of the function.
3. What are NFEs?