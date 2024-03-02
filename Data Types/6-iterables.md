# Data types: Iterables

This article is about iterables in JavaScript.

## Symbol.iterator
Iterable objects are a generalization of arrays. That’s a concept that allows us to make any object useable in a `for..of` loop.

If an object isn’t technically an array, but represents a collection (list, set) of something, then `for..of` is a great syntax to loop over it.

If you create your own object, it won't be iterable by defaul. If you want it to be so, you need to implement an appriopriate method - `Symbol.iterator`.

```javascript
let range = {
    from: 1,
    to: 5
};
  
range[Symbol.iterator] = function() {
    const arr = [];

    for (let key in this) {
        arr.push(this[key]);
    }

    return {
      current: 0,

      next() {
        if (this.current < arr.length) {
          return { done: false, value: arr[this.current++] };
        } else {
          return { done: true };
        }
      }
    };
};
  
for (let num of range) {
    console.log(num);
}
```

The result of next() must have the form `{ done: Boolean, value: any }`, where done=true means that the loop is finished, otherwise value is the next value.

## String is iterable
Arrays and strings are most widely used built-in iterables.

## Iterables and array-likes
*Iterables* are objects that implement the Symbol.iterator method, as described above.

*Array-likes* are objects that have indexes and length, so they look like arrays.

And here’s the object that is array-like, but not iterable:

```javascript
let arrayLike = { // has indexes and length => array-like
  0: "Hello",
  1: "World",
  length: 2
};

// Error (no Symbol.iterator)
for (let item of arrayLike) {}
```

## Array.from
The method takes an *iterable* or *array-like* value and makes a “real” Array from it. Then we can call array methods on it.

`Array.from(arrayLike[, mapFn, thisArg])`

*mapFn* - can be a function that will be applied to each element before adding it to the array.

## Questions
1. How can we make an object iterable?
2. What should the next() function return?
3. Is `string` iterable?
4. What are iterables and array-like objects?
5. How does `Array.from` work?