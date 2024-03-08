# Data types: Object keys, values and entries

This article is about object keys, values and entries in JavaScript.

## Object kyes, values and entries
```javascript
let user = {
  name: "John",
  age: 30
};

// Object.keys(user) = ["name", "age"]
// Object.values(user) = ["John", 30]
// Object.entries(user) = [ ["name","John"], ["age",30] ]
```

**Object.keys/values/entries ignore symbolic properties**

Just like a `for..in` loop, these methods ignore properties that use Symbol(...) as keys.

Usually that’s convenient. But if we want symbolic keys too, then there’s a separate method `Object.getOwnPropertySymbols` that returns an array of only symbolic keys. Also, there exist a method `Reflect.ownKeys(obj)` that returns all keys.

## Transforming objects
Objects lack many methods that exist for arrays, e.g. `map`, `filter` and others.

If we’d like to apply them, then we can use `Object.entries` followed by `Object.fromEntries`.

## Questions
1. What values does Object.keys/values/entries return?
2. How can we access symbolic values?
3. How can we use map/filter/etc. methods with objects?