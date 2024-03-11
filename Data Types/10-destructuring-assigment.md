# Data types: Destructuring assigment

This article is about destructuring assigment in JavaScript.

## Array destructuring
It wroks with any iterable on the right-side. Actually, we can use it with any iterable, not only arrays.

```javascript
let [a, b, c] = "abc"; // ["a", "b", "c"]
let [one, two, three] = new Set([1, 2, 3]);
```
That works, because internally a destructuring assignment works by iterating over the right value. It’s a kind of syntax sugar for calling `for..of` over the value to the right of `=` and assigning the values.

## Object destructuring
Just like with arrays or function parameters, default values can be any expressions or even function calls. They will be evaluated if the value is not provided.
```javascript
let options = {
  title: "Menu"
};

let {width = prompt("width?"), title = prompt("title?")} = options;

alert(title);  // Menu
alert(width);  // (whatever the result of prompt is)
```

If we don't use `let`, we should use `(...)` to wrap the expression.
```javascript
let title, width, height;

// okay now
({title, width, height} = {title: "Menu", width: 200, height: 100});

alert( title ); // Menu
```

## Smart function parameters
There are times when a function has many parameters, most of which are optional. We can pass parameters as an object, and the function immediately destructurizes them into variables.

The full syntax is the same as for a destructuring assignment:
```javascript
function({
  incomingProperty: varName = defaultValue
  ...
})
```


## Questions
1. What is called internally during destructuring an array?
2. How can we set default value, if not provided?
3. How can we destructuring an object if there is no `let`?
4. How can we use destructurizing with functions?