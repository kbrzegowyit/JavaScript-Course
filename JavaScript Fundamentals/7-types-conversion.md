# Data types: Primitive types conversion
Opracowanie dotyczące konwersji typów podstawowych (prymitywnych) do `string`, `number`, `boolean`.

## String
Bardzo oczywista, w zasadzie wszystko jest pakowane w cudzysłowia. 
Ma miejsce kiedy potrzebujemy stringa z wartości.

```javascript
// Booleans
console.log(String(true))   // "true"
console.log(String(false))  // "false"

// Numbers 
console.log(String(11)) // "11"

// Undefined 
console.log(String(undefined)) // "undefined"

// Null 
console.log(String(null)) // "null"
```

## Number
Dzieje się automatycznie w funkcjach i wyrażeniach matematycznych.

```javascript
// Booleans
console.log(true * true) // 1 -> Number(true) = 1, Number(false) = 0
console.log(true + true) // 2
console.log(true / false) // Infinity 

// Strings
console.log("3" / "2"); // 1.5
console.log("3" * "2"); // 6
console.log("3" - "2"); // 1
console.log(Math.pow("3", "2")); // 9
// [Wyjąteki!]
console.log("4" + "2"); // 42 -> konkatenacje, type wynikowy to string
console.log("" + 2) // 2 -> Number("") = 0
console.log("invalid") // NaN

// Undefined 
console.log(Number(undefined)) // NaN 

// Null 
console.log(Number(null)) // 0
```

## Boolean
Bardzo prosta i intuicyjna.
```javascript
// Empty values: 0 (Number), undefined, null, NaN
console.log(Boolean(0)); // false
console.log(Boolean(undefined)); // false
console.log(Boolean(null)); // false
console.log(Boolean(NaN)); // false
console.log(Boolean("")); // false, empty string
// [Uwaga!] None-empty string jest zawsze true
console.log(Boolean("0")); // true
console.log(Boolean(" ")); // true, spacja (biały znak)
            
// Other values are true
```

## Pytania
1. Omów konwersję typów podstawowych do typu `string`.
2. Omów konwersję typów podstawowych do typu `number`.
3. Omów konwersję typów podstawowych do typu `boolean`.
 
**Zwróć uwagę na wyjątki!**
