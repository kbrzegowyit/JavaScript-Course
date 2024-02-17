# Data types: Numbers

This article is about numbers in JavaScript.

## More ways to write a number

We can use the underscore  `_` to make the number more readable e.g `100_000`.

We can use the letter `e` to avoid writing long sequences of zeros.

```javascript
1e3 === 1 * 1000 //1 * 10^3
1.45e2 === 1.45 * 100 //1.45 * 10^2
```

## Hex, binary and octal numbers

- `0b` - binary
- `0o` - octal
- `0x` - hexadecimal

## toString(base)

The method `num.toString(base)` returns a string representation of `num` in the numeral system with the given `base`.

The base can vary from 2 to 36. By default it’s 10.

## Rounding

### Integer

- `Math.floor` Rounds down: 3.1 becomes 3, and -1.1 becomes -2.
- `Math.ceil` Rounds up: 3.1 becomes 4, and -1.1 becomes -1.
- `Math.round` Rounds to the nearest integer: 3.1 becomes 3, 3.6 becomes 4, the middle case: 3.5 rounds up to 4 too.
- `Math.trunc` Removes anything after the decimal point without rounding: 3.1 becomes 3, -1.1 becomes -1.

### Decimal

- `num.toFixed(n)` Rounds the number to n digits after the point and returns a **string** representation of the result.

## isFinite and isNaN

- `isNaN` **converts** its argument to a number and test is for being `NaN`.
- `isFinite` **converts** its argument to a number and returns true if it’s a regular number, not `NaN`/`Infinity`/`-Infinity`

`Number.isNaN` and `Number.isFinite` methods are the more “strict” versions of isNaN and isFinite functions. They do not autoconvert their argument into a number, but check if it belongs to the number type instead.

`Object.is` compares values like `===`, but is more reliable for two edge cases:
- `Object.is(NaN, NaN) === true`
- `Object.is(0, -0) === false`

Normally, the first case is equal false and the second one is equal true.

## parseInt and parseFloat

### Strict conversion
Numeric conversion using a plus `+` or `Number()` is strict. If a value is not exactly a number, it fails.

### parseInt and parseFloat
They “read” a number from a string until they can’t. In case of an error, the gathered number is returned. The function parseInt returns an integer, whilst parseFloat will return a floating-point number.

### Error
There are situations when parseInt/parseFloat will return NaN. It happens when no digits could be read.

## Questions
1. How can we write numbers in JavaScript?
2. What other number systems are additionally supported?
3. How can we convert number to a string in another numerical system?
4. How can we round numbers to integers and decimals?
5. What are `isNaN` and `isFinite`?
6. What is the difference between them?
7. What are edge cases in case of `Object.is` for `NaN` and `0/-0`?
8. How does `+` and `Number()` work?
9. How does `parseInt` and `parseFloat` work?
10. When do they throw an error?