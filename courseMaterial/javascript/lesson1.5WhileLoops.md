## Loops:

Loops are a way for us to do a bunch of things without writing a lot of code! Suppose I wanted to, for some crazy reason, print out "I LIKE TURTLES" 100 times. You could write:
```javascript
console.log("I LIKE TURTLES")
console.log("I LIKE TURTLES")
console.log("I LIKE TURTLES")
console.log("I LIKE TURTLES")
console.log("I LIKE TURTLES")
console.log("I LIKE TURTLES")
...
... // Assume we wrote 100 console logs
...
console.log("I LIKE TURTLES")
console.log("I LIKE TURTLES")
console.log("I LIKE TURTLES")
console.log("I LIKE TURTLES")
```

We could write 100 console logs. That's crazy though. We're very busy people and we don't have time to do that! Instead we can use a loop! The two loops we'll be learning about are while loops and for loops!

### while:
A while loop is very simple it looks like:

```javascript
while( SOME TRUTHY STATEMENT ) {
	// DO STUFF HERE
}
```

So to write "I LIKE TURTLES" 100 times to the console, you simply write:
```javascript
var count = 0

while ( count < 100) {
	console.log("I LIKE TURTLES")
	count = count + 1     // this increments the count! I looks a little weird, but it's basically setting count equal to its old value + 1.
	}
```

Note: If you don't have a conditional statement in the the parentheses of the while loop, it will run forever (sometimes you'll want that, but most of the time you wont):

```javascript
var count = 0

while () {
	console.log("I LIKE TURTLES: " + count)
	count = count + 1     // this increments the count! I looks a little weird, but it's basically setting count equal to its old value + 1.
}
```

You might be wonder what the point of a loop is other than printing "I like turtles" a bunch of times. Suppose you have a login. What if your user enters the wrong information on accident? Let's take the nested if else from above and use that:

```javascript
var count = 0

while(count < 5){
    console.log('count', count)

	var userName = prompt("Who are you?")

  console.log("Your name is: ", userName)

	if(userName == "Spice Girls") {
		alert("SPICE UP YOUR LIFE")
	}
	else if (userName == "Beastie Boys"){
		alert("FIGHT FOR YOUR RIGHT TO PARTY!!")
	}
	else {
		alert("Get out of here you unspicy person!")
	}

	count = count + 1
}

console.log("it's over!")

```