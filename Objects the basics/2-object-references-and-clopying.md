# Objects the basics: Object references and copying

This article is about objects references in JavaScript.

## References and Copying
- `objects` are stored and copied by reference.

- `string`, `number`, `boolean`, etc are stored and copied by value.

> A variable assigned to an object stores not the object itself, but its **address in memory** - in other words **a reference** to it.

> When an object is copied, the reference is copied, but the object itself is not duplicated.

## Comparison
Variables with references to objects are only equal if they point to the same address in memory.

## Cloning
### Shallow copy
We can use `Object.assigne` or `clone = {...object}` (spread syntax).

### Deep copy
In order to clone nasted object we can use the `structuredClone` or `_.cloneDeep` function, which is built into JavaScript.

## Questions
1. What types are stored and copied by reference and what by value?
2. What does it mean that a variable has a reference to something?
3. What does it happen when a variable with a reference to an object is copied?
4. How are objects compared?
5. How can we do shallow clone of an object using built-in methods or syntax?
6. How can we do deep clone of an object using built-in methods or syntax?