## User Input:

There are a number of functions we'll be using throughout the course, and most of those will be defined by us. There are a couple of functions that we'll want to know about before we start using a lot of javascript.

### alert():
Arguably one of the most annoying functions, alert is a really helpful function because it quite literally alerts the user and won't let them do anything until they've acknowledged what the alert is:

```javascript
let alertMessage = 'HEY USER! LOOK AT ME!';

alert(alertMessage);
```

This is often used for forgotten passwords or unsaved data, though it's not unheard of for sites to use alert for poor reasons.

### prompt()

Prompt lets us very blatantly ask questions of our users. Just like alert, we can pass a string into our prompt, but this also comes with a text box for a user response:

```javascript
    let nameQuestion = "What is your name?";
    prompt(nameQuestion);
```
You can then enter your name. However, did you notice that nothing happened with your name? Let's try saving that data:

```javascript
    let nameQuestion = "What is your name?";
    let userName = prompt(nameQuestion);

    // get both alerts and console.logs!
    alert('Hi ' + userName);
    console.log('Hello! ' + userName);
```