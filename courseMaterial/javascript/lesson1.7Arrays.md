### Arrays

Up to now, all of the variables that we've worked with have stored only one value. That's really helpful (and you'll use it a lot), but it's also possible to store a bunch of values in a single variable! These are what we call 'arrays'.

Arrays are typically used to store a list of things that are similar, like names, dates, etc.

Think of an array as a box with some values in it!

```javascript
var array = [7.23, -5.3, 1.28]
```

Now we have an array called *array* (clever, right?) which we can think of like a box with those values inside:

![Vector](../img/Vector.png)

To access what's inside of an array, we need to use a special notation like:

```javascript
arrayName[indexOfPosition]
```

All array elements have an index that starts counting at 0. `array` above has 3 indexes, numbered `0`, `1`, and `2`.  It may not make that much sense now, but that is the typical convention for how to write arrays in many langauges.

To access elements in our var `array`, we then could use the notation:

```javascript
console.log('The first element of our array is: ' + array[0])
console.log('The second element of our array is: ' + array[1])
console.log('The third element of our array is: ' + array[2])
```

And because our arrays are `var`s, we can change what's inside! Let's start over with our code:

```javascript
var array = [7.23, -5.3, 1.28]

console.log('The first element of our array is: ' + array[0])
console.log('The second element of our array is: ' + array[1])
console.log('The third element of our array is: ' + array[2])

array[1] = -1.08
array[2] = 3.25

console.log('The first element of our array is: ' + array[0])
console.log('The second element of our array is: ' + array[1])
console.log('The third element of our array is: ' + array[2])
```



You can think of what's happening in `array` as:

![Vector](../img/VectorCrossover.png)

Now, what if, instead of having only 3 elements in our array, we had 100?  Instead of writing a console log for all 100 elements, we can use loops! Remember the `.length` we could use for strings? We can also use that for arrays! This is really good for knowing how many times we want to loop! Check it out:

```javascript
var array = [7.23, -5.3, 1.28]

for(var i = 0; i < array.length; i++) {
  console.log('The element at index ' + i + ' is ' + array[i])
}

array[1] = -1.08
array[2] = 3.25

for(var i = 0; i < array.length; i++) {
  console.log('The element at index ' + i + ' is ' + array[i])
}
```
