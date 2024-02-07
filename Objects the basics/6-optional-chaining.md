# Objects the basics: Optional chaining

This article is about the optional chaining in JavaScript.

## Optional chaining
Optional chaining `?.` stops the evaluation if the value before `?.` is `undefined` or `null` and returns `undefined`.

In other words, `value?.prop`:
- works as `value.prop` if `value` exists (not `null` or `undefined`),
- otherwise (when the `value` is `null`/`undefined`) it returns `undefined`.

>Keep in mind that the value must be declared, otherwise you will get the **ReferenceError: value not defined**.

>Don't overuse the optional chaining - we should use `?.` only where it’s ok that something doesn’t exist.

## Other variants
If we want to check some whether an object contains a function, we can use this construction as follows.

```javascript
let userAdmin = {
  admin() {
    alert("I am admin");
  }
};

let userGuest = {};

userAdmin.admin?.(); // I am admin

userGuest.admin?.(); // nothing happens (no such method)
```

If we want to access the properties of an object, we can use brackets as follows.

```javascript
let key = "firstName";

let user1 = {
  firstName: "John"
};

let user2 = null;

alert( user1?.[key] ); // John
alert( user2?.[key] ); // undefined
```

>We can use `?.` for safe reading and deleting, but not writing. This is because the expression evaluates to `undefined`.

```javascript
user?.name = "John"; // Error, doesn't work because it evaluates to: undefined = "John"
```

## Questions
1. What is optinal chaining in JavaScript?
2. How does it work?
3. When do we get an error using the optinal chaining?
4. What error do we get then?
5. When shouldn't we overuse the optional chaining?
6. How can we use the optional chaining with functions?
7. How can we use the optional chaining with brackets?
8. Can we use the optional chaining for reading and writing and deleting?
