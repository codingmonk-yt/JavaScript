# Chapter 8

## JavaScript Comparisons: Understanding How Values Are Compared

JavaScript provides comparison operators to check if values are equal, greater than, less than, and so on. This guide explains how comparisons work in JavaScript, including some interesting quirks.

**Comparison Operators:**

* **Greater than (`>`)**
  * Checks if the left operand is greater than the right operand.
  * Example: `2 > 1` evaluates to `true`.
* **Less than (`<`)**
  * Checks if the left operand is less than the right operand.
  * Example: `1 < 2` evaluates to `true`.
* **Greater than or equal to (`>=`)**
  * Checks if the left operand is greater than or equal to the right operand.
  * Example: `3 >= 2` evaluates to `true`.
* **Less than or equal to (`<=`)**
  * Checks if the left operand is less than or equal to the right operand.
  * Example: `1 <= 1` evaluates to `true`.
* **Equal (`==`)** (Double equals sign)
  * Checks if the left operand is equal to the right operand, but may perform type conversion.
  * Example: `'2' == 2` evaluates to `true` (string '2' is converted to number 2).
* **Strict equal (`===`)** (Triple equals sign)
  * Checks if the left operand is strictly equal to the right operand, without type conversion.
  * Example: `'2' === 2` evaluates to `false` (string and number are not the same).
* **Not equal (`!=`)**
  * Checks if the left operand is not equal to the right operand.
  * Example: `3 != 2` evaluates to `true`.
* **Strict not equal (`!==`)** (Double exclamation mark)
  * Checks if the left operand is strictly not equal to the right operand, without type conversion.
  * Example: `1 !== '1'` evaluates to `true` (number and string are not the same type).

**Result of Comparisons:**

Comparisons always return a boolean value:

* `true` - Represents "yes", "correct", or "the truth".
* `false` - Represents "no", "wrong", or "not the truth".

**String Comparison:**

JavaScript compares strings character-by-character, similar to dictionary order. The comparison stops when a difference is found or both strings end.

* Example: `"apple" > "banana"` evaluates to `false` because "b" comes before "p" in the alphabet.

**Type Coercion with `==`:**

When comparing different types with `==`, JavaScript tries to convert one value to the other type. This can lead to unexpected results.

* Example: `0 == false` evaluates to `true` because 0 (falsy) is converted to `false`.

**Strict Equality (`===`)**

Use `===` for strict comparisons that avoid type conversion.

* Example: `0 === false` evaluates to `false` because the types are different.

**Null and Undefined:**

* `null` represents the intentional absence of a value.
* `undefined` indicates a variable has not been assigned a value.

These values have special comparison behavior:

* `null == undefined` evaluates to `true` (special case).
* `null === undefined` evaluates to `false` (strictly different types).
* Comparisons with other values (like `null > 0`) involve type conversion, leading to potentially surprising results.

**Avoiding Comparison Issues:**

* Be cautious when comparing with `null` or `undefined`.
* If a variable might be `null` or `undefined`, check for them explicitly before comparisons.
* Use strict comparisons (`===` and `!==`) when type safety is crucial.

**Summary:**

* Comparison operators return booleans (`true` or `false`).
* Understand string comparison order and type coercion with `==`.
* Use strict comparisons (`===` and `!==`) for reliable equality checks.
* Be mindful of `null` and `undefined` comparisons.

By following these guidelines, you can write clear and predictable JavaScript code that compares values accurately.
