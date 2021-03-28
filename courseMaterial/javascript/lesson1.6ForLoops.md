### For loops:

For loops are the exact same as while loops, but they're a bit more compact! They look like:
```javascript
for( initializer ; condition to check ; something to do after the code runs ){
	// looped code goes here
}
```

What that looks like is:

```javascript
for (var i = 0; i < 10; i = i + 1){
	console.log("I like to repeat myself. " + i + " times");
}
```

You may be wondering what the point of a for loop is, since we can do everything in a while loop just as easily. A lot of people use for loops so that they can easily iterate over arrays (which we're talking about next)!
