# Chapter 16

## Arrow functions, the basics

* There's a concise way to create functions called arrow functions.
* They look like `let func = (arg1, arg2, ..., argN) => expression;`
* This creates a function `func` that takes arguments `arg1` to `argN` and evaluates the expression on the right side with them.
* It's a shorter version of regular function expressions.

## Example: Simple Arrow Function

* `let sum = (a, b) => a + b;` is shorter for `let sum = function(a, b) { return a + b; };`
* It takes two arguments `a` and `b` and returns their sum.

## Single Argument

* If there's one argument, parentheses around it can be omitted: `let double = n => n * 2;`

## No Arguments

* If there are no arguments, parentheses are empty but must be present: `let sayHi = () => alert("Hello!");`

## Usage

* Arrow functions are used like function expressions.

## Multiline Arrow Functions

* For complex functions with multiple statements, use curly braces:

```javascript
let sum = (a, b) => {
  let result = a + b;
  return result;
};
```

* Curly braces require an explicit `return` statement.

## Summary

* Arrow functions are handy for simple actions, especially one-liners.
* They come in two flavors:
    * Without curly braces: `(...args) => expression` - right side is an expression, the function evaluates and returns the result. Parentheses can be omitted for a single argument.
    * With curly braces: `(...args) => { body }` - allows multiple statements inside but requires an explicit `return`.
