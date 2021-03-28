### Objects:

An object is another way to store data. Unlike arrays, however, objects aren't really lists. Objects are ways to store data of different kinds in one spot. Objects have what are called `key : value` pairs. You can access the value inside of the object by calling `object.key`.

 Think of an object as a variable that has a bunch of other, named variables inside of it. An object looks like:

```javascript
var myObject = {
  variableString: 'Something goes here',
  variableString2: 'Something else goes here',
  variableNumber: 14,
  variableNumber2: 3.14
}
```

To access the values inside of `myObject`,  you need to use the `key`. You can do that by typing something like `myObject.variableString` and that would return the sentence `'Something goes here'`. Let's try printing the elements of our object:

```Javascript
var myObject = {
  variableString: 'Something goes here',
  variableString2: 'Something else goes here',
  variableNumber: 14,
  variableNumber2: 3.14
}


console.log('The insides of myObject are: ')
console.log(myObject.variableString)
console.log(myObject.variableString2)
console.log(myObject.variableNumber)
console.log(myObject.variableNumber2)
```



Any object is declared just like any other variable, but instead of directly assigning a value to it, you use curly braces `{ }` and then start declaring your keys value pairs! One thing to note is that your keys don't have to be named boring names like `variableNumber` or `variableString`. Keys can have any name. You can also :

```Javascript
var myDetails = {
  name: 'My Name',
  birthday: 'MyBirthday',
  favoriteFood: 'Pizza',
  moneys: 1000000000,
  socialSecurityNumber: 123456789
}
```



Let's say for some reason, you decided that your favorite food wasn't pizza, and instead you wanted to change it to broccoli for some reason. You could change that by just reassigning it like you do with a variable!

```javascript
var myDetails = {
  name: 'My Name',
  birthday: 'MyBirthday',
  favoriteFood: 'Pizza',
  moneys: 1000000000,
  socialSecurityNumber: 123456789
}

// for some reason you don't like pizza anymore:
myDetails.favoriteFood = 'broccoli'

console.log('My new details are: ')
console.log(myDetails.name)
console.log(myDetails.birthday)
console.log(myDetails.favoriteFood)
console.log(myDetails.moneys)
console.log(myDetails.socialSecurityNumber)


```

### Mixing and Matching!

The more you learn to code, the more you'll realize that you can mix and match everything we've done so far:

#### Objects with Arrays:

Just like our objects can store any data we want, we can also have them store arrays too! Suppose we took what we did above (reminder that we had changed our favorite food to broccoli):

```Javascript
var myDetails = {
  name: 'My Name',
  birthday: 'MyBirthday',
  favoriteFood: 'broccoli',
  moneys: 1000000000,
  socialSecurityNumber: 123456789
}
```

Instead of one favorite food, we wanted to have a whole list (why limit ourselves to just one!):

```javascript
var myDetails = {
  name: 'My Name',
  birthday: 'MyBirthday',
  favoriteFood: ['pizza', 'broccoli', 'ice cream', 'tacos', 'cabbage', 'brussels sprouts'],
  moneys: 1000000000,
  socialSecurityNumber: 123456789
}
```



Now we can have a whole list of foods that we love! To access our foods, we just need to use the same notation we used with objects AND mix that with the notation we used for arrays:

```javascript
var myDetails = {
  name: 'My Name',
  birthday: 'MyBirthday',
  favoriteFood: ['pizza', 'broccoli', 'ice cream', 'tacos', 'cabbage', 'brussels sprouts'],
  moneys: 1000000000,
  socialSecurityNumber: 123456789
}

console.log('My first favorite food is: ', myDetails.favoriteFood[0])
console.log('My second most favorite food is: ', myDetails.favoriteFood[1])
console.log('My third most favorite food is: ', myDetails.favoriteFood[2])
console.log('My fourth most favorite food is: ', myDetails.favoriteFood[3])
console.log('My fifth most favorite food is: ', myDetails.favoriteFood[4])
console.log('My sixth most favorite food is: ', myDetails.favoriteFood[5])
```



That all looks fine and dandy, but wouldn't it be easier to use a loop? Maybe a for loop?

```javascript
var myDetails = {
  name: 'My Name',
  birthday: 'MyBirthday',
  favoriteFood: ['pizza', 'broccoli', 'ice cream', 'tacos', 'cabbage', 'brussels sprouts'],
  moneys: 1000000000,
  socialSecurityNumber: 123456789
}

console.log('My favorite foods ranked in order are: ' )

for(var i = 0; i < 6; i++ ){
	console.log(i + '. ' + myDetails.favoriteFood[i]) //here we're using i to count from 0->5
}
```



Remember how arrays all have the `.length` property? We can use that in our for loop here:

```javascript
var myDetails = {
  name: 'My Name',
  birthday: 'MyBirthday',
  favoriteFood: ['pizza', 'broccoli', 'ice cream', 'tacos', 'cabbage', 'brussels sprouts'],
  moneys: 1000000000,
  socialSecurityNumber: 123456789
}

console.log('My favorite foods ranked in order are: ' )

for(var i = 0; i < myDetails.favoriteFood.length; i++ ){    // use the .length!
	console.log(i + '. ' + myDetails.favoriteFood[i])
}
```

#### Arrays of Objects:

To create an array of objects, instead of using single 'primitive' types, we can use objects instead. Let's assume we're running a pizza restaurant and we need to send a list of pizza orders to our kitchen so they fire those pizzas up!

```javascript
var pizzaList =  [    		// open the array with the square brackets
  {
    sizeInches: 12,
    sauce: 'Tomato',
    style: 'Meat Lovers',
  },
  {
    sizeInches: 8,
    sauce: 'Alfredo',
    style: 'Cheese',
  },
  {
    sizeInches: 12,
    sauce: 'Tomato',
    style: 'Vegetarian',
  }													// There's no comma at the end because it's the last element!
]

```



We'll need a way to print those pizzas out. We've seen objects with arrays in them, but how do we access they keys of objects inside of an array? The way we do that is like:

```javascript
listName[indexPosition].key
```



It may look weird now, but you'll get used to it. Let's try by printing our pizza list in a loop:

```javascript
var pizzaList =  [
  {
    sizeInches: 12,
    sauce: 'Tomato',
    style: 'Meat Lovers',
  },
  {
    sizeInches: 8,
    sauce: 'Alfredo',
    style: 'Cheese',
  },
  {
    sizeInches: 12,
    sauce: 'Tomato',
    style: 'Veggie Lovers',
  }
]

console.log('THE PIZZAS WE NEED TO MAKE ARE: ')
for (var i = 0; i < pizzaList.length; i++){
  console.log('Pizza ' + i)
  console.log('Size: ' + pizzaList[i].sizeInches) // listName[index].key
	console.log('Sauce: ' + pizzaList[i].sauce)
  console.log('Style: ' + pizzaList[i].style)
  console.log('\n')   // "\n" adds a new line in the console so we can separate the pizzas!
}
```


### Arrays of Objects WITH Arrays in them:



Here we're going to tackle two new ideas! First, what if we had a list of pizzas, but what if each of our pizzas had a list of ingredients? Let's see what that looks like first (we'll change our meat lovers to have a whole slew of meats, our vegetarian will have just veggies, and our cheese will have… well, cheese):

```javascript
var pizzaList =  [
  {
    sizeInches: 12,
    sauce: 'Tomato',
    ingredients: ['Pepperoni', 'Sausage', 'Bacon', 'Chicken', 'Anchovies', 'Bratwurst'],
  },
  {
    sizeInches: 8,
    sauce: 'Alfredo',
    ingredients: ['Cheese'],
  },
  {
    sizeInches: 12,
    sauce: 'Tomato',
    ingredients: ['Mushrooms', 'Spinach', 'Broccoli', 'Sweet Potato', 'Asparagus'],
  }
]


```



Those pizzas look delicious, but how are we going to print them out? We know we can print an array pretty easily with a for loop. We could try to hard code everything out like we've done before:

```javascript
var pizzaList =  [
  {
    sizeInches: 12,
    sauce: 'Tomato',
    style: 'Meat Lovers',
    ingredients: ['Pepperoni', 'Sausage', 'Bacon', 'Chicken', 'Anchovies', 'Bratwurst'],
  },
  {
    sizeInches: 8,
    sauce: 'Alfredo',
    style: 'Cheese',
    ingredients: ['Cheese'],
  },
  {
    sizeInches: 12,
    sauce: 'Tomato',
    style: 'Veggie Lovers',
    ingredients: ['Mushrooms', 'Spinach', 'Broccoli', 'Sweet Potato', 'Asparagus'],
  }
]

console.log('THE PIZZAS WE NEED TO MAKE ARE: ')
for (var i = 0; i < pizzaList.length; i++){
  console.log('Pizza ' + i)
  console.log('Size: ' + pizzaList[i].sizeInches) // listName[index].key
	console.log('Sauce: ' + pizzaList[i].sauce)
  console.log('Style: ' + pizzaList[i].style)
  console.log('Ingredients: ')
  console.log(pizzaList[i].ingredients[0])
  console.log(pizzaList[i].ingredients[1])
  console.log(pizzaList[i].ingredients[2])
  console.log(pizzaList[i].ingredients[3])
  console.log(pizzaList[i].ingredients[4])
  console.log(pizzaList[i].ingredients[5])
  console.log('\n')   // "\n" adds a new line in the console so we can separate the pizzas!
}
```



What'd you notice? There were a lot of `undefined`s printed. That's because each of the objects has an ingredients list that is a different length! The `Meat Lovers` ingredients array is 6 elements long, the `Cheese` is just 1, and the `Veggie Lovers` is 5.

Since arrays come with that fancy `.length` method, let's use it!  There's nothing that says we can't put a loop inside of a loop! Let's give it a go!

```javascript
var pizzaList =  [
  {
    sizeInches: 12,
    sauce: 'Tomato',
    style: 'Meat Lovers',
    ingredients: ['Pepperoni', 'Sausage', 'Bacon', 'Chicken', 'Anchovies', 'Bratwurst'],
  },
  {
    sizeInches: 8,
    sauce: 'Alfredo',
    style: 'Cheese',
    ingredients: ['Cheese'],
  },
  {
    sizeInches: 12,
    sauce: 'Tomato',
    style: 'Veggie Lovers',
    ingredients: ['Mushrooms', 'Spinach', 'Broccoli', 'Sweet Potato', 'Asparagus'],
  }
]

console.log('THE PIZZAS WE NEED TO MAKE ARE: ')
for (var i = 0; i < pizzaList.length; i++){
  console.log('Pizza ' + i)
  console.log('Size: ' + pizzaList[i].sizeInches) // listName[index].key
	console.log('Sauce: ' + pizzaList[i].sauce)
  console.log('Style: ' + pizzaList[i].style)
  console.log('Ingredients: ')

  // adding INSIDE loop here: Make sure to use a different variable for counting and not `i`
  for (var j = 0; j < pizzaList[i].ingredients.length; j++){
    console.log(pizzaList[i].ingredients[j])
  }

  console.log('\n')   // "\n" adds a new line in the console so we can separate the pizzas!
}
```



There's so much going on! Let's take a moment and look just at that internal `for` loop:

```javascript
  // adding INSIDE loop here: Make sure to use a different variable for counting and not `i`
  for (var j = 0; j < pizzaList[i].ingredients.length; j++){
    console.log(pizzaList[i].ingredients[j])
  }
```



Here we are declaring a new loop, but this time we're usting `j` instead of `i`. That's because we've already declared an `i` above in the first for loop!  We need that `i` to access the `pizzaList` object by using `pizzaList[i]`.

 When we're declaring our stopping codition in the `for` loop, see how we're accessing the length of ingredients by `pizzaList[i].ingredients.length`?  This works just like `pizzaList.length`, but now it's checking the length of the ingredients inside of of `pizzaList[i]`.

Finally, to access each individual ingredient, notice how we're using `i` to denote which pizza we're looking at, and `j` to denote which ingredient we're looking at!

Loops inside of loops are called `nested loops`. They're very powerful, but they definitely take a minute to understand, so if it doesn't make too much sense right, no worries! We'll come back to these later. For now, take a look at this code (which will print out every single `i` and `j` along with the pizzas and ingredients)

```javascript
var pizzaList =  [
  {
    sizeInches: 12,
    sauce: 'Tomato',
    style: 'Meat Lovers',
    ingredients: ['Pepperoni', 'Sausage', 'Bacon', 'Chicken', 'Anchovies', 'Bratwurst'],
  },
  {
    sizeInches: 8,
    sauce: 'Alfredo',
    style: 'Cheese',
    ingredients: ['Cheese'],
  },
  {
    sizeInches: 12,
    sauce: 'Tomato',
    style: 'Veggie Lovers',
    ingredients: ['Mushrooms', 'Spinach', 'Broccoli', 'Sweet Potato', 'Asparagus'],
  }
]

console.log('THE PIZZAS WE NEED TO MAKE ARE: ')
for (var i = 0; i < pizzaList.length; i++){
  console.log('Pizza ' + i)
  console.log('Size: ' + pizzaList[i].sizeInches) // listName[index].key
	console.log('Sauce: ' + pizzaList[i].sauce)
  console.log('Style: ' + pizzaList[i].style)
  console.log('Ingredients: ')

  // adding INSIDE loop here: Make sure to use a different variable for counting and not `i`
  for (var j = 0; j < pizzaList[i].ingredients.length; j++){
    console.log(pizzaList[i].ingredients[j] + ' : i = ' + i + ' j = ' + j )
  }

  console.log('\n')   // "\n" adds a new line in the console so we can separate the pizzas!
}
```
