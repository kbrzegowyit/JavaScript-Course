# Data types: Strings

This article is about strings in JavaScript.

## Format
Internale format for strings is always UTF-16.

## Multiple lines
Advantage of using backticks is that they allow a string to span multiple lines.

## Accessing characters
`str[pos]` or `str.at(pos)`.  
In the second case, we can use negative values to access the values from the end.

We can also iterate over the characters of the string using `for..of`.

## Immutability
Strings are immutable, it is impossible to change a character.
The usual workaround is to create a whole new string and assign it to str instead of the old one.

## Searching for a substring
`str.indexOf(substr, pos)` - returns the position where the match was found or -1.

`str.lastIndexOf(substr, pos)` - the same as the previous one but starting from the end.

`str.includes(substr, pos)` - returns `true`/`false` depending the string contains the match or not.

`startsWith`/`endsWith` - do exactly what they say.

## Getting a substring
`str.slice(start [, end])` - returns the part of the string from start to (but not including) end.

`str.substring(start [, end])` - eturns the part of the string between start and end (not including end).

This is almost the same as slice, but it allows start to be greater than end (in this case it simply swaps start and end values).

`str.substr(start [, length])` - returns the part of the string from start, with the given length.

## Correct comparisons
ECMA-402 provides a special method to compare strings in different languages, following their rules.

The call str.localeCompare(str2) returns an integer indicating whether str is less, equal or greater than str2 according to the language rules:

- Returns a negative number if str is less than str2.
- Returns a positive number if str is greater than str2.
- Returns 0 if they are equivalent.

## Questions
1. What is internal format for strings?
2. Which type of quotes allows mulitple lines?
3. How can we access values of the string from the end?
4. How can we iterate over the characters of the string?
5. Can we change some part of a string by assigning a new value?
6. List functions that we can use to search for a substring.
7. What is the difference between `slice` and `substring`?
8. What method allows us to search for the substring using length?
9. How can we compere strings coming from different languages?