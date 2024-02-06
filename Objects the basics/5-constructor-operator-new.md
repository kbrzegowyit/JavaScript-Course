# Objects the basics: Constructor, operator "new"

This article is about the object constructor in JavaScript.

## Constructor function
It is a function that help us to implement reusable object creation code.

Any function can act as a constructor function, but to distinguish it from 
others we use a **capital letter first**.

```javascript
function User() {
    ...
}

const john = new User();
```

These things happen under the hood:
1. A new empty object is created and assigned to `this`.
2. The function body executes. Usually it modifies `this`, adds new properties to it.
3. The value of `this` is returned.

```javascript
function User(name) {
  // this = {};  (implicitly)

  // add properties to this
  this.name = name;
  this.isAdmin = false;

  // return this;  (implicitly)
}
```

## Return from constructor
Usually constructors don't have a `return` statements but we can use it.
When we return an object, the constructor will return the object, otherwise `this`.

## Methods in constructor
We can also add methods in constructor functions. We have to remember that the method will be added to every object created, so we will get a lot of duplicates.

## Questions
1. What does the constructor function is responsible for in JS?
2. What is the nameing conventions for constructor functions?
3. What does it happen under the hood during object creation?
4. What does it happen when we return something from the constructor?
5. What do we need to keep in mind when adding methods in constructor functions?
