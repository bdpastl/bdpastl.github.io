# JAVASCRIPT

Javascript is one of the most popular programming languages today. It can be used for making scripts, interactive web applications, and web APIs. It can even be used to make games. The largest benefit of the language is its ability to run in web browsers. This course will be highly tailored to that aspect of the language, however, we will first need to start with the basics.

## Printing Values to the Console:

As we go through this course it will be useful to print out values to the console. We can do this with the built in `console.log()` function. Many of the exercises in this class will require that you log values to the console in order to confirm your results. This function can also be very useful when debugging your application.

## Primitives:
Javascript is very different from HTML/CSS, it works completely differently, but don't worry! Everything you need to know will be here!

To start out, primitive types are:

**Integers:** 1,2,3,4,5,ect.
**Floating points:** 2.3, 5.212, 3.14, etc.
**Strings:** "Hello! I am a string!", "I'm also a string!"
**Booleans:** true, false // just true or false!
**Null/Undefined:** null, undefined // You'll see these a lot, basically if something doesn't exist and we try to access it, we'll get these back in return!

### Numbers:
In the codehs sandbox, try writing some numbers. We can do any type of math with javascript that we could do with anything else! Here is some basic math:

```javascript
4 + 20     // Addition
41.3 - 300   // Subtraction
10 / 3     // Division
15 * 3     // Multiplication
10 % 3     // Modulus (ONLY WORKS WITH WHOLE NUMBERS)
```

You're probably very familiar with all of these basic math operators, but you may not have seen modulus yet. Modulus is just a remainder, so in integer division, 10 divided by 3 gives us 3 remainder 1. When we use modulus, 10 % 3 = 1. 10 % 2 doesn't have any remainder, so we get: 10 % 2 = 0.

As a quick note, all of these operators still follow the order of operations*.

### Strings:

```javascript
"Hello World"
'Hello World'

//You can't do "Hello'
// Quotes must match!
// If you wanted to use an apostrophe, use double quotes, or you want to use double quotes in a string:
"I don't ever want to stop coding"
'He said "I like turtles" a lot'

//concatenation:
'Hello ' + 'World'
```

Writing out math and strings is great and all, but that's not what makes code so powerful. We need a way to save those numbers, letters, booleans, etc. That's where variables come in.

## Variables

In programming, it's commonplace to create 'references' to these values in memory. This is the concept of '**instantiating a variable**' (`const`, `let`) and '**assigning a value to a variable**' (`=`). Whenever a _value_ in memory no longer has a _reference_ to it, the JS _garbage collector_ comes along to completely remove it from memory.

### **`const` vs. `let`**

Two keywords allow us to create a variable: `const` and `let`.
If we create a variable with `const`, the variable _cannot_ be reassigned with a new value. However, if we create a variable with `let`, the variable _can_ be mutated(changed) and/or reassigned.

```javascript
const name;
let favoriteSong;
```

> **NOTE**: You may have seen JS variables created with the keyword `var`. The keyword `var` is used in pre-ES6 JavaScript to create a variable. Although there is a key difference, you can think of `var` as simply being an alternative for `let` for the time being.


### **Assignment Operator: `=`**

The assignment operator (`=`) is used to link variables to the values they reference. The assignment operator works right to left, for example:

```javascript
let age = 29;
```

In this example, we are creating a _value_ (`29`) on the right and a _variable_ (`age`)on the left. The _assignment operator_ takes the value on the _right_ and assigns it to the variable on the _left_.


### The `typeof` Operator

You can check/get the type of data for any _primitive_ by using the `typeof` _operator_ like so:

```javascript
typeof "Motorbike";
typeof 550;
typeof false;
```

The `typeof` operator returns the data type in a _string_ (i.e. "string", "number", "boolean")


> **TIP**: This can be handy when trying to debug your code. You can `log()` the `typeof` of some variable to make sure that the data type it references is what you expect.


### **Dynamic Typing**

As a language, JavaScript is **dynamically typed** (or _loosely typed_) - we don't have to explicitly declare what type of data will be stored in a variable, and we can replace data of one type with any other type of data.


Changing from string to number is completely fine in javascript! This can be extremely helpful, but it can also be very difficult if you're not paying attention (e.g. it would get really weird if you were calculating someone's bill on your site, and you tried to add 15 + 'Sweater').

## Type Conversions

### Strings

Both `booleans` and `numbers` can be converted to a string using the `String()` function:

```javascript
  let boolVal = true;
  let boolStr = String(boolVal); // boolStr now stores the value "true"

  let numVal = 123;
  let numStr = String(numVal); // boolStr now stores the value "123"
```

Additionally, variables of type `boolean` and `number` also have a method called `toString():

```javascript
  let boolVal = true;
  let boolStr = boolVal.toString(); // boolStr now stores the value "true"

  let numVal = 123;
  let numStr = numVal.toString(); // boolStr now stores the value "123"
```

### Booleans

The function `Boolean` can be used to convert values into the type `boolean`:

```javascript
  Boolean(""); // evaluates to false
  Boolean("true"); // evaluates to true
  Boolean("false"); // evaluates to true
  Boolean(0); // evaluates to false
  Boolean(1); // evaluates to true
```

### Numbers

The function `Number` can be used to convert values into the type `number`:

```javascript
  Number("123"); // evaluates to the number 123
  Number(""); // evaluates to the number 0
  Number("0"); // evaluates to the number 0
  Number("blob"); // evaluates to the number NaN
  Number(false); // evaluates to the number 0
  Number(true); // evaluates to the number 1
```