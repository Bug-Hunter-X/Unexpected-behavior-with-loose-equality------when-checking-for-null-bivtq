# JavaScript Loose Equality Bug

This repository demonstrates a common JavaScript bug involving the loose equality operator (==) and null checks.  The loose equality operator does type coercion, leading to unexpected behavior when comparing null with 0. This can cause errors when handling function parameters.

## Bug Description
The provided `foo` function checks if parameters `a` and `b` are null using the `==` operator.  This is problematic because `0 == null` evaluates to `false`, even though 0 is not equivalent to null.

## How to Reproduce
Clone this repository and run `bug.js`. You will see that it throws an error when you pass in the number 0 as an argument instead of explicitly checking for null.

## Solution
The solution involves using strict equality (===) to reliably check for null.  Strict equality avoids type coercion, providing a more accurate null check.  Refer to the `bugSolution.js` file for the corrected code.