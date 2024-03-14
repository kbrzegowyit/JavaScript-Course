# Advanced working with functions: Rest Parameters And Spread Syntax

This article is about rest parameters and spread syntax in JavaScript.

## Rest parameters
The dots literally mean “gather the remaining parameters into an array”.

The ...rest must always be last.

```javascript
function sumAll(...args) { // args is the name for the array
  let sum = 0;

  for (let arg of args) sum += arg;

  return sum;
}

alert( sumAll(1) ); // 1
alert( sumAll(1, 2) ); // 3
alert( sumAll(1, 2, 3) ); // 6
```

## Spread syntax
When `...arr` is used in the function call, it “expands” an iterable object `arr` into the list of arguments.

Here we use the spread syntax to turn the string into array of characters:
```javascript
let str = "Hello";

alert( [...str] ); // H,e,l,l,o
```

The spread syntax internally uses iterators to gather elements, the same way as `for..of` does.

## Copy an array/object
Here is how we can copy an array:
```javascript
let arr = [1, 2, 3];

let arrCopy = [...arr]; // spread the array into a list of parameters
                        // then put the result into a new array

// do the arrays have the same contents?
alert(JSON.stringify(arr) === JSON.stringify(arrCopy)); // true

// are the arrays equal?
alert(arr === arrCopy); // false (not same reference)

// modifying our initial array does not modify the copy:
arr.push(4);
alert(arr); // 1, 2, 3, 4
alert(arrCopy); // 1, 2, 3
```
and an object:
```javascript
let obj = { a: 1, b: 2, c: 3 };

let objCopy = { ...obj }; // spread the object into a list of parameters
                          // then return the result in a new object

// do the objects have the same contents?
alert(JSON.stringify(obj) === JSON.stringify(objCopy)); // true

// are the objects equal?
alert(obj === objCopy); // false (not same reference)

// modifying our initial object does not modify the copy:
obj.d = 4;
alert(JSON.stringify(obj)); // {"a":1,"b":2,"c":3,"d":4}
alert(JSON.stringify(objCopy)); // {"a":1,"b":2,"c":3}
```

So we used `let arrCopy = [...arr];` and `let objCopy = { ...obj };` to copy the elements. It's much shorter than `let objCopy = Object.assign({}, obj)` or for an array `let arrCopy = Object.assign([], arr)` so we prefer to use it whenever we can.

## Questions
1. What does the rest paramter mean?
2. What does the spread syntax do?
3. How does the syntax work with strings?
4. How should we perform shallow copying in the case of arrays and objects?