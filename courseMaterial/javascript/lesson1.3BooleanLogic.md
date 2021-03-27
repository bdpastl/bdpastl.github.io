## Boolean logic:
​    Boolean logic is how we can do what is called "control flow". We'll get to how to control how our programs work a little later, but first, we need to know how to properly show off our boolean values! For now we'll start with just with boolean values with true and false:

### AND:
	For something to work with AND, both sides around the `&&` need to be true:

```javascript true && true = true     // both are true, so this resolves to being true
        true && false = false   // only one is true, so we ultimately get false
        false && true = false   // only one is true, so we ultimately get false
        false && false = false  // both are false! So naturally, false.
```

### OR:
	For something to work with OR, we just need one of the sides to be true around the `||` operator!

```javascript true || true   = true   // both are true, so this is true!
        true || false  = true   // one side is true, so we still get true
        false || true  = true   // one side is true, so we still get true, even though the first was false
        false || false = false  // both are false! So, we ultimately get false here.
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
var oneIsLessThanFive = 1 < 5
console.log("it is " + oneIsLessThanFive + " that one is less than 5")

var oneIsGreaterThanFive = 1 > 5
console.log("it is " +oneIsGreaterThanFive + " that one is greater than 5")

var oneEqualsOne = 1 == 1
console.log("it is " + oneEqualsOne + " that one equals one!")

var fiveEqualsOne = 5 == 1
console.log("it is " + fiveEqualsOne + " that five equals one!")

var oneIsNotFive = 1 != 5
console.log("it is " + oneIsNotFive + " that one is not five")

var stringEquality = "Strings?" == "Strings?"
console.log("it is " + stringEquality + " that the two strings `Strings?` and `Strings?` are equal")

var stringNotEqual = "One String" == "Other String"
console.log("it is " + stringNotEqual + " that 'One string' is equal to 'Other string'")

var stringInequality = "One String" != "Other String"
console.log("it is " + stringInequality + " that 'One String' does not equal 'other'")

var sameStringInequality = "Strings?" != "Strings?"
console.log("it is " + sameStringInequality + " that 'Strings?' and 'Strings?' are not equal")
```


We can save the truthiness of those operators in variables like we just did, but what makes this REALLY powerful is that we can check the truthfulness of variables themselves! We'll take the exact same code as above, but now everything will be a variable!

```javascript
var one = 1
var five = 5

var oneIsLessThanFive = one < five
console.log("it is " + oneIsLessThanFive + " that one is less than five")

var oneIsGreaterThanFive = one > five
console.log("it is " +oneIsGreaterThanFive + " that one is greater than five")

var oneEqualsOne = one == one
console.log("it is " + oneEqualsOne + " that one equals one!")

var fiveEqualsOne = five == one
console.log("it is " + fiveEqualsOne + "that five equals one!")

var oneIsNotFive = one != five
console.log("it is " + oneIsNotFive + " that one is not five")

var stringQuestion = "Strings?"
var oneString = "One String"
var otherString = "Other String"

var stringEquality = stringQuestion == stringQuestion
console.log("it is " + stringEquality + " that the two strings `Strings?` and `Strings?` are equal")

var stringNotEqual = oneString == otherString
console.log("it is " + stringNotEqual + " that 'One string' is equal to 'Other string'")

var stringInequality = oneString != otherString
console.log("it is " + stringInequality + " that 'One String' does not equal 'other'")

var sameStringInequality = stringQuestion != stringQuestion
console.log("it is " + sameStringInequality + " that 'Strings?' and 'Strings?' are not equal")
```

By doing what we just did above, we can now create really powerful programs!

It is also possible to string the boolean logic together:

```javascript
var one = 1
var five = 5

var oneIsLessThanFive = one < five
console.log("it is " + oneIsLessThanFive + " that one is less than 5")

var oneIsGreaterThanFive = one > five
console.log("it is " +oneIsGreaterThanFive + " that one is greater than 5")

var eitherOR = oneIsLessThanFive || oneIsGreaterThanFive
var bothAnd = oneIsLessThanFive && oneIsGreaterThanFive

console.log("only one can be true, is it the 'eitherOr' or the 'bothAnd'? eitherOR: " + eitherOR + "     bothAnd:" + bothAnd)

// The above code for either or is the same as writing:
eitherOR = one < five || one > five
bothAnd = one < five && one > five

// either either or is true or both and is true, to say that we would write:
var ultimateOutcome = eitherOR || bothAnd


// the same way to write the above is:
ultimateOutcome = (one < five || one > five) || (one < five && one > five)

console.log('The ULTIMATE outcome: ' + ultimateOutcome)
```

Don't get too bogged down into trying to follow the logic. Just so long as you understand the basic's that's good enough (entire careers are spent in logic! We only need the basics).