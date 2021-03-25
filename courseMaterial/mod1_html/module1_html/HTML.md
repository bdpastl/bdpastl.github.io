# Welcome!

In this class we'll be learning about HTML, CSS, Javascript, and Bootstrap! Over the course of the next few weeks, you'll go from making very simple, introductory websites, to eventually making your own content rich websites.  If we have time, we'll be able to eventually develop our own dynamic websites!

[TOC]

## What you will need:

- A computer

- A [CodeHS](https://codehs.com/) Account.
  - If you haven't already, [**Please create an account here**](https://codehs.com/go/9854E). If you don't have a school-issued email address, you can use your personal email address.
  - Enter **9854E** as the Class Code.

- [Slack](https://slack.com/)
  - Slack is a web-app (and a downloadable app) that allows for us to converse quickly and easily (and to share code quickly). You should have received an email to join our slack, but if not, please let us know!
  - Students can use Slack to ask instructors questions outside of class. Feel free to post a message in the [**#introweb**](https://bdpastl.slack.com/archives/C012DUTGPJL) slack channel.

Now, onto the fun stuff:


## Getting Started - What is the Web?

### The Internet

[The internet is a system of computer networks that are all connected](https://i.imgur.com/9Sqim7F.png). Originally used by the US Military and Academic Universities, the internet has changed the way the world shares news, information, and ideas. The internet allows your Computer, phone, iPad, etc, to connect to servers located all over the world.

The internet has revolutionized the way the world communicates, does business, and shares information.You can upload and download files from the internet. When you watch a movie on Netflix, you're on the internet! When you play a video game over XBox Live, you're on the internet! If you're reading this webpage, you're on the internet! Your parents might even use the internet to check their bank account and do work.

Most people connect to the internet via their Internet Service Provider, also known as an "ISP". Your ISP could be a mobile telecommunication company - like Sprint or T-Mobile, a cable company - like Spectrum, or even a dial-up internet company, like AOL.

### Web Browsers

A web browser is an app which runs on your Computer or mobile device which allows you to access websites on the internet. Some example web browsers are:

- Chrome
- Firefox
- Safari
- Internet Explorer
- Edge

### Web Development

Web development is the process of designing and creating a Website for the internet. Websites can be simple pages with text, images, and links:

- [BDPA STL](https://bdpastl.github.io/)
- [UK Government](https://www.gov.uk/)
- [The First Website ever made!](http://info.cern.ch/hypertext/WWW/TheProject.html)

 Website can also be complicated, dynamic pages where content is streamed, uploaded, and always changing:

- [Youtube](https://youtube.com)
- [Twitter](https://twitter.com)
- [Google](https://google.com)

### How do we create Websites?

With code! Specifically, websites are usually created with languages such as: [HTML](https://en.wikipedia.org/wiki/HTML), [CSS](https://en.wikipedia.org/wiki/CSS), and [Javascript](https://en.wikipedia.org/wiki/JavaScript). We will be spending most of our time learning HTML and CSS, as they are the most basic building blocks to build any website, and will provide a solid foundation to go on and build more complicated software systems.



## HTML - Structuring Websites:

HTML (Hyper Text Markup Language) is the primary way of creating static webpages. When you think of coding, you probably don't think of HTML in the same way you think of a more complex language like javascript. Markup languages are langauges that help us render documents! HTML helps us render documents with elements and attributes (and a whole lot more).  Our web browsers download the HTML code, and render the code on our own computers! We'll be going from the very basics of HTML all the way to the newest version: HTML 5 in the coming couple weeks!

You may have noticed that at the beginning of our HTML code, we have:

```html
<!doctype html>
```

`<!doctype html>` is not an element! It is something for our web browser to read to know that we're rendering an HTML page!

### Elements (aka Tags):

You can boil almost all of HTML down to elements (sometimes called tags) and attributes! Elements are any html code that we call with angled brackets:

```html
<h1>the word 'h1' surrounded by angled brackets is a type of element!</h1>
```

Elements have a very special syntax (i.e. they're written in a very special way):

| All elements start with `<element-name>` | All elements end with ` </element-name>` |       Most elements have their own special functions!        |
| :--------------------------------------: | :--------------------------------------: | :----------------------------------------------------------: |
|                 `<html>`                 |                `</html>`                 |   **HTML** elements are where we put all of the HTML code    |
|                 `<head>`                 |                `</head>`                 | This is where we put special 'header' elements, like page titles, styles, scripts, etc. The **head** is where the site's brains live |
|                 `<body>`                 |                `</body>`                 | The **body** is where we put the content that renders on the page! |
|                 `<div>`                  |                 `</div>`                 | This is a **div** element, which is kind of a catch-all block element (which we'll talk about more) |
|                  `<p>`                   |                  `</p>`                  | **Paragraph** elements where a lot of people put their text content! |
|                  `<a>`                   |                  `</a>`                  | **Anchor** elements are where we place our links (both internal and external)! |



You've already seen that some elements don't follow the rules, that's because we don't really need to put text between the opening and closing tags:

| Empty HTML Elements |      Empty HTML Elements Have Their Functionality Too!       |
| :-----------------: | :----------------------------------------------------------: |
|      `<br />`       | When you write HTML, if you need to write a new line without creaing a whole new section, use this **break**. |
|      `<hr />`       | Sometimes you want a break. **Horizontal rule** will create a nice little line on the page. |
|      `<img />`      | The internet would be an extremely boring place without pictures! This **image** tag lets us place images on our page! |
|     `<link />`      | You saw the anchor element up above, that's used a lot for internal links. The **link** element is often used for external links (like say if you wanted to send somebody to google!) |



These are just a small handful of the elements we'll be using throughout the coming weeks!

And remember **ALWAYS CLOSE YOUR ELEMENTS**

Now that you've seen all the elements, let's get a look at what an HTML page looks like! Below is the most basic html page you'll ever come across:



Play with this code [here](https://codepen.io/bdpastl/pen/oVpRPK):

```html
<!doctype html>
<html>
  <head>
  </head>
  <body>
    Hello World!
  </body>
</html>
```

While you're playing with the code, try placing text in the head!



### Block Elements:

When we write HTML, we'll be using a lot of block elements. A **block element** is an element that takes up as much possible space as it can from left to right! There are a lot of ways to get around this, but for now, let's take a look:

[Take a look here](https://codepen.io/bdpastl/pen/PLBKQm) to see how these take up the whole page (note: CSS on codepen for example purposes only):

```html
<!doctype html>
<html>
  <head>
  </head>
  <body>
    <div>
      I'm a div! I take up as much room as possible!
    </div>
    <p>
      Me too! As a paragraph, I'm a pretty big deal.
    </p>
    <hr />
  </body>
</html>
```



### Paragraphs and Divs

Keeping Content together is a big part of writing your site! Both paragraphs and divs are meant to be containers. Both `<p>` and `<div>`  put a space after themselves. Like paragraphs in books, we want to keep them separated. The only major difference between them is that people often use `<div>` as a catchall and write special classes for it in CSS, which we'll get to soon!

To see how these work, take a look  [at the *lorem ipsum* placeholder text](https://codepen.io/bdpastl/pen/MxBvLL):

  ```html
<!doctype html>
<html>
  <head>
  </head>
  <body>
    <div>
				Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor 			incididunt ut labore et dolore magna aliqua.


      Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
    </div>
    <p>
Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum</p>
    <hr />
  </body>
</html>
  ```

Did you notice that when the code was rendered, the second line of our `<div>` didn't actually show up as a second line? That's because no matter how many line breaks we enter on our keyboard, HTML will not render a line break. For that we need to add a `<br />`. [Check it out](https://codepen.io/bdpastl/pen/qvyXGb):

```html
<!doctype html>
<html>
  <head>
  </head>
  <body>
    <div>
				Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor 			incididunt ut labore et dolore magna aliqua.
      <br />
      Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
    </div>
    <p>
Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum</p>
    <hr />
  </body>
</html>
```

The `<br />` gives us a new line!

Now that you've seen *lorem ipsum* it won't look so weird once you come across it again. It's really just placeholder text.



#### Text Formatting

Now that you know how to write the most common tags in HTML, you should probably get comfortable with using special tags that aren't block elements in order to format our text! When we format our HTML, we want it to ultimately look just like any other text that you'd make in MS Word, but the downside is that we can't just highlight out text and press `ctrl` + `c`.



##### Bold Lettering:

To **boldly** letter something in our code, we need to use the `<strong>` or the `<b>` elements. They both look the exact same to us, but for screen readers for visually impaired people `<strong>` shows a little bit less emphasis. [Take a look and how this code renders:](https://codepen.io/bdpastl/pen/drjZPK)

```html
<!doctype html>
<html>
  <head>
  </head>
  <body>
    <div>
			Sometimes when you want some text to be bolder than other text, you can use the <b>bold</b> or <strong>strong</strong> tags!
    </div>
  </body>
</html>
```



#### Italic Lettering:

Just like using bold and strong on words looks the same, but actually acts different, *the same thing goes for italics!* `<i>` and `<em>` both look like italics, but `<i>` shows greater emphasis to a screen reader than does `<em>`. [Take a look at the code](https://codepen.io/bdpastl/pen/KEByzz):

```html
<!doctype html>
<html>
  <head>
  </head>
  <body>
    <div>
      I make some pretty bad jokes sometimes, so I need to <i>italicize</i> and <em>emphasize</em> my words a lot so people know I'm telling a joke!!
    </div>
  </body>
</html>
```



#### Underlining

Sometimes bold and italics don't get the point across as much as we'd want, <u>that's when we'd want to start underlining our text!</u> To do this, we use the `<u>` element. This Underlines all text betwen the `<u>` <u>and</u> `</u>`. [Check out how underlining works](https://codepen.io/bdpastl/pen/GeBOrL):

```html
<!doctype html>
<html>
  <head>
  </head>
  <body>
    <div>
      <u>I FEEL EXTREMELY IMPORTANT</u>!!

      <div> Also, you <b>might</b> think we're crazy but you can <b><i><u>ADD ALL THREE TOGETHER</u></i></b></div>
    </div>
  </body>
</html>
```



#### Superscripts and Subscripts

Suppose you wanted to properly format some math on your site? You can do that with superscripts `<sup>` and subscripts `<sub>`! [Look at that beautiful math](https://codepen.io/bdpastl/pen/VRBrMq?editors=1000):

```html
<!doctype html>
<html>
  <head>
  </head>
  <body>
    <div> MATH IS NEAT! </div>
    <div> E = MC<sup>2</sup></div>
    <div> Later, when we work with lists and arrays, you can denote a sub-element by writing array<sub>n</sub> where `n` is the element number!</div>
  </body>
</html>
```



#### Code and Preformat

We're getting pretty thick in the weeds for formatting, so this is it for the time being. The last two we have are for when we want to display 'code' or 'preformatted' text! **Code** `<code>` will render our font to look more like a monspaced text, and **preformat** `<pre>` will render our text with the spaces and new lines EXACTLY as we left them! The main difference is that `<pre>` is a block element that makes its own section, while `<code>` is an inline element, like all of the previous formatters. [Check out how it renders](https://codepen.io/bdpastl/pen/OqwOZP?editors=1000):

```html
<!doctype html>
<html>
  <head>
  </head>
  <body>
    <div> When we want to talk about a certain <code>line of code</code> in our HTML, we can use the code element!</div>
    <div> If we have a whole giant block of code with special spacing,
      	<pre> we can
      									use preformatted
     text
       with
         pre < </div>
  </body>
</html>
```





### Headers

Paragraphs and divs are great and all, but how should we title them? Luckily, we can do that with our header elements! Headers range in size from `<h1>` to `<h6>`. Our H1 headers are the biggest. [Take a gander](https://codepen.io/bdpastl/pen/pYZWvY):

```html
<!doctype html>
<html>
  <head>
  </head>
  <body>
    <h1> H1. Welcome to my site! </h1>
    <h2> H2. This is where I can introduce you to myself </h2>
    <h3> H3. I really like to write code </h3>
    <h4> H4. I also really like to take pictures of bugs </h4>
    <h5> H5. It would be super neat if I could make a photo blog for all of my bug pictures </h5>
    <h6> H6. Maybe once we learn how to include images into our site we can start posting bug pictures? </h6>
    <div>
       I'm normal sized text, by the way. Just for reference.
    </div>
  </body>
</html>
```

Headers get consecutively smaller as the numbers go! Be sure not to go too small, or you might end up with a header smaller than your actual text!



### Links

Anchor elements `<a>` can use an `href` to point to a link!  Why don't you [click on THIS link](https://codepen.io/bdpastl/pen/EMeWqq)!

```html
<!doctype html>
<html>
  <head>
  </head>
  <body style='background-color:lightblue'>
    <h1 style='border-left: 1px solid blue; padding: 10px'> The internet is a series of links! </h1>
		<hr />
   <div>
         Sometimes you'll want to link to a new site, or a new page! <a href='https://bdpastl.github.io'>I am a link! Please click me</a>. By including links in your site, you can create a create a very dynamic experience!
    </div>

  </body>
</html>
```



You can also link to other portions of your page (but since our pages aren't big enough, we're not going to tackle this yet) by using the anchor tag with an ID:



```html
<!doctype html>
<html>
  <head>
  </head>
  <body style='background-color:lightblue'>
    <h1 style='border-left: 1px solid blue; padding: 10px'> The internet is a series of links! </h1>
		<hr />
   <div>
        Suppose I wanted to make sure somebody could navigate right to a spot on my page! I could then write an anchor with the attribute <a id='comeToMe'> to come directly to this spot</a>.
    </div>

    <div>
      On a completely different spot on the same page, we can create a navigation href by saying <a href='#comeToMe'>click here to go to the other spot!</a>
    </div>

  </body>
</html>
```

It's good to know that we can do this. Once our sites are large enough, we'll be able to navigate internally!



### Images

When you need to source a link (to either an image or to a new site), you need to use the src attribute! The `<img />` element needs attributes! Especially since there's no real text we want to have inside of our image. There are multiple ways to upload an image to your site, but for now, let's just grab a link. We need to place the link as a value for the source attribute, like below! [See the code in action!](https://codepen.io/bdpastl/pen/OqomzZ)

```html
<!doctype html>
<html>
  <head>
  </head>
  <body style='background-color:lightblue'>
    <h1 style='border-left: 1px solid blue; padding: 10px'> Images are some of the best parts of the internet! </h1>
		<hr />
   	<div>
       Check out this beautiful image of my old pet, Rosie!
        <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/christmasTarantula.JPG' />
    </div>

  </body>
</html>
```

Now the width of my old photo is pretty big… Photos often have differing sizes, so we often need to scale them ourselves! [Check it out:](https://codepen.io/bdpastl/pen/qvMmoq)

```html
<!doctype html>
<html>
  <head>
  </head>
  <body style='background-color:lightblue'>
    <h1 style='border-left: 1px solid blue; padding: 10px'> Images are some of the best parts of the internet! </h1>
		<hr />
   	<div>
       Check out this beautiful image of my old pet, Rosie!
        <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/christmasTarantula.JPG' style='width:500; height:500' />
    </div>

  </body>
</html>
```



### Lists:

So, we just listed all of those really cool things we want to do above! How would we actually write a list of things we like on our about me pages? How about a list?

#### Unordered Lists:

Unordered Lists are bulleted lists. This is where we will introduce the concept of an **attribute** (don't worry, we'll go into a lot more detail later). Attributes let us futher customize our code!

[Take a look at this default unordered list](https://codepen.io/bdpastl/pen/YgjrVr):

```html
<!doctype html>
<html>
  <head>
  </head>
  <body>
    <h1> Welcome to my site! </h1>
    <hr />
     <ul>
       <li>I really like to write code</li>
       <li>I also really like to take pictures of bugs</li>
       <li>It would be super neat if I could make a photo blog for all of my bug pictures !</li>
       <li>Maybe once we learn how to include images into our site we can start posting bug pictures?</li>
     </ul>
  </body>
</html>
```

By using attributes, we can start changing things up in our lists (we'll go into how attributes work in detail after this section!):

Check out [how these attributes change the list](https://codepen.io/bdpastl/pen/gEjGGK):

```html
<!doctype html>
<html>
  <head>
  </head>
  <body>
    <h1> Welcome to my site! </h1>
    <hr />
     <ul>
       <li type='square'>I really like to write code</li>
       <li type='square'>Does that make me a square?</li>
       <li type='square'>Some people do call me a block head...</li>
       <li type='square'>Maybe they're just not seeing me at the right ANGLE?</li>
     </ul>
  </body>
</html>
```

We can do what we did above, but, that's a lot of work to write `type='square'` on each single list item `<li>`. What we can do instead, is write it on top, at the unordered list `<ul>` level, and the `type='square'` will fall through down to the list items. Check out [how much easier that was to write](https://codepen.io/bdpastl/pen/drjVJV?editors=1100):

```html
<!doctype html>
<html>
  <head>
  </head>
  <body>
    <h1> Welcome to my site! </h1>
    <hr />
     <ul type='square'>
       <li>I really like to write code</li>
       <li>Does that make me a square?</li>
       <li>Some people do call me a block head...</li>
       <li>Maybe they're just not seeing me at the right ANGLE?</li>
     </ul>
  </body>
</html>
```

The types we can use for unordered lists are:

```html
<ul type='square'></ul>  <!-- blocks -->
<ul type='disc'></ul>  <!-- bullets -->
<ul type='circle'></ul> <!-- empty circles -->
```



#### Ordered Lists:

Ordered lists are just like unordered lists, but, well, they're ordered! They're numbered/lettered in some way that gives order to the list! EXCITING! They work in the exact same way of unordered lists, but instead of using the unordered list `<ul>` we use the ordered list `<ol>`. [Check it out:](https://codepen.io/bdpastl/pen/zbLEmo)

```html
<!doctype html>
<html>
  <head>
  </head>
  <body>
    <h1> Welcome to my site for counting!! </h1>
    <hr />
     <ol>
       <li> I love counting! </li>
       <li> Math is super neat!</li>
       <li> Did you know that accountants count things for a living!? </li>
       <li> Actuarily, we should account for all mathematically focused jobs!</li>
     </ol>
  </body>
</html>
```

Just like unordered lists, we can use attributes to change [how we're listing things](https://codepen.io/bdpastl/pen/NJBaJZ):

```html
<!doctype html>
<html>
  <head>
  </head>
  <body>
    <h1> Welcome to my site for counting!! </h1>
    <hr />
     <ol type='I'>
       <li> love counting! </li>
       <li> Roman numerals are super weird!</li>
       <li> Did you know romans didn't have a number for zero?!? </li>
       <li> In fact, the Greeks didn't either!! Weird huh??</li>
     </ol>
  </body>
</html>
```

Here are the types of ordered lists we can use!

```html
<ol type='1'></ol> Numbers!
<ol type='a'></ol> Lowercase letters!
<ol type='A'></ol> Uppercase letters!
<ol type='i'></ol> Lowercase roman numerals!
<ol type='I'></ol> Uppercase roman numerals!
```



## Attributes

​	This is a good a time as any to introduce attributes! So far we've only seen the `type` attribute, but from here on out, we'll be using attributes regularly! There are a ton of attributes. There is absolutely no need to memorize them all, but it is good to know the most used ones off the top of your head!

### Style

By using the style attribute, we're allowing for what's called 'inline' styling. That means that we're styling a specific element within our code. This is good to know that we can do (and we will do it for now), but once we learn CSS styling, we won't be doing much inline styling!

### Color

We can change the color of an attribute by giving it a value! We can change the text color with just `color`, and  background color with `background-color`. Take a look and [see these busy colors](https://codepen.io/bdpastl/pen/QoBaKq?editors=1000)

```html
<!doctype html>
<html>
  <head>
  </head>
  <body style='background-color:lightblue'>
    <h1 style='color:red'> Welcome to my site! </h1>

    <hr />
     <ul style='background-color:#FFAA00'>
       <li>I really like to write code</li>
       <li style='background-color:blue; color:white'>I especially like to make my page as colorful as possible!</li>
       <li > Too many colors might be rough on the eyes, though....</li>
     </ul>
  </body>
</html>
```

Notice that not only are we using color names, we're also using hex code! You can find more out about what colors to use by taking a look at the [web colors wikipedia page](https://en.wikipedia.org/wiki/Web_colors).



### Font Size

We don't always want to have the same sizes of font in our paragraphs! We might want some containers with larger fonts, and others with smaller! We can do that with `font-size`! [Take a look](https://codepen.io/bdpastl/pen/NJBXzy):

```html
<!doctype html>
<html>
  <head>
  </head>
  <body style='background-color:lightblue'>
    <h1> Welcome to my site! </h1>

    <hr />
     <ul>
       <li style='font-size:300%'>I really like to write code</li>
       <li style='font-size:2em'>Sometimes, I think making my text get smaller</li>
       <li style='font-size:18px'> and smaller and smaller</li>
       <li style='font-size:12px'> is really funny</li>
     </ul>
  </body>
</html>
```

So, not only can we control exactly what our `font-size` is by way of using pixels, we can also use a percenage of what our font is (with reference to what it already was) with `%` and `em` (`em` is just equal to the current font size).



#### Borders

A lot of time, we want to cordon off some content! We can easily do that with a border! Borders are a little weird though (and we'll explore borders more when we work with CSS). Borders have an intersesting syntax, when we call border, we need to call it with `border: 'size' 'type' 'color'`, like `border: 1px solid black` or `border: 1px dotted red`. [Check it out](https://codepen.io/bdpastl/pen/LaBeKN):

```html
<!doctype html>
<html>
  <head>
  </head>
  <body style='background-color:lightblue'>
    <h1 style='border: 1px solid black'> Welcome to my site! </h1>
		<hr />
    <div style='border: 1px dashed red'>
      My site isn't currently much, but give it some time, and this will become super neat!
    </div>

  </body>
</html>
```





#### Padding and Margin

Padding and Margins helps us add some space around our content! Padding makes the space inside the element bigger, while margin makes the area outside the element bigger! Take a look at the way that [margin and padding render:](https://codepen.io/bdpastl/pen/NJByKB)

```html
<!doctype html>
<html>
  <head>
  </head>
  <body style='background-color:lightblue'>
    <h1 style='border: 1px solid black; padding: 10px'> Welcome to my site! </h1>
		<hr />
    <div style='border: 1px dashed red; margin: 10px '>
      My site isn't currently much, but give it some time, and this will become super neat!
    </div>

  </body>
</html>
```

You may have noticed that we didn't remove the borders! You can add as many styles as you want, just so long as they're broken up by semi-colons!







So, now you've gotten a crash course in web development, try making your own website! Your homework after this week is to make your own site (and host it on your github.io page!). Take all the code elements from above and mix and match (and even try nesting)!
