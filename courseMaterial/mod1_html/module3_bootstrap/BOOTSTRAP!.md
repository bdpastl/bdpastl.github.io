# BOOTSTRAP! 

www.getbootstrap.com 



Up until now, we've been relying on HTML and CSS! Both of those are amazing, but to make a site look really good with html and css, you need to do a lot of extra work (think *HOURS* of styling). Luckily for us, there are libraries out there that we can use in a matter of minutes! One of the most popular libraries out there is bootstrap (which is made up of css and javascript). This helps us make a really amazing looking website without an incredible amount of work! 

So, to use bootstrap, we need to bring it in to our style sheet. We need to go to getboostrap.com. We can EITHER include bootstrap in your header by including its URL as a css file, OR we download all the bootstrap files (which will be good for all of us to do, since we don't always have access to the internet). 

I would 100% recommend downloading bootstrap since it can load when your'e working offline, but for the sake of our learning (since we're on codepen and all on the internet right now), we'll be using the URL version because we're posting our code into codepen and GitHub.io! 

To use bootstrap by their web links, all we need to do is grab the link and script (we won't be using the script just yet, but it's good to have) from bootstrap's site (https://getbootstrap.com/docs/3.4/). 



As a quick reminder, here's what a site with [no bootstrap looks like](https://codepen.io/bdpastl/pen/GLrYyN): 

```html
<!doctype html>
<html>
  <head>
  </head>
  <body>
    <h1> This is a site with no bootstrap </h1>
    <div>It's just like everything we've worked on before, but with no styling</div>
    <button> I'm a boring button </button>
  </body>
</html>
```

^^ Pretty boring, right? Now, once we add our headers into our site, [our styling will completely change](https://codepen.io/bdpastl/pen/BEpqJZ): 

```html
<!doctype html>
<html>
  <head>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">

    <!-- Latest compiled and minified JavaScript -->
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js" integrity="sha384-aJ21OjlMXNL5UyIl/XNwTMqvzeRMZH2w8c5cRVpzpU8Y5bApTppSuUkhZXN0VxHd" crossorigin="anonymous"></script>
  </head>
  <body>
    <h1> This is a site with Bootstrap! </h1>
    <div>Check out how our font changed!</div>
    <button> I should look way better</button>
  </body>
</html>

```



You probably noticed that the `<h1>` and `<div>` text changed on their own without adding a class, while the button required us to specifically add a class. That's because in bootstrap's css, there are some element level stylings, like 

```css
/* At line 362 in bootstrap's css file */
h1, h2, h3, h4, h5, h6,.h1, .h2, .h3, .h4, .h5, .h6 {
  margin-bottom: 0.5rem;
  font-weight: 500;
  line-height: 1.2;
}
```



So, our site has changed, but you'd think there'd be more, right? You're absolutely right! There is so much more! While bootstrap does have a lot of inherently different things, we'll often have to use classes provided by bootstrap!  Let's take a quick look at bootstrap's button class: 

```css
.btn {
  display: inline-block;
  font-weight: 400;
  color: #212529;
  text-align: center;
  vertical-align: middle;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  background-color: transparent;
  border: 1px solid transparent;
  padding: 0.375rem 0.75rem;
  font-size: 1rem;
  line-height: 1.5;
  border-radius: 0.25rem;
  transition: color 0.15s ease-in-out, background-color 0.15s ease-in-out, border-color 0.15s ease-in-out, box-shadow 0.15s ease-in-out;
}
```

(There's no real need to know what's inside of these buttons, but it's good to see that there's a lot of styling in there. Mostly styling we'd rather not do. Why reinvent the wheel?) [Let's see what that looks like below](https://codepen.io/bdpastl/pen/dLNgdY): 

```html
<!doctype html>
<html>
  <head>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">

    <!-- Latest compiled and minified JavaScript -->
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js" integrity="sha384-aJ21OjlMXNL5UyIl/XNwTMqvzeRMZH2w8c5cRVpzpU8Y5bApTppSuUkhZXN0VxHd" crossorigin="anonymous"></script>
  </head>
  <body>
    <h1> This is a site with Bootstrap! </h1>
    <div>Check out how our font changed!</div>
    <button class='btn btn-success'> I NOW look way better</button>
  </body>
</html>

```

 We'll learn a lot more about bootstrap as we go on, but just know that everything you see here is just a tiny amount of what bootstrap can do! For every lesson we go over, documentation will be posted, but do some exploration for yourself! You might find something really cool. 

**NOTE:** Throughout the class, you've been learning a ton of material. You are not expected to memorize this material. Documentation exists online so that we can easily refer to it. Professional developers forget things all the time! That's why documentation exists



## Buttons

So natraully, we just saw a button in the two examples before, let's talk about buttons. Bootstrap has a ton of button options. You can find the button documentation here: https://getbootstrap.com/docs/3.4/css/#buttons. [Take a look!](https://codepen.io/bdpastl/pen/zXNmRX?editors=1000) 

```html
<!doctype html>
<html>
  <head> 
    <title>Press my buttons!</title>
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">

    <!-- Latest compiled and minified JavaScript -->
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js" integrity="sha384-aJ21OjlMXNL5UyIl/XNwTMqvzeRMZH2w8c5cRVpzpU8Y5bApTppSuUkhZXN0VxHd" crossorigin="anonymous"></script>
  </head>
  <body>
    <h1> This is a site with Bootstrap! </h1>
    <div>Check out all the button types below (they're not linked to anything right now, so they just sit there and look good):</div> <hr />                

    <!-- These were literally just copy pasted from bootstrap!-->
    <!-- Standard button -->
    <button type="button" class="btn btn-default">I'm a Default button</button>

    <!-- Provides extra visual weight and identifies the primary action in a set of buttons -->
    <button type="button" class="btn btn-primary">I'm the Primary button</button>

    <!-- Indicates a successful or positive action -->
    <button type="button" class="btn btn-success">I'm a Success button</button>

    <!-- Contextual button for informational alert messages -->
    <button type="button" class="btn btn-info">I'm an Info button</button>

    <!-- Indicates caution should be taken with this action -->
    <button type="button" class="btn btn-warning">I'm a Warning button</button>

    <!-- Indicates a dangerous or potentially negative action -->
    <button type="button" class="btn btn-danger"> I'm a Danger button</button>

    <!-- Deemphasize a button by making it look like a link while maintaining button behavior -->
    <button type="button" class="btn btn-link">I'm a really pretty Link</button>
  </body>
</html>
```



 You can also change the size of buttons by using [btn-lg, btn-sm, btn-xs](https://codepen.io/bdpastl/pen/ROKeMG?editors=1000): 

```html
<!doctype html>
<html>
  <head> 
    <title>Press my buttons!</title>
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">

    <!-- Latest compiled and minified JavaScript -->
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js" integrity="sha384-aJ21OjlMXNL5UyIl/XNwTMqvzeRMZH2w8c5cRVpzpU8Y5bApTppSuUkhZXN0VxHd" crossorigin="anonymous"></script>
  </head>
  <body>
    <h1> This is a site with Bootstrap! </h1>
    <div>Check out all the button types below (they're not linked to anything right now, so they just sit there and look good):</div> <hr />                


    <button type="button" class="btn btn-default">I'm a Default button, with default size</button>
    <br />

    <button type="button" class="btn btn-primary btn-lg">I'm LARGE the Primary button</button>
    <br />

    <button type="button" class="btn btn-success btn-sm">I'm a small Success button</button>

    <br />

    <button type="button" class="btn btn-info btn-xs">I'm a xtra-small Info button</button>

    <br />

    <button type="button" class="btn btn-warning btn-lg">I'm a large Warning button</button>
    <br />

    <button type="button" class="btn btn-danger btn-lg"> I'm a large Danger button</button>
    <br />

    <button type="button" class="btn btn-link btn-lg">I'm a really pretty BIG Link</button>

  </body>
</html>
```



You can use button classes on [things that aren't just buttons](https://codepen.io/bdpastl/pen/WWRazM?editors=1000):  

```html
<!doctype html>
<html>
  <head> 
    <title>Press my buttons!</title>
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">

    <!-- Latest compiled and minified JavaScript -->
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js" integrity="sha384-aJ21OjlMXNL5UyIl/XNwTMqvzeRMZH2w8c5cRVpzpU8Y5bApTppSuUkhZXN0VxHd" crossorigin="anonymous"></script>
  </head>
  <body>
    <h1> This is a site with Bootstrap! </h1>
    <div>Below is an anchor tag that's using a button class:</div> <hr />                
    <a href='https://bdpastl.github.io' class='btn btn-info'>Check me out!</a>

  </body>
</html>
```

There are a ton of classes that we can use for buttons. Take a look through the documentation to see if you want to use any of those! (We'll revisit buttons later once we start using javascript).



## JUMBOTRONS

Jumbotrons are for when you want really [showcase some material!](https://codepen.io/bdpastl/pen/mgRzLO?editors=1000) 

```html
<!doctype html>
<html>
   <head> 
     <title>Jumbotron!!</title>
     <!-- Latest compiled and minified CSS -->
     <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">

     <!-- Latest compiled and minified JavaScript -->
     <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js" integrity="sha384-aJ21OjlMXNL5UyIl/XNwTMqvzeRMZH2w8c5cRVpzpU8Y5bApTppSuUkhZXN0VxHd" crossorigin="anonymous"></script>
   </head>
   <body>
     <div class='jumbotron'> <h1> This is a site with Bootstrap! </h1>
       <div>Below is an anchor tag that's using a button class:</div> <hr />                
       <a href='https://bdpastl.github.io' class='btn btn-info'>Check me out!</a>

       <div> Doesn't this look much better? </div>
     </div>

     <div> Here's some stuff outside the jumbotron.</div>
   </body>
</html>
```



That looks great and all, but let's throw that jumbotron in a [container for some extra padding](https://codepen.io/bdpastl/pen/MRJPGP?editors=1000): 

```html
<!doctype html>
 <html>
   <head> 
     <title>Jumbotrons!</title>
     <!-- Latest compiled and minified CSS -->
     <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">

     <!-- Latest compiled and minified JavaScript -->
     <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js" integrity="sha384-aJ21OjlMXNL5UyIl/XNwTMqvzeRMZH2w8c5cRVpzpU8Y5bApTppSuUkhZXN0VxHd" crossorigin="anonymous"></script>
   </head>
   <body>
     <div class='container'>
       <div class='jumbotron'> <h1> This is a site with Bootstrap! </h1>
         <div>Below is an anchor tag that's using a button class:</div> <hr />                
         <a href='https://bdpastl.github.io' class='btn btn-info'>Check me out!</a>

         <div> Doesn't this look much better? </div>
       </div>

       <div>Here's some stuff outside the jumbotron, but now INSIDE our container. Try moving me outisde the container! </div>
     </div>
   </body>
</html>
```





## FORMS & INPUTS!

We haven't spent any time on forms just yet, but it's good to know that bootstrap has a very sleek form styling! There are an infinite number of form possibilities. To get some kind of idea of what kind of form you'd like, check out the form documentation: https://getbootstrap.com/docs/3.4/css/#forms

[See the code in action!](https://codepen.io/bdpastl/pen/vMgVrX?editors=1000)

```html
<!doctype html>
<html>
  <head> 
    <title>Forms!</title>
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">

    <!-- Latest compiled and minified JavaScript -->
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js" integrity="sha384-aJ21OjlMXNL5UyIl/XNwTMqvzeRMZH2w8c5cRVpzpU8Y5bApTppSuUkhZXN0VxHd" crossorigin="anonymous"></script>
  </head>
  <body>
    <div class='container'>
      <div class='jumbotron'> <h1> This is a site with Bootstrap! </h1>
        <div>Below is an anchor tag that's using a button class:</div> <hr />                
        <a href='https://bdpastl.github.io' class='btn btn-info'>Check me out!</a>

        <div> Doesn't this look much better? </div>
      </div>

      <div>Below is a form!</div>
      <div>(notice how the text box goes across the entire page? We could use our CSS to deal with that, but bootstrap has a grid system, which we'll learn about soon!)</div>
      <form>
        <div class="form-group"> <!-- The class Form group has special spacing for us! -->
          <label for="exampleInputEmail1">Email address</label>
          <input type="email" class="form-control" id="exampleInputEmail1" placeholder="Email"> <!-- Form control gives us a special css class for our inputs! Try removing it to see what happens! -->
        </div>
        <div class="form-group">
          <label for="exampleInputPassword1">Password</label>
          <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Password">
        </div>
        <div class="form-group">
          <label for="exampleInputFile">File input</label>
          <input type="file" id="exampleInputFile">
          <p class="help-block">Example block-level help text here.</p>
        </div>
        <div class="checkbox">
          <label>
            <input type="checkbox"> Check me out
          </label>
        </div>
        <button type="submit" class="btn btn-default">Submit</button> 
      </form>
    </div>
  </body>
</html>
```



You can also make your form take up a significantly smaller area by adding the `class='form-inline'` (remember how we used `inline` to make our divs fit inside of other elements?) [to your form](https://codepen.io/bdpastl/pen/JVEmaj?editors=1000): 

```html
  <!doctype html>
  <html>   
    <head> 
      <title>Forms!</title>
      <!-- Latest compiled and minified CSS -->
      <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">

      <!-- Latest compiled and minified JavaScript -->
      <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js" integrity="sha384-aJ21OjlMXNL5UyIl/XNwTMqvzeRMZH2w8c5cRVpzpU8Y5bApTppSuUkhZXN0VxHd" crossorigin="anonymous"></script>
    </head>
    <body>
      <div class='container'>
        <div class='jumbotron'> <h1> This is a site with Bootstrap! </h1>
          <div>Below is an anchor tag that's using a button class:</div> <hr />                
          <a href='https://bdpastl.github.io' class='btn btn-info'>Check me out!</a>

          <div> Doesn't this look much better? </div>
        </div>

        <div>Below is a form!</div>
        <div>(notice how the text box goes across the entire page? We could use our CSS to deal with that, but bootstrap has a grid system, which we'll learn about soon!)</div>
        <form flass='form-inline'>
          <div class="form-group"> <!-- The class Form group has special spacing for us! -->
            <label for="exampleInputEmail1">Email address</label>
            <input type="email" class="form-control" id="exampleInputEmail1" placeholder="Email"> <!-- Form control gives us a special css class for our inputs! Try removing it to see what happens! -->
          </div>
          <div class="form-group">
            <label for="exampleInputPassword1">Password</label>
            <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Password">
          </div>
          <div class="form-group">
            <label for="exampleInputFile">File input</label>
            <input type="file" id="exampleInputFile">
            <p class="help-block">Example block-level help text here.</p>
          </div>
          <div class="checkbox">
            <label>
              <input type="checkbox"> Check me out
            </label>
          </div>
          <button type="submit" class="btn btn-default">Submit</button> 
        </form>
      </div>
    </body>
</html>
```





## Navbars!

 Navbars help us navigate sites! Many sites you've been to are gargantuan, and it's hard to navigate a site just with scrolling (on inline links). These make it much easier to traverse a site, [and they make our sites look really professional](https://codepen.io/bdpastl/pen/EJZdeq?editors=1000).

```html
<!doctype html>
<html>
  <head> 
    <title>Navbar!</title>
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">

    <!-- Latest compiled and minified JavaScript -->
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js" integrity="sha384-aJ21OjlMXNL5UyIl/XNwTMqvzeRMZH2w8c5cRVpzpU8Y5bApTppSuUkhZXN0VxHd" crossorigin="anonymous"></script>
  </head>
  <body>
    <nav class='navbar navbar-default' style='background-color:#f1f1f1'>
      Here's my navbar
    </nav>
  </body>
</html>
```



The navbar doesn't really look like anything here, but that's because we don't have any of the [corresponding elements inside it](https://codepen.io/bdpastl/pen/mgRzzW?editors=1000)!

```html
<!doctype html>
<html>
  <head> 
    <title>Navbars!</title>
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">

    <!-- Latest compiled and minified JavaScript -->
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js" integrity="sha384-aJ21OjlMXNL5UyIl/XNwTMqvzeRMZH2w8c5cRVpzpU8Y5bApTppSuUkhZXN0VxHd" crossorigin="anonymous"></script>
  </head>
  <body>
    <nav class='navbar navbar-default'>
      <div class='navbar-header' style='background-color:#f1f1f1'>
        <a href='#' class='navbar-brand'>My Name</a>
      </div>
    </nav>
  </body>
</html>
```

Let's add some links [(though they'll all be empty for a while)](https://codepen.io/bdpastl/pen/WWRaLJ?editors=1000):

```html
<!doctype html>
<html>
  <head> 
    <title>Navbars!</title>
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">

    <!-- Latest compiled and minified JavaScript -->
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js" integrity="sha384-aJ21OjlMXNL5UyIl/XNwTMqvzeRMZH2w8c5cRVpzpU8Y5bApTppSuUkhZXN0VxHd" crossorigin="anonymous"></script>
  </head>
  <body>
    <nav class='navbar navbar-default'>
      <div class='navbar-header' style='background-color:#f1f1f1'>
        <a href='#' class='navbar-brand'>My Name</a>
      </div>

      <ul class='nav navbar-nav'>
        <li> <a href='#'> Photo Gallery </a></li>
        <li> <a href='#'> Blog </a></li>
      </ul>

      <ul class='nav navbar-nav navbar-right'>
        <li> <a href='#'> About Me </a></li>
        <li> <a href='#'> Code Portfolio </a></li>
        <li> <a href='#'> Contact </a></li>
      </ul>
    </nav>
  </body>
</html>
```



SPACING IS EVERYTHING [(notice contact is against the far right side)](https://codepen.io/bdpastl/pen/XQpxoL?editors=1000): 

```html
<!doctype html>
<html>
  <head> 
    <title>Navbar!</title>
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">

    <!-- Latest compiled and minified JavaScript -->
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js" integrity="sha384-aJ21OjlMXNL5UyIl/XNwTMqvzeRMZH2w8c5cRVpzpU8Y5bApTppSuUkhZXN0VxHd" crossorigin="anonymous"></script>
  </head>
  <body>
    <nav class='navbar navbar-default'>
      <div class='container'>
        <div class='navbar-header' style='background-color:#f1f1f1'>
          <a href='#' class='navbar-brand'>My Name</a>
        </div>

        <ul class='nav navbar-nav'>
          <li> <a href='#'> Photo Gallery </a></li>
          <li> <a href='#'> Blog </a></li>
        </ul>

        <ul class='nav navbar-nav navbar-right'>
          <li> <a href='#'> About Me </a></li>
          <li> <a href='#'> Code Portfolio </a></li>
          <li> <a href='#'> Contact </a></li>
        </ul>
      </div>
    </nav>
  </body>
</html>
```

What do you think would happen if you put the navbar inside the container?



Now that we understand what's happening in the nav-bar, let's checkout the [bootstrap navbar that we can add to our site](https://codepen.io/bdpastl/pen/pBRxGQ?editors=1000): 

```html
<!doctype html>
<html>
  <head> 
    <title>NAVBAR!</title>
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">

    <!-- Latest compiled and minified JavaScript -->
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js" integrity="sha384-aJ21OjlMXNL5UyIl/XNwTMqvzeRMZH2w8c5cRVpzpU8Y5bApTppSuUkhZXN0VxHd" crossorigin="anonymous"></script>
  </head>
  <body>
    <nav class="navbar navbar-default">
      <div class="container-fluid">
        <!-- Brand and toggle get grouped for better mobile display -->
        <div class="navbar-header">
          <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1" aria-expanded="false">
            <span class="sr-only">Toggle navigation</span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
          </button>
          <a class="navbar-brand" href="#">Brand</a>
        </div>

        <!-- Collect the nav links, forms, and other content for toggling -->
        <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
          <ul class="nav navbar-nav">
            <li class="active"><a href="#">Link <span class="sr-only">(current)</span></a></li>
            <li><a href="#">Link</a></li>
            <li class="dropdown">
              <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">Dropdown <span class="caret"></span></a>
              <ul class="dropdown-menu">
                <li><a href="#">Action</a></li>
                <li><a href="#">Another action</a></li>
                <li><a href="#">Something else here</a></li>
                <li role="separator" class="divider"></li>
                <li><a href="#">Separated link</a></li>
                <li role="separator" class="divider"></li>
                <li><a href="#">One more separated link</a></li>
              </ul>
            </li>
          </ul>
          <form class="navbar-form navbar-left">
            <div class="form-group">
              <input type="text" class="form-control" placeholder="Search">
            </div>
            <button type="submit" class="btn btn-default">Submit</button>
          </form>
          <ul class="nav navbar-nav navbar-right">
            <li><a href="#">Link</a></li>
            <li class="dropdown">
              <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">Dropdown <span class="caret"></span></a>
              <ul class="dropdown-menu">
                <li><a href="#">Action</a></li>
                <li><a href="#">Another action</a></li>
                <li><a href="#">Something else here</a></li>
                <li role="separator" class="divider"></li>
                <li><a href="#">Separated link</a></li>
              </ul>
            </li>
          </ul>
        </div><!-- /.navbar-collapse -->
      </div><!-- /.container-fluid -->
    </nav>
  </body>
</html>
```



This looks really cool! But, even though we're pulling in the bootstrap css and javascript libraries, we're missing one tiny thing - jQuery. If you google jquery cdn it'll be at the first link (or just take the links I post in the code). Make sure that you place the jQuery file before the src for the javascript file! We'll talk about why this all works later, but fow now, let's make our own [navbar do what the above one does!](https://codepen.io/bdpastl/pen/mgRzom?editors=1000)! 

```html
<!doctype html>

<html>
  <head> 
    <title>Press my buttons!</title>
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">

    <script  src="http://code.jquery.com/jquery-3.3.1.js"   integrity="sha256-2Kok7MbOyxpgUVvAk/HJ2jigOSYS2auK4Pfzbm7uH60="   crossorigin="anonymous"></script>


    <!-- Latest compiled and minified JavaScript -->
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js" integrity="sha384-aJ21OjlMXNL5UyIl/XNwTMqvzeRMZH2w8c5cRVpzpU8Y5bApTppSuUkhZXN0VxHd" crossorigin="anonymous"></script>


  </head>
  <body>
    <nav class="navbar navbar-default">
      <div class="container-fluid">
        <!-- Brand and toggle get grouped for better mobile display -->
        <div class="navbar-header">
          <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1" aria-expanded="false">
            <span class="sr-only">Toggle navigation</span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
          </button>
          <a class="navbar-brand" href="#">Brand</a>
        </div>

        <!-- Collect the nav links, forms, and other content for toggling -->
        <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
          <ul class="nav navbar-nav">
            <li class="active"><a href="#">Link <span class="sr-only">(current)</span></a></li>
            <li><a href="#">Link</a></li>
            <li class="dropdown">
              <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">Dropdown <span class="caret"></span></a>
              <ul class="dropdown-menu">
                <li><a href="#">Action</a></li>
                <li><a href="#">Another action</a></li>
                <li><a href="#">Something else here</a></li>
                <li role="separator" class="divider"></li>
                <li><a href="#">Separated link</a></li>
                <li role="separator" class="divider"></li>
                <li><a href="#">One more separated link</a></li>
              </ul>
            </li>
          </ul>
          <form class="navbar-form navbar-left">
            <div class="form-group">
              <input type="text" class="form-control" placeholder="Search">
            </div>
            <button type="submit" class="btn btn-default">Submit</button>
          </form>
          <ul class="nav navbar-nav navbar-right">
            <li><a href="#">Link</a></li>
            <li class="dropdown">
              <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">Dropdown <span class="caret"></span></a>
              <ul class="dropdown-menu">
                <li><a href="#">Action</a></li>
                <li><a href="#">Another action</a></li>
                <li><a href="#">Something else here</a></li>
                <li role="separator" class="divider"></li>
                <li><a href="#">Separated link</a></li>
              </ul>
            </li>
          </ul>
        </div><!-- /.navbar-collapse -->
      </div><!-- /.container-fluid -->
    </nav>
  </body>
</html>

```





## Bootstrap Grid System: 

So now we know how to make some really cool things in bootstrap, let's take a second to talk about how bootstrap works on a website with its "grid system"

Up until now, we've only worked with block and inline elements. The only way we really knew how to make things smaller was to use something like  _float_  or by using flexbox. A big reason people like to use bootstrap is that bootstrap has a built in 'grid' system, which takes care of a lot tedious hours of styling our website structure and layout for us! (See an example of bootstrap at bdpastl.github.io - when there, try to make the window smaller and see what happens! That's the grid system in action!)

When we say "grid system" what we mean is that bootstrap is set up in such a way that there are 12 columns on the site (this will make a lot more sense in a minute). When we're styling our site, all we need to do is make sure that our containers all add up to 12! 


 [Let's take a look](https://codepen.io/bdpastl/pen/YMNJMp?editors=1000): 

```html
<!doctype html>

<html>
  <head> 
    <title>GRIDS ARE NEAT!</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">
    <style>
      .border-red{ border: 1px solid red }
      .border-orange{ border: 1px solid orange }
      .border-yellow{ border: 1px solid yellow }
      .border-green{ border: 1px solid green }
      .border-blue{ border: 1px solid blue }
      .border-indigo{ border: 1px solid indigo } 
      .border-violet{ border: 1px solid violet }

      .container1{ background-color: gray }
      .container2{ background-color: lightGray }
      .container3{ background-color: DimGray }
      .container4{ background-color: SlateGray }
      .container5{ background-color: silver }

    </style>
  </head>
  <body >
    <div class='container container1'>
      <div class='col col-xl-12 border-red'> I am a column that takes up the entire screen because I have 12 columns </div>
    </div>
    <div class='container container2'>
      <div class='col col-lg-6 border-orange'>We take up only half the screen because we've got '6' columns </div>
      <div class='col col-lg-6 border-yellow'>We take up only half the screen because we've got '6' columns</div>
    </div>
    <div class='container container3'>
      <div class='col col-md-4 border-green'> We take up 4 columns! </div>
      <div class='col col-md-4 border-blue'> There are 3 of us! </div>
      <div class='col col-md-4 border-indigo'> and you know, that 3 * 4 = 12! </div>
    </div>
    <div class='container container4'>
      <div class='col col-sm-3 border-violet'>The four of us take 3 columns each</div>
      <div class='col col-sm-3 border-red'> It's pretty cool if you ask me</div>
      <div class='col col-sm-3 border-yellow'>We can fit some neat things here</div>
      <div class='col col-sm-3 border-green'> Just gotta make sure we all add up to 12! (also, notice how I extend below the others?) </div>
    </div>
    <div class='container container5'>
      <div class='col col-xs-2 border-blue'>We all take up 2!</div>
      <div class='col col-xs-2 border-indigo'>We're very small </div>
      <div class='col col-xs-2 border-violet'> Not as small as 1s!</div>
      <div class='col col-xs-2 border-red'>but still pretty dang small</div>
      <div class='col col-xs-2 border-orange'>But at least there are 6 </div>
      <div class='col col-xs-2 border-yellow'>of us :D </div>
      <div class='col col-xs-1 border-green'>We </div>
      <div class='col col-xs-1 border-blue'> are</div>
      <div class='col col-xs-1 border-indigo'> all </div>
      <div class='col col-xs-1 border-violet'> only </div>
      <div class='col col-xs-1 border-red'> one </div>
      <div class='col col-xs-1 border-orange'> column </div>
      <div class='col col-xs-1 border-yellow'> wide</div>
      <div class='col col-xs-1 border-green'> but </div>
      <div class='col col-xs-1 border-blue'> there's </div>
      <div class='col col-xs-1 border-indigo'> a lot </div>
      <div class='col col-xs-1 border-violet'> of </div>
      <div class='col col-xs-1 border-red'> us!</div>                        
    </div>
    </div>
  </body>
</html>
```

Did you notice that the last couple rows were in the same container? You can have as many divs as you'd like in a container, but if you're using the grid system (which you should because it's awesome!), you need to make sure that your column size all adds up to 12! Interestingly enough though, try making your screen smaller and see what happens to the divs in the bottom container. Things get weird!

Speaking of columns adding up to 12, your columns don't all have to be of equal length if they're in a row! They only need to add up to 12! [Let's do some mixing and matching](https://codepen.io/bdpastl/pen/WWRaWy?editors=1000)!

```html
<!doctype html>

<html>
  <head> 
    <title>MIX AND MATCH!</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">
    <style>
      .border-red{ border: 1px solid red }
      .border-orange{ border: 1px solid orange }
      .border-yellow{ border: 1px solid yellow }
      .border-green{ border: 1px solid green }
      .border-blue{ border: 1px solid blue }
      .border-indigo{ border: 1px solid indigo } 
      .border-violet{ border: 1px solid violet }

      .container1{ background-color: gray }
      .container2{ background-color: lightGray }
      .container3{ background-color: DimGray }
      .container4{ background-color: SlateGray }
      .container5{ background-color: silver }

    </style>
  </head>
  <body >
    <div class='container container1'>
      <div class='col col-xl-12 border-red'> I am still a column that takes up the entire screen because I have 12 columns </div>
    </div>
    <div class='container container2'>
      <div class='col col-lg-6 border-orange'>I only take up only half the screen because I've got '6' columns </div>
      <div class='col col-xs-1 border-green'>I'm 1 </div>
      <div class='col col-md-3 border-red'> I'm 3 </div>
      <div class='col col-xs-2 border-blue'> and I'm 2!</div>

    </div>
    <div class='container container3'>
      <div class='col col-md-2 border-green'> Tiny 2s </div>
      <div class='col col-lg-8 border-blue'> Can surround an 8! </div>
      <div class='col col-md-2 border-indigo'> And add up to 12! </div>
    </div>
    <div class='container container4'>
      <div class='col col-sm-2 border-violet'>So long as we get 12</div>
      <div class='col col-sm-3 border-red'> Our containers will be fine! </div>
      <div class='col col-md-5 border-yellow'>We can do some neat column stuff!</div>
      <div class='col col-sm-2 border-green'> Columns are cool! </div>
    </div>
    <div class='container'>
      But what happens if we have columns that don't add up?
    </div>
     <div class='container container5'>
      <div class='col col-xs-1 border-blue'>ONE</div>
      <div class='col col-xs-2 border-indigo'>TWO </div>
      <div class='col col-sm-3 border-violet'> THREE</div>
      <div class='col col-md-4 border-red'> FOUR</div>
      <div class='col col-md-5 border-orange'>FIVE </div>                    
      <div class='col col-md-6 border-yellow'>SIX </div>                    
      <div class='col col-lg-7 border-green'>SEVEN </div>                    
      <div class='col col-md-8 border-blue'>EIGHT </div>                    
      <div class='col col-md-9 border-indigo'>NINE </div>                    
      <div class='col col-md-10 border-violet'>TEN </div>                    
      <div class='col col-md-11 border-red'>ELEVEN </div>                    
      <div class='col col-md-12 border-orange'>TWELVE! </div>   
       It doesn't look so great :( 
       Also why am I over here? Maybe try wrapping me in a div or something?
                    
    </div>
    </div>
  </body>
</html>
```



## Grids of differing sizes! 

Grid elements can have differing sizes! Did you notice the `col-xs-1`, `col-md-5`, `col-lg-6`, etc? Look at the below code (which is just our original grid from the first portion, but all the columns are `col-lg-#`). When you're on this screen, in codepen, shrink the size of the screen. [What happens?](https://codepen.io/bdpastl/pen/KYaGLr?editors=1000) 

```html
<!doctype html>
<html>
  <head> 
    <title>LARGE GRIDS ARE NEAT!</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">
    <style>
      .border-red{ border: 1px solid red }
      .border-orange{ border: 1px solid orange }
      .border-yellow{ border: 1px solid yellow }
      .border-green{ border: 1px solid green }
      .border-blue{ border: 1px solid blue }
      .border-indigo{ border: 1px solid indigo } 
      .border-violet{ border: 1px solid violet }

      .container1{ background-color: gray }
      .container2{ background-color: lightGray }
      .container3{ background-color: DimGray }
      .container4{ background-color: SlateGray }
      .container5{ background-color: silver }

    </style>
  </head>
  <body >
    <div class='container container1'>
      <div class='col col-xl-12 border-red'> I am a column that takes up the entire screen because I have 12 columns </div>
    </div>
    <div class='container container2'>
      <div class='col col-lg-6 border-orange'>We take up only half the screen because we've got '6' columns </div>
      <div class='col col-lg-6 border-yellow'>We take up only half the screen because we've got '6' columns</div>
    </div>
    <div class='container container3'>
      <div class='col col-lg-4 border-green'> We take up 4 columns! </div>
      <div class='col col-lg-4 border-blue'> There are 3 of us! </div>
      <div class='col col-lg-4 border-indigo'> and you know, that 3 * 4 = 12! </div>
    </div>
    <div class='container container4'>
      <div class='col col-lg-3 border-violet'>The four of us take 3 columns each</div>
      <div class='col col-lg-3 border-red'> It's pretty cool if you ask me</div>
      <div class='col col-lg-3 border-yellow'>We can fit some neat things here</div>
      <div class='col col-lg-3 border-green'> Just gotta make sure we all add up to 12! (also, notice how I extend below the others?) </div>
    </div>
    <div class='container container5'>
      <div class='col col-lg-2 border-blue'>We all take up 2!</div>
      <div class='col col-lg-2 border-indigo'>We're very small </div>
      <div class='col col-lg-2 border-violet'> Not as small as 1s!</div>
      <div class='col col-lg-2 border-red'>but still pretty dang small</div>
      <div class='col col-lg-2 border-orange'>But at least there are 6 </div>
      <div class='col col-lg-2 border-yellow'>of us :D </div>
      <div class='col col-lg-1 border-green'>We </div>
      <div class='col col-lg-1 border-blue'> are</div>
      <div class='col col-lg-1 border-indigo'> all </div>
      <div class='col col-lg-1 border-violet'> only </div>
      <div class='col col-lg-1 border-red'> one </div>
      <div class='col col-lg-1 border-orange'> column </div>
      <div class='col col-lg-1 border-yellow'> wide</div>
      <div class='col col-lg-1 border-green'> but </div>
      <div class='col col-lg-1 border-blue'> there's </div>
      <div class='col col-lg-1 border-indigo'> a lot </div>
      <div class='col col-lg-1 border-violet'> of </div>
      <div class='col col-lg-1 border-red'> us!</div>                        
    </div>
    </div>
  </body>
</html>
```



[Now let's try it with half `col-lg-#` and half `col-md-#`:](https://codepen.io/bdpastl/pen/dLNgBp?editors=1000) 

```html
<!doctype html>
<html>
  <head> 
    <title>LARGE GRIDS ARE NEAT!</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">
    <style>
      .border-red{ border: 1px solid red }
      .border-orange{ border: 1px solid orange }
      .border-yellow{ border: 1px solid yellow }
      .border-green{ border: 1px solid green }
      .border-blue{ border: 1px solid blue }
      .border-indigo{ border: 1px solid indigo } 
      .border-violet{ border: 1px solid violet }

      .container1{ background-color: gray }
      .container2{ background-color: lightGray }
      .container3{ background-color: DimGray }
      .container4{ background-color: SlateGray }
      .container5{ background-color: silver }

    </style>
  </head>
  <body >
    <div class='container container1'>
      <div class='col col-md-12 border-red'> I am a column that takes up the entire screen because I have 12 columns </div>
    </div>
    <div class='container container2'>
      <div class='col col-md-6 border-orange'>We take up only half the screen because we've got '6' columns </div>
      <div class='col col-md-6 border-yellow'>We take up only half the screen because we've got '6' columns</div>
    </div>
    <div class='container container3'>
      <div class='col col-md-4 border-green'> We take up 4 columns! </div>
      <div class='col col-md-4 border-blue'> There are 3 of us! </div>
      <div class='col col-md-4 border-indigo'> and you know, that 3 * 4 = 12! </div>
    </div>
    <div class='container container4'>
      <div class='col col-md-3 border-violet'>The four of us take 3 columns each</div>
      <div class='col col-md-3 border-red'> It's pretty cool if you ask me</div>
      <div class='col col-md-3 border-yellow'>We can fit some neat things here</div>
      <div class='col col-md-3 border-green'> Just gotta make sure we all add up to 12! (also, notice how I extend below the others?) </div>
    </div>
    <div class='container container5'>
      <div class='col col-md-2 border-blue'>We all take up 2!</div>
      <div class='col col-md-2 border-indigo'>We're very small </div>
      <div class='col col-md-2 border-violet'> Not as small as 1s!</div>
      <div class='col col-md-2 border-red'>but still pretty dang small</div>
      <div class='col col-md-2 border-orange'>But at least there are 6 </div>
      <div class='col col-md-2 border-yellow'>of us :D </div>
      <div class='col col-md-1 border-green'>We </div>
      <div class='col col-md-1 border-blue'> are</div>
      <div class='col col-md-1 border-indigo'> all </div>
      <div class='col col-md-1 border-violet'> only </div>
      <div class='col col-md-1 border-red'> one </div>
      <div class='col col-md-1 border-orange'> column </div>
      <div class='col col-md-1 border-yellow'> wide</div>
      <div class='col col-md-1 border-green'> but </div>
      <div class='col col-md-1 border-blue'> there's </div>
      <div class='col col-md-1 border-indigo'> a lot </div>
      <div class='col col-md-1 border-violet'> of </div>
      <div class='col col-md-1 border-red'> us!</div>                        
    </div>
    </div>
  </body>
</html>
```



So you're probably wondering "what the heck is going on with this junk?", and initially this makes little to no sense, BUT this level of responsiveness lets us really good looking websites for both desktops, laptops, tablets, and smartphones!

We can do this by having our divs take in not just [one class for styling, but multiple!](https://codepen.io/bdpastl/pen/pBRxXq?editors=1000) 

```html
<!doctype html>
<html>
  <head> 
    <title>LARGE GRIDS ARE NEAT!</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">
    <style>
      .border-red{ border: 1px solid red }
      .border-orange{ border: 1px solid orange }
      .border-yellow{ border: 1px solid yellow }
      .border-green{ border: 1px solid green }
      .border-blue{ border: 1px solid blue }
      .border-indigo{ border: 1px solid indigo } 
      .border-violet{ border: 1px solid violet }

      .container1{ background-color: gray }
      .container2{ background-color: lightGray }


    </style>
  </head>
  <body >
    <div class='container container1'>
      <div class='col col-lg-2 col-md-2 border-blue'>We all take up 2!</div>
      <div class='col col-lg-2 col-md-2 border-indigo'>We're very small </div>
      <div class='col col-lg-2 col-md-2 border-violet'> Not as small as 1s!</div>
      <div class='col col-lg-2 col-md-2 border-red'>but still pretty dang small</div>
      <div class='col col-lg-2 col-md-2 border-orange'>But at least there are 6 </div>
      <div class='col col-lg-2 col-md-2 border-yellow'>of us :D </div>
    </div>
    <div class='container container2'> 
      <div class='col col-lg-1 col-md-2 border-green'>We </div>
      <div class='col col-lg-1 col-md-2 border-blue'> are</div>
      <div class='col col-lg-1 col-md-2 border-indigo'> all </div>
      <div class='col col-lg-1 col-md-2 border-violet'> only </div>
      <div class='col col-lg-1 col-md-2 border-red'> one </div>
      <div class='col col-lg-1 col-md-2 border-orange'> column </div>
      <div class='col col-lg-1 col-md-2 border-yellow'> wide</div>
      <div class='col col-lg-1 col-md-2 border-green'> but </div>
      <div class='col col-lg-1 col-md-2 border-blue'> there's </div>
      <div class='col col-lg-1 col-md-2 border-indigo'> a lot </div>
      <div class='col col-lg-1 col-md-2 border-violet'> of </div>
      <div class='col col-lg-1 col-md-2 border-red'> us!</div>                        
    </div>
    </div>
  </body>
</html>
```

What's happening above is that initially on a normal large screen, all of the columns take up only 2 in the top container, and all of the 12 in the bottom container take up 1. When our screen gets slightly smaller, (that is when it's no longer 'lg'), we shift all of our columns to being 2 wide (which keeps our top columns in place, but gives us 2 rows of the columns in the below container!

 [So let's make our site REALLY responsive:](https://codepen.io/bdpastl/pen/oOBaKL?editors=1000) 

```html
<!doctype html>
<html>
  <head> 
    <title>LARGE GRIDS ARE NEAT!</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">
    <style>
      .border-red{ border: 1px solid red }
      .border-orange{ border: 1px solid orange }
      .border-yellow{ border: 1px solid yellow }
      .border-green{ border: 1px solid green }
      .border-blue{ border: 1px solid blue }
      .border-indigo{ border: 1px solid indigo } 
      .border-violet{ border: 1px solid violet }

      .container1{ background-color: gray }
      .container2{ background-color: lightGray }


    </style>
  </head>
  <body >
    <div class='container container1'> 
      <div class='col col-lg-4 col-md-4 col-sm-6 col-xs-12 border-blue'>We all take up 2!</div>
      <div class='col col-lg-4 col-md-4 col-sm-6 col-xs-12 border-indigo'>We're very small </div>
      <div class='col col-lg-4 col-md-4 col-sm-6 col-xs-12 border-violet'> Not as small as 1s!</div>
      <div class='col col-lg-4 col-md-4 col-sm-6 col-xs-12 border-red'>but still pretty dang small</div>
      <div class='col col-lg-4 col-md-4 col-sm-6 col-xs-12 border-orange'>But at least there are 6 </div>
      <div class='col col-lg-4 col-md-4 col-sm-6 col-xs-12 border-orange'>of us!! </div>
    </div>
    <div class='container container2'> 
      <div class='col col-lg-1 col-md-2 col-sm-3 col-xs-4 border-green'>We </div>
      <div class='col col-lg-1 col-md-2 col-sm-3 col-xs-4 border-blue'> are</div>
      <div class='col col-lg-1 col-md-2 col-sm-3 col-xs-4 border-indigo'> all </div>
      <div class='col col-lg-1 col-md-2 col-sm-3 col-xs-4 border-violet'> only </div>
      <div class='col col-lg-1 col-md-2 col-sm-3 col-xs-4 border-red'> one </div>
      <div class='col col-lg-1 col-md-2 col-sm-3 col-xs-4 border-orange'> column </div>
      <div class='col col-lg-1 col-md-2 col-sm-3 col-xs-4 border-yellow'> wide</div>
      <div class='col col-lg-1 col-md-2 col-sm-3 col-xs-4 border-green'> but </div>
      <div class='col col-lg-1 col-md-2 col-sm-3 col-xs-4 border-blue'> there's </div>
      <div class='col col-lg-1 col-md-2 col-sm-3 col-xs-4 border-indigo'> a lot </div>
      <div class='col col-lg-1 col-md-2 col-sm-3 col-xs-4 border-violet'> of </div>
      <div class='col col-lg-1 col-md-2 col-sm-3 col-xs-4 border-red'> us!</div>              
    </div>
    </div>
  </body>
</html>
```

While what we've done may not look immediately pretty, this is exactly how many developers build their sites! One thing to note, see how we have so much written in our classes? It would be super wise to probably clean that up, and create css classes up in the styling section of our site! 

## Photo Blog V2

So, we've spent a while going over bootstrap, but let's take a moment and go refactor our photo-blog from last time! For reference, here's what it looked like at the end of the [last lesson (without using flexbox)](https://codepen.io/bdpastl/pen/OqKjvW): 

```html
<!doctype html>

    <html>
	<head>
		<style>
			div { float: left; padding: 20px; }
			img { width: 500px; height: 500px }
			.border{ border: 2px solid black; margin: 5px}

		</style>
	</head>
	<body>
        <h1> My Photo Blog: </h1>
        <hr />
		<div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/batwing.JPG' /></div>
		<div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/christmasTarantula.JPG' /></div>
		<div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/cicada.JPG' /></div>
		<div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/desertHairy.JPG' /></div>
		<div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/giantFlower.JPG' /></div>
		<div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/glassWing.JPG' /></div>
		<div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/greenJay.png' /></div>
		<div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/leafwing.JPG' /></div>
		<div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/lubber.JPG' /></div>
		<div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/luna.JPG' /></div>
		<div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/morphoScales.png' /></div>
		<div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/moth.JPG' /></div>
	</body>
 </html>

```

By using float, we had a pretty responsive webiste, but I bet we can do some really cool things with bootstrap! 

Let's start with adding a jumbotron inside of a container instead of just a header (also note that we added back in the javascript and jquery elements to our head): 

```html
<!doctype html>
<html>
  <head> 
    <title>Photo blog!</title>
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">

    <script  src="http://code.jquery.com/jquery-3.3.1.js"   integrity="sha256-2Kok7MbOyxpgUVvAk/HJ2jigOSYS2auK4Pfzbm7uH60="   crossorigin="anonymous"></script>


    <!-- Latest compiled and minified JavaScript -->
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js" integrity="sha384-aJ21OjlMXNL5UyIl/XNwTMqvzeRMZH2w8c5cRVpzpU8Y5bApTppSuUkhZXN0VxHd" crossorigin="anonymous"></script>

    <style>
      div { float: left; padding: 20px; }
      img { width: 500px; height: 500px }
      .border{ border: 2px solid black; margin: 5px}
    </style>

  </head>
  <body>
    <div class='container'>
      <div class='jumbotron'>
        <h1>
          My Photo Blog:
        </h1>
        <p>
          This is a place for me to show off my cool bug photos.
        </p>
      </div>  
    </div>

    <hr />
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/batwing.JPG' /></div>
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/christmasTarantula.JPG' /></div>
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/cicada.JPG' /></div>
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/desertHairy.JPG' /></div>
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/giantFlower.JPG' /></div>
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/glassWing.JPG' /></div>
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/greenJay.png' /></div>
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/leafwing.JPG' /></div>
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/lubber.JPG' /></div>
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/luna.JPG' /></div>
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/morphoScales.png' /></div>
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/moth.JPG' /></div>
  </body>
</html>


```

Something's wrong, right? That's because our `<style>` section is overwriting our bootstrap! Try removing the ` div { float: left; padding: 20px; }`. It'll look a little weird for now, but just bear with the changes! 

[Now let's add in our navbar from before](https://codepen.io/bdpastl/pen/ZZBmPL) (not the bootsrap navbar from their site, but the navbar we had built!): 

```html
<!doctype html>
<html>
  <head> 
    <title>Photo Blog!</title>
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">

    <script  src="http://code.jquery.com/jquery-3.3.1.js"   integrity="sha256-2Kok7MbOyxpgUVvAk/HJ2jigOSYS2auK4Pfzbm7uH60="   crossorigin="anonymous"></script>


    <!-- Latest compiled and minified JavaScript -->
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js" integrity="sha384-aJ21OjlMXNL5UyIl/XNwTMqvzeRMZH2w8c5cRVpzpU8Y5bApTppSuUkhZXN0VxHd" crossorigin="anonymous"></script>

    <style>
      img { width: 500px; height: 500px }
      .border{ border: 2px solid black; margin: 5px}
    </style>

  </head>
  <body>
    <nav class='navbar navbar-default'>
      <div class='container'>
        <div class='navbar-header' style='background-color:#f1f1f1'>
          <a href='#' class='navbar-brand'>My Name</a>
        </div>

        <ul class='nav navbar-nav'>
          <li> <a href='#'> Photo Gallery </a></li>
          <li> <a href='#'> Blog </a></li>
        </ul>

        <ul class='nav navbar-nav navbar-right'>
          <li> <a href='#'> About Me </a></li>
          <li> <a href='#'> Code Portfolio </a></li>
          <li> <a href='#'> Contact </a></li>
        </ul>
      </div>
    </nav>
    <div class='container'>
      <div class='jumbotron'>
        <h1>
          My Photo Blog:
        </h1>
        <p>
          This is a place for me to show off my cool bug photos.
        </p>
      </div>  
    </div>

    <hr />
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/batwing.JPG' /></div>
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/christmasTarantula.JPG' /></div>
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/cicada.JPG' /></div>
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/desertHairy.JPG' /></div>
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/giantFlower.JPG' /></div>
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/glassWing.JPG' /></div>
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/greenJay.png' /></div>
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/leafwing.JPG' /></div>
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/lubber.JPG' /></div>
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/luna.JPG' /></div>
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/morphoScales.png' /></div>
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/moth.JPG' /></div>
  </body>
</html>
```

Now our site has a cool navbar up top AND a jumbotron showing off our blog's name! 

So, we learned about the grid system before. Let's try to make a site where we have 3 images going across in rows. First we want to wrap our images in a `<div class='container'>` AND make sure that we add a `class='col col-lg-4'` to our [divs wrapping our images](https://codepen.io/bdpastl/pen/xeRmxW): 

```html
<!doctype html>
<html>
  <head> 
    <title>Photo blog!</title>
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">

    <script  src="http://code.jquery.com/jquery-3.3.1.js"   integrity="sha256-2Kok7MbOyxpgUVvAk/HJ2jigOSYS2auK4Pfzbm7uH60="   crossorigin="anonymous"></script>


    <!-- Latest compiled and minified JavaScript -->
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js" integrity="sha384-aJ21OjlMXNL5UyIl/XNwTMqvzeRMZH2w8c5cRVpzpU8Y5bApTppSuUkhZXN0VxHd" crossorigin="anonymous"></script>

    <style>
      img { width: 500px; height: 500px }
      .border{ border: 2px solid black; margin: 5px}
    </style>

  </head>
  <body>
    <nav class='navbar navbar-default'>
      <div class='container'>
        <div class='navbar-header' style='background-color:#f1f1f1'>
          <a href='#' class='navbar-brand'>My Name</a>
        </div>

        <ul class='nav navbar-nav'>
          <li> <a href='#'> Photo Gallery </a></li>
          <li> <a href='#'> Blog </a></li>
        </ul>

        <ul class='nav navbar-nav navbar-right'>
          <li> <a href='#'> About Me </a></li>
          <li> <a href='#'> Code Portfolio </a></li>
          <li> <a href='#'> Contact </a></li>
        </ul>
      </div>
    </nav>
    <div class='container'>
      <div class='jumbotron'>
        <h1>
          My Photo Blog:
        </h1>
        <h4>
          This is a place for me to show off my photos.
        </h4>
      </div>
      <hr />
      <div class='container'>
        <div class='col col-lg-4'><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/batwing.JPG' /></div>
        <div class='col col-lg-4'><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/christmasTarantula.JPG' /></div>
        <div class='col col-lg-4'><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/cicada.JPG' /></div>
        <div class='col col-lg-4'><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/desertHairy.JPG' /></div>
        <div class='col col-lg-4'><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/giantFlower.JPG' /></div>
        <div class='col col-lg-4'><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/glassWing.JPG' /></div>
        <div class='col col-lg-4'><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/greenJay.png' /></div>
        <div class='col col-lg-4'><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/leafwing.JPG' /></div>
        <div class='col col-lg-4'><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/lubber.JPG' /></div>
        <div class='col col-lg-4'><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/luna.JPG' /></div>
        <div class='col col-lg-4'><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/morphoScales.png' /></div>
        <div class='col col-lg-4'><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/moth.JPG' /></div>
      </div>
    </div>
  </body>
</html>
```

At this point, we have our images being somewhat responsive, but it looks like they're being overlapped. What can we do about that? This is where we can wrap our images in a `<div class='thumbnail'>`. This will give us the entire photo inside the [div scaled properly](https://codepen.io/bdpastl/pen/vMyvKM)! 

```html
<!doctype html>
<html>
  <head> 
    <title>Photo Blog!</title>
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">

    <script  src="http://code.jquery.com/jquery-3.3.1.js"   integrity="sha256-2Kok7MbOyxpgUVvAk/HJ2jigOSYS2auK4Pfzbm7uH60="   crossorigin="anonymous"></script>


    <!-- Latest compiled and minified JavaScript -->
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js" integrity="sha384-aJ21OjlMXNL5UyIl/XNwTMqvzeRMZH2w8c5cRVpzpU8Y5bApTppSuUkhZXN0VxHd" crossorigin="anonymous"></script>

    <style>
      img { width: 500px; height: 500px }
      .border{ border: 2px solid black; margin: 5px}
    </style>

  </head>
  <body>
    <nav class='navbar navbar-default'>
      <div class='container'>
        <div class='navbar-header' style='background-color:#f1f1f1'>
          <a href='#' class='navbar-brand'>My Name</a>
        </div>

        <ul class='nav navbar-nav'>
          <li> <a href='#'> Photo Gallery </a></li>
          <li> <a href='#'> Blog </a></li>
        </ul>

        <ul class='nav navbar-nav navbar-right'>
          <li> <a href='#'> About Me </a></li>
          <li> <a href='#'> Code Portfolio </a></li>
          <li> <a href='#'> Contact </a></li>
        </ul>
      </div>
    </nav>
    <div class='container'>
      <div class='jumbotron'>
        <h1>
          My Photo Blog:
        </h1>
        <h4>
          This is a place for me to show off my photos.
        </h4>
      </div>
      <hr />
      <div class='container'>
        <div class='col col-lg-4'>
          <div class='thumbnail'>
            <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/batwing.JPG' />
          </div>
        </div>
        <div class='col col-lg-4'>
          <div class='thumbnail'>
            <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/christmasTarantula.JPG' />
          </div>
        </div>
        <div class='col col-lg-4'>
          <div class='thumbnail'>
            <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/cicada.JPG' />
          </div>
        </div>
        <div class='col col-lg-4'>
          <div class='thumbnail'>
            <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/desertHairy.JPG' />
          </div>
        </div>
        <div class='col col-lg-4'>
          <div class='thumbnail'>
            <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/giantFlower.JPG' />
          </div>
        </div>
        <div class='col col-lg-4'>
          <div class='thumbnail'>
          <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/glassWing.JPG' />
          </div>
        </div>
        <div class='col col-lg-4'>
          <div class='thumbnail'>
          <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/greenJay.png' />
          </div>
        </div>
        <div class='col col-lg-4'>
          <div class='thumbnail'>
          <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/leafwing.JPG' />
          </div>
        </div>
        <div class='col col-lg-4'>
          <div class='thumbnail'>
          <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/lubber.JPG' />
          </div>
        </div>
        <div class='col col-lg-4'>
          <div class='thumbnail'>
          <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/luna.JPG' />
          </div>
        </div>
        <div class='col col-lg-4'>
          <div class='thumbnail'>
            <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/morphoScales.png' />
          </div>
        </div>
        <div class='col col-lg-4'>
          <div class='thumbnail'>
            <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/moth.JPG' /></div>
        </div>
      </div>
    </div>
  </body>
</html>
```

Now we've got all of our images looking super good - but try rescaling! Once our screen gets a little smaller, we just get one image per line. That's boring! We want our blog to scale from 3 down to 2 down to 1 image per row! Mostly just to look fancy, but hey! Fancy sites are cool!  

So, remember back from grids that we can use `col col-md-#` to determine the size of what a div will be when we scale our screen to a medium size? Let's try `col col-md-6` [so that we'll get two images per row](https://codepen.io/bdpastl/pen/KYNbQq): 

```html
<!doctype html>
<html>
  <head> 
    <title>Photo Blog!</title>
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">

    <script  src="http://code.jquery.com/jquery-3.3.1.js"   integrity="sha256-2Kok7MbOyxpgUVvAk/HJ2jigOSYS2auK4Pfzbm7uH60="   crossorigin="anonymous"></script>


    <!-- Latest compiled and minified JavaScript -->
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js" integrity="sha384-aJ21OjlMXNL5UyIl/XNwTMqvzeRMZH2w8c5cRVpzpU8Y5bApTppSuUkhZXN0VxHd" crossorigin="anonymous"></script>

    <style>
      img { width: 500px; height: 500px }
      .border{ border: 2px solid black; margin: 5px}
    </style>

  </head>
  <body>
    <nav class='navbar navbar-default'>
      <div class='container'>
        <div class='navbar-header' style='background-color:#f1f1f1'>
          <a href='#' class='navbar-brand'>My Name</a>
        </div>

        <ul class='nav navbar-nav'>
          <li> <a href='#'> Photo Gallery </a></li>
          <li> <a href='#'> Blog </a></li>
        </ul>

        <ul class='nav navbar-nav navbar-right'>
          <li> <a href='#'> About Me </a></li>
          <li> <a href='#'> Code Portfolio </a></li>
          <li> <a href='#'> Contact </a></li>
        </ul>
      </div>
    </nav>
    <div class='container'>
      <div class='jumbotron'>
        <h1>
          My Photo Blog:
        </h1>
        <h4>
          This is a place for me to show off my photos.
        </h4>
      </div>
      <hr />
      <div class='container'>
        <div class='col col-lg-4 col-md-6'>
          <div class='thumbnail'>
            <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/batwing.JPG' />
          </div>
        </div>
        <div class='col col-lg-4 col-md-6'>
          <div class='thumbnail'>
            <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/christmasTarantula.JPG' />
          </div>
        </div>
        <div class='col col-lg-4 col-md-6'>
          <div class='thumbnail'>
            <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/cicada.JPG' />
          </div>
        </div>
        <div class='col col-lg-4 col-md-6'>
          <div class='thumbnail'>
            <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/desertHairy.JPG' />
          </div>
        </div>
        <div class='col col-lg-4 col-md-6'>
          <div class='thumbnail'>
            <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/giantFlower.JPG' />
          </div>
        </div>
        <div class='col col-lg-4 col-md-6'>
          <div class='thumbnail'>
          <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/glassWing.JPG' />
          </div>
        </div>
        <div class='col col-lg-4 col-md-6'>
          <div class='thumbnail'>
          <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/greenJay.png' />
          </div>
        </div>
        <div class='col col-lg-4 col-md-6'>
          <div class='thumbnail'>
          <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/leafwing.JPG' />
          </div>
        </div>
        <div class='col col-lg-4 col-md-6'>
          <div class='thumbnail'>
          <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/lubber.JPG' />
          </div>
        </div>
        <div class='col col-lg-4 col-md-6'>
          <div class='thumbnail'>
          <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/luna.JPG' />
          </div>
        </div>
        <div class='col col-lg-4 col-md-6'>
          <div class='thumbnail'>
            <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/morphoScales.png' />
          </div>
        </div>
        <div class='col col-lg-4 col-md-6'>
          <div class='thumbnail'>
            <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/moth.JPG' /></div>
        </div>
      </div>
    </div>
  </body>
</html>
```

So, that's great and all, but when our screens get small, it still doesn't look that good. Let's try changing `col-md-6` to `col-sm-6`. [Let's see how that works:](https://codepen.io/bdpastl/pen/qwqLYg)

```html
<!doctype html>
<html>
  <head> 
    <title>Photo Blog!</title>
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">

    <script  src="http://code.jquery.com/jquery-3.3.1.js"   integrity="sha256-2Kok7MbOyxpgUVvAk/HJ2jigOSYS2auK4Pfzbm7uH60="   crossorigin="anonymous"></script>


    <!-- Latest compiled and minified JavaScript -->
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js" integrity="sha384-aJ21OjlMXNL5UyIl/XNwTMqvzeRMZH2w8c5cRVpzpU8Y5bApTppSuUkhZXN0VxHd" crossorigin="anonymous"></script>

    <style>
      img { width: 500px; height: 500px }
      .border{ border: 2px solid black; margin: 5px}
    </style>

  </head>
  <body>
    <nav class='navbar navbar-default'>
      <div class='container'>
        <div class='navbar-header' style='background-color:#f1f1f1'>
          <a href='#' class='navbar-brand'>My Name</a>
        </div>

        <ul class='nav navbar-nav'>
          <li> <a href='#'> Photo Gallery </a></li>
          <li> <a href='#'> Blog </a></li>
        </ul>

        <ul class='nav navbar-nav navbar-right'>
          <li> <a href='#'> About Me </a></li>
          <li> <a href='#'> Code Portfolio </a></li>
          <li> <a href='#'> Contact </a></li>
        </ul>
      </div>
    </nav>
    <div class='container'>
      <div class='jumbotron'>
        <h1>
          My Photo Blog:
        </h1>
        <h4>
          This is a place for me to show off my photos.
        </h4>
      </div>
      <hr />
      <div class='container'>
        <div class='col col-lg-4 col-sm-6'>
          <div class='thumbnail'>
            <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/batwing.JPG' />
          </div>
        </div>
        <div class='col col-lg-4 col-sm-6'>
          <div class='thumbnail'>
            <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/christmasTarantula.JPG' />
          </div>
        </div>
        <div class='col col-lg-4 col-sm-6'>
          <div class='thumbnail'>
            <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/cicada.JPG' />
          </div>
        </div>
        <div class='col col-lg-4 col-sm-6'>
          <div class='thumbnail'>
            <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/desertHairy.JPG' />
          </div>
        </div>
        <div class='col col-lg-4 col-sm-6'>
          <div class='thumbnail'>
            <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/giantFlower.JPG' />
          </div>
        </div>
        <div class='col col-lg-4 col-sm-6'>
          <div class='thumbnail'>
          <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/glassWing.JPG' />
          </div>
        </div>
        <div class='col col-lg-4 col-sm-6'>
          <div class='thumbnail'>
          <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/greenJay.png' />
          </div>
        </div>
        <div class='col col-lg-4 col-sm-6'>
          <div class='thumbnail'>
          <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/leafwing.JPG' />
          </div>
        </div>
        <div class='col col-lg-4 col-sm-6'>
          <div class='thumbnail'>
          <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/lubber.JPG' />
          </div>
        </div>
        <div class='col col-lg-4 col-sm-6'>
          <div class='thumbnail'>
          <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/luna.JPG' />
          </div>
        </div>
        <div class='col col-lg-4 col-sm-6'>
          <div class='thumbnail'>
            <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/morphoScales.png' />
          </div>
        </div>
        <div class='col col-lg-4 col-sm-6'>
          <div class='thumbnail'>
            <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/moth.JPG' /></div>
        </div>
      </div>
    </div>
  </body>
</html>
```



One final note on our photoblog's grid system, have you noticed that the borders around the image get kind of weird when you're rescaling? That's because we still have our styles up in the header. Try deleting those to see what happens! 



