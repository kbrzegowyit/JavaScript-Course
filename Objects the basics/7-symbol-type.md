# Objects the basics: Objects methods, "this"

This article is about the symbol type in JavaScript.

## Symbols
They represnet unique identifiers.

We can create the symbol as follows.

```javascript
let id = Symbol(); // without description

let id = Symbol("id"); // with description
```

Symbols are guaranteed to be **unique**. The description is just a label and it doesn't affect anything.

## Hidden properties
We can use symbols when using a third-party code. If we don't want to override the properties of an object, we can use symbols.

```javascript
const obj = { name: "John" };

const name = Symbol("name");

obj[name] = 'Super Boss';

console.log(obj.name, obj[name]); // "John" "Super Boss"

console.log(obj) // { name: 'John', Symbol(name): 'Super Boss' }
```

## for..in
Symbols are skipped by `for..in` and `Object.keys(obj)`. This is a part of the general `hiding symbolic properties` pronciple.

Note that `Object.assign` copies all properties, symbols too.

## Global symbols
We can register our symbol in the global registry in order to share symbols between different application parts.

```javascript
let id = Symbol.for("id"); // returns the symbol (creates if it doesn't exist)

let key = Symbol.keyFor(sym) // returns a name by global symbol
```

>There are also predefined symbols that we can use.

## Questions
1. What are the symbols?
2. How can we create the symbol?
3. Does the description affect anything?
4. How can we avoid overriding some properties of an object?
5. Do we have an access to the symbols in for..in?
6. Are the symbols copied by `Object.assing`?
7. What are the global symbols?
8. How can we read or create a global symbol?