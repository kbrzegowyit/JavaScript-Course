# Advanced working with functions: Recursion And Stack

This article is about recursion and stack in JavaScript.

## The execution contex and stack
The **execution context** is an internal data structure that contains details about the execution of the function.

When a function makes a nested call, the following happens:

* The current function is paused.
* The execution context associated with it is remembered in a special data structure called **execution context stack**.
* The nested call executes.
* After it ends, the old execution context is retrieved from the stack, and the outer function is resumed from where it stopped.

Recursion takes more memory than a loop, but is sometimes more convinient than a complex solution with loops.

## Recursive structures
### What is it
They are called *recursively-defined* data structures.

It's a structure that replicates itself in parts.

### Application
The approach can be useful in case of working with HTML or XML documents.

### Recursive function components
When a function calls itself, that's called a *recursion step*. The *basis* of recursion is function argument that make the task so simple that the function does not make another call.

## Linked List
It's recursively defined as an object with:
* value
* next - referencing to the next linked list element or `null` if that's the end.

### Pros and cons
| Pros    | Cons |
| -------- | ------- |
| we can easily rearrange an array (insert/delete)  | we can't access an element by its number, we need to go next **N** elements to get Nth element.    |

## Questions
1. What is execution context and stack?
2. What approach uses less memory?
3. What are recursively-defined DS?
4. What is recursive approach?
5. When can it be useful?
6. What is Linked List and its pros and cons?
7. Whta are the components of recursive function?