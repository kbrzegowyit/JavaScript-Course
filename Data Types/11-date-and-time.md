# Data types: Date and time

This article is about date and time in JavaScript.

## Creation
1. `new Date()` create a Date object for the current date and time.
2. `new Date(milliseconds)` Create a Date object with the time equal to number of milliseconds (1/1000 of a second) passed after the Jan 1st of 1970 UTC+0.
3. `new Date(datestring)`
4. `new Date(year, month, date, hours, minutes, seconds, ms)`

> *Timestamp* An integer number representing the number of milliseconds that has passed since the beginning of 1970.

## Access date components
* `getFullYear` - get the year (4 digits)
* `getMonth` - get the month 0-11
* `getDate` - get the day of the month 1-31
* `getHours/getMinutes/getSeconds/getMilliseconds()`
* `getDay` - get the day of the week 0 (Sunday) - 6 (Saturday)
* `getTime` -  the timestamp for the date from the January 1st of 1970 UTC+0.
* `getTimezoneOffset` - the difference between UTC and the local time zone, in minutes. 

> Use getUTCMonth/Day/... for the time zone UTC+0.

## Autocorrection
It is a very handy feature of Date objects. We can set out-of-range values, and it will auto-adjust itself.

## Date to number, date difference
When a Date object is converted to number, it becomes the timestamp same as date.getTime().

The difference between dates is in ms.

## Date parse from a string
The string format should be: *YYYY-MM-DDTHH:mm:ss.sssZ*.

The optional 'Z' part denotes the time zone in the format +-hh:mm. A single letter Z would mean UTC+0.

## Questions
1. How can we create a new date?
2. What is the timestamp?
3. How can we create a new date?
4. How can we access the date components?
5. What is the autocorrection mechanism?
6. What is the unit of subtraction of dates?
7. How can we get a date from a string?