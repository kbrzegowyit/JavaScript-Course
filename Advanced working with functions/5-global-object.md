# Advanced working with functions: Global Object

This article is about the global object in JavaScript.

## Global Object
It provides variables and functions that are available anywhere.

In a browser it is named `window`, for Node.js it is `global`.

> In a browser, global functions and variables declared with `var` become the property of the global object. Unless you are using modules.

## Using for polyfills
It is used to test the support of modern language features.

If there’s none (say, we’re in an old browser), we can create “polyfills”: add functions that are not supported by the environment, but exist in the modern standard.

```javascript
if (!window.Promise) {
  window.Promise = ... // custom implementation of the modern language feature
}
```

## Questions
1. What is the global object?
2. What is it named in a browser versus Node.js?
3. What does become part of the global object in the browser? When?