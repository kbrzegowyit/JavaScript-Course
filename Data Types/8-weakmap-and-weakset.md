# Data types: WeakMap and WeakSet

This article is about WeakMap and WeakSet in JavaScript.

## WeakMap
The first difference between `Map` and `WeakMap` is that keys must be objects, not primitive values.

If we use an object as the key in it, and there are no other references to that object – it will be removed from memory (and from the map) automatically.

`WeakMap` has only the following methods:
- weakMap.set(key, value)
- weakMap.get(key)
- weakMap.delete(key)
- weakMap.has(key)

**Use case: caching**
We can use it to store the results for keys calculating it for the first time only. 

## WeakSet
It behaves similarly:

- It is analogous to Set, but we may only add objects to WeakSet (not primitives).
- An object exists in the set while it is reachable from somewhere else.
- Like Set, it supports add, has and delete, but not size, keys() and no iterations.

**Use case**
We can add users to WeakSet to keep track of those who visited our site.

The  most notable limitation of WeakMap and WeakSet is the absence of iterations, and the inability to get all current content

## Questions
1. What is the WeakMap keys type?
2. When a value in WeakMap will be deleted?
3. List the methods of the WeakMap.
4. Give some use case for the WeakMap.
5. Give some use case for the WeakSet.
6. What is the biggest limitation in case of WeakMap and WeakSet?