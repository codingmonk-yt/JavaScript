# Chapter 6

## Type Conversion in JavaScript

JavaScript automatically converts values between different types in certain situations. However, you can also explicitly convert values using built-in functions. Here's a breakdown of the most common conversions:

**1. String Conversion**

* Happens whenever a value needs to be displayed as text (e.g., in `alert()`, printing to the console).
* You can also use the `String(value)` function to convert a value to a string.
* Examples:

```javascript
let num = 123;
alert(typeof num); // number

let str = String(num); // str becomes "123" (string)
alert(typeof str); // string

alert(Boolean("hello")); // true (string converted to "true")
alert(Boolean(0)); // false (number converted to "false")
```

**2. Numeric Conversion**

* Happens automatically in mathematical operations (e.g., `+`, `-`, `*`, `/`).
* You can use the `Number(value)` function to explicitly convert a value to a number.
* Conversion rules:

  * `undefined` becomes `NaN` (Not a Number).
  * `null` becomes `0`.
  * `true` and `false` become `1` and `0`, respectively.
  * Strings are converted according to the following logic:
    * Leading and trailing whitespaces are ignored.
    * If the remaining string is empty, the result is `0`.
    * Otherwise, the number is parsed from the string.
    * If parsing fails (invalid number format), the result is `NaN`.

* Examples:

```javascript
let str = "345";
alert(typeof str); // string

let num = Number(str); // num becomes 345 (number)
alert(typeof num); // number

alert(Number("hello")); // NaN (invalid number format)
alert(Number(true)); // 1
alert(Number(null)); // 0
```

**3. Boolean Conversion**

* Happens in logical operations (e.g., `&&`, `||`, `!`).
* You can use the `Boolean(value)` function to explicitly convert a value to a boolean.
* Conversion rules:

  * `0`, `""` (empty string), `null`, `undefined`, and `NaN` become `false`.
  * Any other value becomes `true`.

* Examples:

```javascript
alert(Boolean(10)); // true
alert(Boolean(0)); // false
alert(Boolean("")); // false
alert(Boolean(" ")); // true (any non-empty string is true)
alert(Boolean(null)); // false
```

**Important points:**

* Remember that `undefined` becomes `NaN` during numeric conversion, not `0`.
* An empty string (`""`) and a string with only whitespaces (`" "`) are considered `true` in boolean conversion.
* Object conversion will be covered later in the chapter `Object to primitive conversion`.

**In summary:**

Understanding type conversion is essential for working with different data types in JavaScript. These conversions happen implicitly or explicitly, and knowing the rules helps you write predictable and efficient code.
