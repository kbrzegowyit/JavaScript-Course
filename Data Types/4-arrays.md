# Data types: Arrays

This article is about arrays in JavaScript.

## Declaration
We can create an array using `let arr = []` lub `let arr = new Array()`;

## Access to the elements
We can access the elements of an array using `arr[pos]` or `arr.at(pos)`.

The latter works in the same way as for strings.

## Internals
An array is a special kind of object. The engine tries to store its elements in the contiguous memory area, one after another, to make arrays work really fast. 

But they all break if we quit working with an array as with an “ordered collection” and start working with it as if it were a regular object.

The ways to misuse an array:

- Add a non-numeric property like arr.test = 5.
- Make holes, like: add arr[0] and then arr[1000] (and nothing between them).
- Fill the array in the reverse order, like arr[1000], arr[999] and so on.

## Performance
Adding and removing elements from the begining of the array is slower than doing it from the end of the array.

This is because the elements have to be moved every time.

## Loops
To iterate over an array we should use `for..of`.

## Length
Tt is actually not the count of values in the array, but the greatest numeric index plus one.

If we increase it manually, nothing interesting happens. But if we decrease it, the array is truncated. The process is irreversible.

## toString
Arrays have their own implementation of toString method that returns a comma-separated list of elements.

```javascript
let arr = [1, 2, 3];

alert( arr ); // 1,2,3
alert( String(arr) === '1,2,3' ); // true
```

Arrays do not have Symbol.toPrimitive, neither a viable valueOf, they implement only toString conversion

## Questions
1. How can we create an array?
2. How can we access the elements of an array?
3. How is the array represented internally?
4. Describe the impact on performance while adding and removing items.
5. Which loop should we use with arrays?
6. What is lenght porperty?
7. What does it happen when we increase and decrease it?
8. How does array conversion work?