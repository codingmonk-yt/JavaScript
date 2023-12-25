# Chapter 1: JavaScript Variables

Variables are what makes up most of javascript. These Variables make up things from numbers to objects, which are all over javascript to make one's life easier.

## Section 1.1: Defining a Variable

```js
let myVariable = "This is a variable!";
```

**This is an example of defining variables. This variable is called a "string" because it has ASCII characters (A-Z, 0-9,!@#$, etc.)**

## Section 1.2: Using a Variable

```js
let number1 = 5;
number1 = 3;
```

> Here, we defined a number called "number1" which was equal to 5. However, on the second line, we changed the value to 3. To show the value of a variable, we log it to the console or use window.alert():

```js
console.log(number1); // 3
window.alert(number1); // 3
```

To add, subtract, multiply, divide, etc., we do like so:

```js
number1 = number1 + 5; // 3 + 5 = 8
number1 = number1 - 6; // 8 - 6 = 2
let number2 = number1 * 10; // 2 (times) 10 = 20
let number3 = number2 / number1; // 20 (divided by) 2 = 10;
```

> We can also add strings which will concatenate them, or put them together. For example:

```js
let myString = "I am a " + "string!"; // "I am a string!"
```


## Section 1.3: Types of Variables

```js
let myInteger = 12; // 32-bit number (from -2,147,483,648 to 2,147,483,647)`
let myLong = 9310141419482; // 64-bit number (from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807)
let myFloat = 5.5; // 32-bit floating-point number (decimal)
let myDouble = 9310141419482.22; // 64-bit floating-point number
let myBoolean = true; // 1-bit true/false (0 or 1) let myBoolean2 = false;
let myNotANumber = NaN;
let NaN_Example = 0/0; // NaN: Division by Zero is not possible
let notDefined; // undefined: we didn't define it to anything yet window.alert(aRandomVariable); // undefined
let myNull = null; // null // etc...
```

## Section 1.4: Arrays and Objects

```js
let myArray = []; // empty array
```

An array is a set of variables. For example:

```js

let favoriteFruits = ["apple", "orange", "strawberry"];
let carsInParkingLot = ["Toyota", "Ferrari", "Lexus"];
let employees = ["Billy", "Bob", "Joe"];
let primeNumbers = [2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31];
let randomVariables = [2, "any type works", undefined, null, true, 2.51];
myArray = ["zero", "one", "two"];
window.alert(myArray[0]); // 0 is the first element of an array
                           // in this case, the value would be "zero"
myArray = ["John Doe", "Billy"];
elementNumber = 1;
window.alert(myArray[elementNumber]); // Billy

```

An object is a group of values; unlike arrays, we can do something better than them:

```js
myObject = {};
john = {firstname: "John", lastname: "Doe", fullname: "John Doe"};
billy = {
firstname: "Billy", lastname: undefined, fullname: "Billy"
};
window.alert(john.fullname); // John Doe window.alert(billy.firstname); // Billy
```

Rather than making an array ["John Doe", "Billy"] and calling myArray[0], we can just call john.fullname and billy.fullname.





