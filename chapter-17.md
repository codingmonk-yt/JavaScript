# Chapter 17

## JavaScript Specials

* **Code structure**
    * Statements are ended with semicolons `;`.
    * Automatic semicolon insertion happens in most cases, but it's recommended to use semicolons after every statement.
    * Semicolons are not required after code blocks `{...}` and loops.
    * Extra semicolons are ignored.
* **Strict mode**
    * Enabled with `"use strict";` at the beginning of a script or function.
    * Enforces stricter behavior and prevents some errors.
    * Modern features often enable strict mode implicitly.
* **Variables**
    * Can be declared with `let`, `const`, or `var` (old-fashioned).
    * Variable names can include letters, digits, `$`, `_`, and some non-Latin characters.
    * Variables are dynamically typed and can hold any data type.
    * There are 8 data types: `number`, `bigint`, `string`, `boolean`, `null`, `undefined`, `object`, and `symbol`.
    * `typeof` operator returns the data type of a value, except for `null` (wrongly shows as "object") and functions (shows as "function").
* **Interaction** (Browser environment)
    * `prompt(question, [default])`: Asks a question and returns the user's input or `null` if canceled.
    * `confirm(question)`: Asks a question with Yes/No options and returns `true` for Yes, `false` for No.
    * `alert(message)`: Displays a modal message box.
    * All these functions pause code execution until the user responds.
* **Operators**
    * Arithmetic: `+`, `-`, `*`, `/`, `%` (remainder), `**` (power). Binary `+` concatenates strings.
    * Assignment: `=`, combined assignments like `+=`.
    * Bitwise: Work on bits of integers (refer to documentation when needed).
    * Conditional: `cond ? resultA : resultB`.
    * Logical: `&&` (AND), `||` (OR), `!` (NOT). Short-circuit evaluation.
    * Nullish coalescing: `??`. Returns first defined value in a list.
    * Comparison: `==` (converts to number except for `null` and `undefined`), `===` (strict equality).
    * Other: Comma operator, etc.
* **Loops**
    * Three types: `while`, `do...while`, `for`.
    * `for` loop variable declared with `let` is only visible inside the loop.
    * `break` exits the loop, `continue` skips the current iteration. Labels can be used for nested loops.
* **Switch statement**
    * Alternative to multiple `if` statements.
    * Uses strict equality (`===`) for comparisons.
* **Functions**
    * Three ways to define: function declaration, function expression, arrow function.
    * Can have local variables and parameters with default values.
    * Always return a value (even `undefined` if no `return` statement).
 
