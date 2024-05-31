# Chapter 4

## Data Types in JavaScript

JavaScript has several built-in data types to store different kinds of information. Here's a breakdown of the essential ones:

**Numbers:**

* Represent both whole numbers (integers) and decimals (floating-point numbers).
* Used for mathematical operations like addition, subtraction, multiplication, and division.
* Examples: `42`, `3.14159`, `-100`.

**Strings:**

* Represent sequences of characters, enclosed in quotes (single or double quotes, or backticks).
* Backticks allow embedding variables or expressions within the string using `${...}`.
* Examples: `"Hello, world!"`, `'JavaScript'`, ``This is a string with ${variable}``.

**Booleans:**

* Represent logical values: `true` or `false`.
* Used for conditional statements and comparisons.
* Examples: `true` (meaning yes or correct), `false` (meaning no or incorrect).

**null:**

* A special value that signifies "no value" or "absence of a value."
* Used to indicate that a variable has no assigned data.
* Example: `let x = null;`.

**undefined:**

* Another special value that indicates a variable has been declared but not assigned a value.
* Not the same as `null`.
* Example: `let y; // y is undefined`.

**Objects:**

* Complex data structures used to store collections of key-value pairs.
* We'll explore objects in a dedicated chapter later.

**Symbols (advanced):**

* Used to create unique identifiers for objects.
* We'll touch on symbols briefly here but cover them in more detail later.

**typeof Operator:**

* Returns the data type of a value.
* Useful for checking the type of data you're working with.
* Example: `typeof 42` returns `"number"`.

**Key Points:**

* JavaScript is dynamically typed, meaning variables don't have a fixed data type.
* You can store different data types in the same variable at different times.
* Choosing the right data type helps make your code more readable and efficient.

**In summary:**

JavaScript provides various data types to handle different kinds of information. Understanding these types is essential for writing effective JavaScript code. 
