# Chapter 7

## Basic JavaScript Operators: Understanding the Math Behind Your Code

This guide breaks down essential JavaScript operators, focusing on both familiar math concepts and JavaScript-specific behaviors.

**Terminology:**

* **Operand:** The value an operator acts on. In `5 * 2`, `5` and `2` are the operands.
* **Unary Operator:** Operates on a single operand (e.g., `-x` negates `x`).
* **Binary Operator:** Operates on two operands (e.g., `5 + 2` adds `5` and `2`).

**Math Operators:**

* **Addition (`+`)**
  * Sums numbers (e.g., `5 + 2` equals `7`).
  * Concatenates strings (e.g., `"hello" + "world"` equals `"helloworld"`).
    * If one operand is a string, the other is converted to a string too (e.g., `'1' + 2` equals `"12"`).
* **Subtraction (`-`)**
  * Subtracts numbers (e.g., `8 - 3` equals `5`).
* **Multiplication (`*`)**
  * Multiplies numbers (e.g., `5 * 2` equals `10`).
* **Division (`/`)**
  * Divides numbers (e.g., `8 / 2` equals `4`).
* **Remainder (`%`)**
  * Calculates the remainder after integer division (e.g., `8 % 3` equals `2`).
* **Exponentiation (`**`)**
  * Raises a number to a power (e.g., `2 ** 3` equals `8`).
    * Works for non-integer powers as well (e.g., `4 ** (1/2)` equals `2` for square root).

**String Concatenation with `+`:**

* The `+` operator can combine strings.
* Example: `let message = "hello" + " " + "world";` creates a string "hello world".

**Unary Plus (`+`)**

* Converts a non-numeric value to a number (e.g., `+true` equals `1`).
* Useful when working with user input that might be strings.

**Operator Precedence:**

* Defines the order in which operations are evaluated.
* Higher precedence operators are evaluated first (e.g., `2 * 2 + 1` equals `5` because multiplication happens before addition).
* Parentheses can override precedence (e.g., `(2 + 2) * 1` equals `4`).

**Assignment (`=`)**

* Assigns a value to a variable (e.g., `let x = 5`).
* The assignment itself has a low precedence and is evaluated last.
* The assignment operator also returns a value (the assigned value).

**Chained Assignments (`=` with multiple variables):**

* Assigns the same value to multiple variables (e.g., `let a = b = c = 2 + 2`).
* Evaluation happens from right to left.

**Modify-in-place Operators (`+=`, `-=`, etc.)**

* Shorthand for operations that modify a variable and then reassign it (e.g., `x += 5` is the same as `x = x + 5`).

**Increment (`++`) and Decrement (`--`)**

* Increase or decrease a variable by 1 (e.g., `x++` increments `x`).
* Can be used in prefix (`++x`) or postfix (`x++`) form.
* Prefix returns the new value, postfix returns the old value.

**Bitwise Operators (`&`, `|`, etc.)**

* Operate on numbers at the bit level (advanced topic, not covered here).

**Comma Operator (`,`)**

* Evaluates multiple expressions, but only returns the last one's value (e.g., `let sum = (1 + 2, 3 + 4);` sets `sum` to `7`).
* Rarely used, but can be seen in complex code.


**Key Points:**

* Understand operator precedence to write predictable code.
* Use unary plus for converting non-numbers to numbers.
* Be mindful of string concatenation with `+`.
* Consider readability when using chaining or comma operators.

By mastering these operators, you'll have a solid foundation for performing calculations and manipulating data in JavaScript.
