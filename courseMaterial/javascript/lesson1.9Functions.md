### Functions:

Functions are the most powerful part of any language! We've been using functions this entire time already, but we just didn't realize it. `console.log` is a function provided by javascript that lets us print to the console!

What makes functions so powerful is that they  let us split our code up into small, reusable modules! They also let us keep our code really clean! Once our projects start getting really big, it's easy to lose place of where you put a certain chunk of code!

There are many ways to write a function in javascript, but the way we're goin to write functions is like:

```javascript
const functionName = function() {
  // function body
}
```

**Note**: you first probably noticed that we said `const`. That's because if you make your function a `var` you might accidentally write over it (because you can reassign variables to a new value)!

We called our function `functionName` and then assigned it the the value of `function(){  }`. What we just did was create an empty function. By using the `function()` keyword, we're saying that whenver we call this later (like when we call `console.log`) we'll get to execute whatever code we put in the body! Let's give it a quick go:

```javascript
const pizzaQuestion = function() {
  console.log('Do you like pizza?');
  console.log('OF COURSE YOU DO BECAUSE PIZZA IS AMAZING!')
};

pizzaQuestion()    // this calls the function
```



Now, when you have a function declared, notice that none of those console logs show up in our console. That's because the code can only be executed when we invoke our function! That's done by calling our function like `pizzaQuestion()`.

**Note:** You absolutely need to write the `()` after your function name to call it. Otherwise, your console will just tell you that what you entered was a function.



#### Parameters:

One thing that makes functions really useful is that they can take in parameters! A parameter is a special value that we "pass in" to our function:

```javascript
const functionName = function(parameter1, parameter2) {
	console.log('Parameter 1 is ', parameter1)
  console.log('Parameter 2 is ', parameter2)
}

// call it with the name:
functionName('WHAT?', 'HUZZAH')
```

By passing variables into our functions, we can work with the data we pass and do some pretty cool things!

```javascript
const doMath = function(number1, number2) {
	var newNumber = number1 + number2
  console.log('The sum of ' + number1 + ' and ' + number2 + ' is ' + newNumber)
}

doMath(11, 22) // this calls the function by passing in numbers to doMath!
```


You don't have to pass in literal numbers and strings to functions! You can also pass in variables!

```Javascript
const doMath = function(number1, number2) {
	var newNumber = number1 + number2
  console.log('The sum of ' + number1 + ' and ' + number2 + ' is ' + newNumber)
}

var eleven = 11
var twentyTwo = 22

doMath(eleven, twentyTwo) // this calls the function by passing in numbers to doMath!
```


#### Return Values:

Functions would be great with just the ability to store code and take in parameters, but what makes functions so powerful is that they can also return values! Let's try one with no parameters, and go back to pizza. When you return a value from a function, you need to have a variable catch it!:

```javascript
const pizzaQuestion = function() {
  console.log('Do you like pizza?');
  console.log('OF COURSE YOU DO BECAUSE PIZZA IS AMAZING!')
  return "You're getting a cheese pizza!"
};

var pizzaReturn = pizzaQuestion()    // pizza question returned a string to the var
console.log(pizzaReturn) 						 // print what pizzaQuestion returned!
```



When `pizzaQuestion` returned the string `"You're getting a cheese pizza"`, it stored that value in `pizzaReturn`.



To make our functions more dynamic, we can actually pass data into them with the paramaters, and then return some data based off of what we passed in! Let's go back to our `doMath` function:

```javascript
const doMath = function(number1, number2) {
	var newNumber = number1 + number2
  console.log('The sum of ' + number1 + ' and ' + number2 + ' is ' + newNumber)

  return newNumber
}

var eleven = 11
var twentyTwo = 22

var mathReturn = doMath(eleven, twentyTwo)  // return newNumber and stores it in mathReturn
```

In the above function, we not only passed data in, we also manipulated it to get a new value, and returned that data in a new variable!  Passing data back and forth is exactly how incredibly responsive websites are built!

