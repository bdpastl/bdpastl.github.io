### Ifs Elses:
These follow the exact same logic as how we speak:

` If I eat icecream then I will be happy! ELSE (that is, if I don't eat ice cream) I will be very sad. `

What's different is that in the code, we need to have our sentence follow a special syntax:

```javascript
	if(some truthy statement) {
		// MAKE SURE TO WRAP THIS IN CURLY BRACES LIKE SO:
		console.log('someSpecialOutcome is happening because our truthy statement was true');
	} else {
		console.log('some other outcome is happening if the trythy statement is false');
	};
```

Let's code this out:

```javascript
	let snackIWillEat = 'iceCream';

	if(snackIWillEat == 'iceCream'){
		alert('I AM VERY HAPPY!');
	}
	else {
		console.log('NOW I AM SAD')
	};
```

This code alerted us that I was happy because I ate ice cream! What if I didn't, though? Let's try it again:

```javascript
	let snackIWillEat = 'broccoli';
	if(snackIWillEat == 'iceCream'){
		alert('I AM VERY HAPPY!');
	}
	else {
		console.log("Well now I'm sad");
	};
```

Now we see that in the console, I printed that I was sad. That's because 'broccoli' just isn't ice cream.

It's fun to know whether or not someone will be sad when they don't eat ice cream, BUT why are conditionals useful? What if you needed somebody to log into a website? You would need a conditional to verify that they were who they said they were!

```javascript
	let userName = prompt("Who are you?");

	if(userName == "Spice Girls") {
		alert("SPICE UP YOUR LIFE");
	}
	else {
		alert("Get out of here you unspicy person!");
	};
```

Now, let's take a second and talk about using multiple ifs! You can "nest" if/else statments:

```javascript
	let userName = prompt("Who are you?");

	if(userName == "Spice Girls") {
		alert("SPICE UP YOUR LIFE");
	} else if (userName == "Beastie Boys"){
		alert("FIGHT FOR YOUR RIGHT TO PARTY!!");
	}
	else {
		alert("Get out of here you unspicy person!");
	};
```

You can nest as many if elses as you want! If this looks super weird, don't worry too much on syntax now. We'll be doing this a lot, and it will eventually sink in!
