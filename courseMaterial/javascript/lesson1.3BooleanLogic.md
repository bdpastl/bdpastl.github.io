## Boolean logic:
​Boolean logic is how we can do what is called "control flow". We'll get to controlling the flow of our programs work a little later, but first, we need to know how to properly show off our boolean values! For now we'll start with just with boolean values with true and false:

### AND:
For something to work with AND, both sides around the `&&` need to be true:

```javascript
	true && true // evaluates to true - both are true, so this resolves to being true
	true && false // evaluates to false - only one is true, so we ultimately get false
	false && true // evaluates to false - only one is true, so we ultimately get false
	false && false // evaluates to false - both are false! So naturally, false.
```

### OR:
	For something to work with OR, we just need one of the sides to be true around the `||` operator!

```javascript
	true || true // evaluates to true - both are true, so this is true!
	true || false // evaluates to true - one side is true, so we still get true
	false || true // evaluates to true - one side is true, so we still get true, even though the first was false
	false || false // evaluates to false - both are false! So, we ultimately get false here.
```

The above are the basis of how we control the flow of our programs. This may not make sense now because well, true is true, that doesn't really tell us anything. Let's start looking at conditions:


## Conditions:

When checking conditions, we can use basic greater than, less than, equal to, or not equal to in order to check what's going on with our program. These may not make the most sense at the moment (particuarly the checking for equality, but it'll make sense the more you use them!):

### Less than / greater than:
	1 < 5 is true because 1 is less than 5
	5 < 2 is false because 5 is more than 2
	2 > 5 is also false, because again, 5 is more than 2.


### Equals / Not Equals:

Unlike less than and greater than, we need to do something different with checking for equality. This is because when we use 1 equals sign, in javascript that's the 'assignment' operator which we saw above in the variables section. To check for equality, we need to use `==`. Likewise, to check for things not being equal, we need to use `!=`:


	1 == 1 is true because one does equal one.
	1 == 5 is false because 5 and 1 are completely differet numbers.
	1 != 5 is true because 1 is not equal to 5!
	1 != 1 is false because 1 is equal to 1 (And by using the != operator, we're trying to see if they're not equal)

You can also check strings for equality!
``` "Strings?" == "Strings?" is true because the two strings are the exact same!
"One String" == "Other String" is false because the strings don't say the same thing!
"One String" != "Other string" is true because the strings don't equal each other!
"Strings?" != "Strings?" is false because they are the same string, and we're checking for inequality!
```


Hopefully those make a little bit of sense, but what's great is that we don't have to use 'literals' (that is, non-variables) to check for some sort of boolean condition:

```javascript
let oneIsLessThanFive = 1 < 5;
console.log("it is " + oneIsLessThanFive + " that one is less than 5");

let oneIsGreaterThanFive = 1 > 5;
console.log("it is " +oneIsGreaterThanFive + " that one is greater than 5");

let oneEqualsOne = 1 == 1;
console.log("it is " + oneEqualsOne + " that one equals one!");

let fiveEqualsOne = 5 == 1;
console.log("it is " + fiveEqualsOne + " that five equals one!");

let oneIsNotFive = 1 != 5;
console.log("it is " + oneIsNotFive + " that one is not five");

let stringEquality = "Strings?" == "Strings?";
console.log("it is " + stringEquality + " that the two strings `Strings?` and `Strings?` are equal");

let stringNotEqual = "One String" == "Other String";
console.log("it is " + stringNotEqual + " that 'One string' is equal to 'Other string'");

let stringInequality = "One String" != "Other String";
console.log("it is " + stringInequality + " that 'One String' does not equal 'other'");

let sameStringInequality = "Strings?" != "Strings?";
console.log("it is " + sameStringInequality + " that 'Strings?' and 'Strings?' are not equal");
```


We can save the truthiness of those operators in variables like we just did, but what makes this REALLY powerful is that we can check the truthfulness of variables themselves! We'll take the exact same code as above, but now everything will be a variable!

```javascript
let one = 1;
let five = 5;

let oneIsLessThanFive = one < five;
console.log("it is " + oneIsLessThanFive + " that one is less than five");

let oneIsGreaterThanFive = one > five;
console.log("it is " +oneIsGreaterThanFive + " that one is greater than five");

let oneEqualsOne = one == one;
console.log("it is " + oneEqualsOne + " that one equals one!");

let fiveEqualsOne = five == one;
console.log("it is " + fiveEqualsOne + "that five equals one!");

let oneIsNotFive = one != five;
console.log("it is " + oneIsNotFive + " that one is not five");

let stringQuestion = "Strings?";
let oneString = "One String";
let otherString = "Other String";

let stringEquality = stringQuestion == stringQuestion;
console.log("it is " + stringEquality + " that the two strings `Strings?` and `Strings?` are equal");

let stringNotEqual = oneString == otherString;
console.log("it is " + stringNotEqual + " that 'One string' is equal to 'Other string'");

let stringInequality = oneString != otherString;
console.log("it is " + stringInequality + " that 'One String' does not equal 'other'");

let sameStringInequality = stringQuestion != stringQuestion;
console.log("it is " + sameStringInequality + " that 'Strings?' and 'Strings?' are not equal");
```

By doing what we just did above, we can now create really powerful programs!

It is also possible to string the boolean logic together:

```javascript
let one = 1;
let five = 5;

let oneIsLessThanFive = one < five;
console.log("it is " + oneIsLessThanFive + " that one is less than 5");

let oneIsGreaterThanFive = one > five;
console.log("it is " +oneIsGreaterThanFive + " that one is greater than 5");

let eitherOR = oneIsLessThanFive || oneIsGreaterThanFive;
let bothAnd = oneIsLessThanFive && oneIsGreaterThanFive;

console.log("only one can be true, is it the 'eitherOr' or the 'bothAnd'? eitherOR: " + eitherOR + "     bothAnd:" + bothAnd);

// The above code for either or is the same as writing:
eitherOR = one < five || one > five;
bothAnd = one < five && one > five;

// either either or is true or both and is true, to say that we would write:
let ultimateOutcome = eitherOR || bothAnd;


// the same way to write the above is:
ultimateOutcome = (one < five || one > five) || (one < five && one > five);

console.log('The ULTIMATE outcome: ' + ultimateOutcome);
```

Don't get too bogged down into trying to follow the logic. Just so long as you understand the basic's that's good enough (entire careers are spent in logic! We only need the basics).

### Triple Equals
The `===` operator is very similar to the `==` operator. The one key difference is that `===` checks the type of each operand.

For example:

```javascript
12 == "12" // evaluates to true
12 === "12" // evaluates to false
```

This distinction exists because of a little thing in Javascript called 'type coercion' but we won't get into that. In general, stick to using `===` in your programs to avoid bugs.