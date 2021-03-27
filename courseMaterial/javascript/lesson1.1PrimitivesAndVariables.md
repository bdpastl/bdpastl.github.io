

# JAVASCRIPT

Javascript is one of the most popular programming languages today. It can be used for making scripts, interactive web applications, and web APIs. It can even be used to make games. The largest benefit of the language is its ability to run in web browsers. This course will be highly tailored to that aspect of the language, however, we will first need to start with the basics.

### console.log():

As we go through this course it will be useful to print out values to the console. We can do this with the built in `console.log()` function. Many of the exercises in this class will require you to log values to the console in order to confirm your results. This function can also be very useful when debugging your application.

To find out what's happening in our code, the very first function we'll look at is `console.log()`. This function takes whatever we pass into it, and logs it into the console (weird, huh?).

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

## Variables:

Syntax:

var variableName = someValue
const constantName = someUNCHANGINGValue

Take a look at the below code.

```javascript
// Numbers!
// Anything we could do with numbers we can also do with variables!
var a = 5
var b = 20
var c = a + b
var d = b / a

// Strings:
// Anything we could do with strings we can do with variables with strings in them!

var cityName = 'St. Louis '
var sportsTeam = 'Cardinals'

var sportsTeamInCity = cityName + sportsTeam


// You can do some neat things with strings:
var howLongIsSportsTeam = sportsTeam.length
var cityNameLength = cityName.length
```

A thing that variables can do is change! In javascript, they can change not only their value but also their type.

```javascript
var food = 'pizza'
food = 'cake'

food = 'the cake is a lie'

food = 5
```

Changing from string to number is completely fine in javascript! This can be extremely helpful, but it can also be very difficult if you're not paying attention (e.g. it would get really weird if you were calculating someone's bill on your site, and you tried to add 15 + 'Sweater').
