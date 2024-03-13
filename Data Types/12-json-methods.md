# Data types: JSON methods, toJSON

This article is about JSON methods in JavaScript.

## Stringify
Converts objects into JSON.

The method `JSON.stringify(object)` takes the object and converts it into a string.

JSON is data-only language-independent specification, so some JavaScript-specific object properties are skipped:
* Function properties (methods)
* Symbolic keys and values
* Properties that store `undefined`

`let json = JSON.stringify(value[, replacer, space])`

**value**

A value to encode.

**replacer**

Array of properties to encode or a mapping function function(key, value).

**space**

Amount of space to use for formatting or string as indentation.

## toJSON
Like toString for string conversion, an object may provide method toJSON for to-JSON conversion.

## JSON.parse
`let value = JSON.parse(str[, reviver]);`

**str**

JSON-string to parse.


**reviver**
Optional function(key,value) that will be called for each (key, value) pair and can transform the value.


```javascript
let str = '{"title":"Conference","date":"2017-11-30T12:00:00.000Z"}';

let meetup = JSON.parse(str, function(key, value) {
  if (key == 'date') return new Date(value);
  return value;
});

alert( meetup.date.getDate() ); // now works!
```

## Questions
1. What is the `JSON.stringify` method responsible for?
2. What properties are skipped by the method?
3. How can we specify the keys we want to parse?
4. How can we specify the indentation?
5. How can we specify behaviour of an object during JSON conversion?
6. How can we transform JSON values during parsing?
