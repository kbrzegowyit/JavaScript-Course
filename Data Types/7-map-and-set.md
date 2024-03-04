# Data types: Iterables

This article is about iterables in JavaScript.

## Map
Map is a collection of keyed data items, just like an Object. But the main difference is that Map allows keys of any type.

>**`map[key]` isn't the right way to use a `Map`.**
Although map[key] also works, e.g. we can set map[key] = 2, this is treating map as a plain JavaScript object, so it implies all corresponding limitations (only string/symbol keys and so on).

So we should use map methods: set, get and so on.

>**The insertion order is used**
The iteration goes in the same order as the values were inserted. Map preserves this order, unlike a regular Object.

## Object → Map and Map → Object
### Object.entries: Map from Object
We can create a map from an array with key/value pairs.

```javascript
// array of [key, value] pairs
let map = new Map([
  ['1',  'str1'],
  [1,    'num1'],
  [true, 'bool1']
]);
```

If we have a plain object, and we’d like to create a Map from it, then we can use built-in method `Object.entries(obj)` that returns an array of key/value pairs for an object exactly in that format.

### Object.fromEntries: Object from Map
We can use `Object.fromEntries` to get a plain object from Map.

```javascript
let obj = Object.fromEntries(map.entries()); // make a plain object (*)
// OR
let obj = Object.fromEntries(map); // omit .entries()
```

## Set
A Set is a special type collection – “set of values” (without keys), where each value may occur only once.

The alternative to `Set` could be an array of users, and the code to check for duplicates on every insertion using `arr.find`. But the performance would be much worse, because this method walks through the whole array checking every element. Set is much better optimized internally for uniqueness checks.

### Iteration
We can loop over a set either with `for..of` or using `forEach`:

>**The insertion order is used**
The iteration goes in the same order as the values were inserted.

## Questions
1. What is the main difference between `Map` and `Object`?
2. Why should we avoid using `map[key]`?
3. What will happen when we use object as key with objects?
4. What is the order of elements in `Map`?
5. How can we create a map from an array?
6. How can we create a map from an object?
7. How can we create an object from a map?
8. How does `Set` work?
9. What is the order of elements in `Set`?