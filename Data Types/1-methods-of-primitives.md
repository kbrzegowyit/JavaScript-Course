# Data types: Methods Of Primitives

This article is about data types and methods of primitives in JavaScript.

## A primitive as an object
There are many common operations we can do with `string`, `boolean`, etc. In order not to implement them ourselves, they are build-in to the language. Therefore, when we call a method on a promitive, the following things happen:

1. In the moment when a method is invoked on the primitive, a special object is created.
2. It perfoms the operation and is destroyed.

The objects are called "object wrappers".

>We can crate a primitive as follow `const one = new Number(1)`. However, this approach isn't recommended, because the value is treated as an `object`. Thus, it may lead to different mistakes.

>Using the same functions without operator `new` is totally fine and useful. They convert a value to the coresponding type.

## Questions
1. What are object wrappers?
2. Why should we avoid using e.g. `new Number(1)`?
3. How can we use "object wrappers" to conver a value?