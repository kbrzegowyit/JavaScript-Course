# Objects the basics: Garbage Collection

This article is about objects Garbage Collection in JavaScript.

## Reachablity
This is the main concept of memory management in JavaScript.

If a value isn't reachable, it is deleted.

The algorithm that checks reachability starts from Globals Variables and
goes deeper, marking all references. Once it finishes, all objects that haven't been
marked are removed.
## Questions
1. What is reachablility and how does it work?