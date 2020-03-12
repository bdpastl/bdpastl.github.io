# CSS!

CSS stands for Cascading Style Sheets! Using CSS allows for us to style our sites beyond basic HTML elements! We've already run into styling from the last lesson! Now we're going to take what we've learned from that lesson and expand on it!

We can write our css stylings either inline (which we've already done in the past lesson), in the `<style>` section of our page's `<head>`, or in a completely separate file (we'll get to that at the end, for now we'll start moving our CSS to the style section in the head). 



## Syntax: 

CSS Syntax looks completely different from HTML! This is because it's a different type of language! 

When we write CSS in the style section or a CSS file, we don't wrap it in quotations, like we did with inline styling: 

```css 
selector { property: value, property: value} 
```

In CSS, the property:value pair is a declaration. 

```css
p { color: 'blue', font-size: 12px }
```

CSS Doesn't care how many spaces/new lines your code has, but just make sure you have both opening and closing curly braces!



## Using CSS: 

Like mentioned above, we've already seen  inline styling. This works completely fine and well, but that takes too long to change every single inline style you use. Inline styling is great for one or two changes, but when you have to change every line, that becomes painful. What happens if our website has multiple pages, each with hundreds of lines? Let's quickly convert some inline styled code to use CSS! 

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
        <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/christmasTarantula.JPG' width='500px' />
    </div>  
  </body>
</html>
```

We have styling for our `body`, `h1`, and our `img`. Instead of our stylings and put them in a `<style>` section our `<head>`! [See how the code renders like the above code, but with styling in the header?](https://codepen.io/bdpastl/pen/WWbWVx) 

  ```html
<!doctype html> 
<html>
  <head>
    <style>
      body { background-color: lightblue }
      h1 { border-left: 1px solid blue; 
      		 padding: 10px 
         }
      img { width: 500px }
    </style>
  </head>
  <body>
    <h1> Images are some of the best parts of the internet! </h1> 
		<hr />
   	<div>
       Check out this beautiful image of my old pet, Rosie! 
        <img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/christmasTarantula.JPG' />
    </div>  
  </body>
</html>
  ```

Notice how we put our styling in the `<style>` section of our site, following the below format:

```css 
selector { property: value, property: value} 
```

By using the above format, we've told our site that every time we use a h1, it will always have a border-left, and a padding of 10 pixels, and all of our `<img>` elements will have a width of 500 pixels! As far as our body is concerned, we've only got one, but it's nice to have our styling all in one place instead of spread out throughout the HTML's code! 

### Classes and Identities:

What if we wanted our divs to all have different styles? We can't do that with the CSS above! By using Classes and Identities, we can use as many different styles as we want! 

The differences between classes and IDs is that IDs are unique, and classes aren't! Multiple elements can have the same class, whereas only single elements can have an id. 

What does this mean? 

#### IDs

Creating an ID in a stylesheet, you need to start your selector with the `#`.  [See it in action](https://codepen.io/bdpastl/pen/oOgRjm). 

```html
<!doctype html> 
<html>
  <head>
    <style>
      #IamAnID { color: red } 
    </style>
  </head>
  <body>
    <div id='IamAnID'>WHAT COLOR AM I!?</div>
  </body>
</html>
```



The ID that we made in our `<style></style>` element is used by the `<div></div>` element in our body. Remeber that the ID absolutely has to match (so it's case sensitive). 

By using the ID, we then get to turn our div's color to red! 

A downside to using ID is that only one element should use it in your whole page! [We shouldn't do this](https://codepen.io/bdpastl/pen/zXxQrj): 

```html
<!doctype html> 
<html>
  <head>
    <style>
      #IamAnID { color: red } 
    </style>
  </head>
  <body>
    <div id='IamAnID'>WHAT COLOR AM I!?</div>
    <div id='IamAnID'>I'm the same color!</div>
  </body>
</html>
```

This is because IDs are just that, a specific ID! It's like if somebody was trying to use your driver's license (or school ID, or anything). They're not you! (Note: because our browsers are really good at trying to fix our mistakes, it will render the colors properly, but having more than 1 ID can lead to more problems later on!)



#### Classes

To share CSS among multiple elements, we should use Classes! 

Instead of a `#`, we use a `.` [This way we get to share everything!](https://codepen.io/bdpastl/pen/OGPYbM) 

```html
<!doctype html>
<html>
  <head>
    <style>
      .IamAClass { color: red } 
    </style>
  </head>
  <body>
    <div class='IamAClass'>WHAT COLOR AM I!?</div>
    <div class='IamAClass'>I'm the same color!</div>
  </body>
</html>
```



So, now we can use the same class over and over and over again! When we try to use the class, we add the attribute 'class' in our element, and assign it to the name of our class in the css 'IamAClass'. 

[You can mix and match as many classes and IDs as you want ( remember, some classes might override others):](https://codepen.io/bdpastl/pen/MRYdoQ)  

```html
<!doctype html>
<html>
  <head>
    <style>
      #IamAnID { color: red }
      .bold { font-weight: bold }
      .italic { text-style: italic }
      .underline { text-decoration: underline }
    </style>
  </head>
  <body>
    <div id='IamAnID' class='bold italic underline' >My color is red, I am bold, italic, and underlined!</div>
  </body>
</html>
```



### Commenting Your CSS!

When we wrote comments before in HTML, we used  `<!-- -->`. Because CSS is a different language, we comment differently. We use `/* */`. Just like html, you put your comments between the text: `/* I am a comment! */`. [See (or really don't see) the comments in action!](https://codepen.io/bdpastl/pen/XQJweB?editors=1000) 

```html
<!doctype html>
<html>
  <head>
    <style>
      /* I AM COMMENTED OUT  */
      .IamAClass { color: red } 
    </style>
  </head>
  <body>
    <div class='IamAClass'>WHAT COLOR AM I!?</div>
    <div class='IamAClass'>I'm the same color!</div>
  </body>
</html>
```



### Stylings: 

Now let's explore the differing kinds of stylings we can use! 

#### Background colors: 

We've already seen background-color, but it's good to revisit it! To change background colors is background-color:

​		 `b { background-color: green }`

[See it again in action:](https://codepen.io/bdpastl/pen/yryWvv?editors=1000) 

```html
<!doctype html>
<html>
    <head>
        <style>
            body { background-color: cyan }
        </style>
    </head>
    <body>
        <div> Oh wow, look at this cyan body!  </div>
    </body>
</html>
```



#### Background images! 

You can add a background image if you want (though not always the greatest idea)! [Can you spot the cat in the background??](https://codepen.io/bdpastl/pen/axzrGX)

```html
<html>
    <head>
        <style>
            div { background-image:url('https://ichef.bbci.co.uk/images/ic/720x405/p0517py6.jpg'); height:400px; width:700px;  }
        </style>
    </head>
    <body>
        <div> I HAVE A CAT BEHIND ME!!  </div>
    </body>
</html>
```

Try changing the image height and width to be larger. Notice that the image repeats? You can change that using the attribute: 'background-repeat:no-repeat' in your css! 

With background-repeat, you can use the values: 

- [no-repeat](https://codepen.io/bdpastl/pen/rbagqq?editors=1000)
- repeat // this is the default value
- [repeat-x // repeats along the x-axis (horizontally)](https://codepen.io/bdpastl/pen/yryWGE?editors=1000)
- [repeat-y // repeats along the y-axis (vertically)](https://codepen.io/bdpastl/pen/WWbBmX?editors=1000)

You can use both direct and relative links too! If you have an image file named myImage.jpg in the same folder as  your index.html file, you could just write url('./myImage.jpg') 



##### Background-Attachment: 

This allows your image to [scroll with the page](https://codepen.io/bdpastl/pen/xeGQmZ)! 

```html
<!doctype html>
<html>
  <head>
    <style>
      .scrollImage { background-image:url('https://ichef.bbci.co.uk/images/ic/720x405/p0517py6.jpg'); height:1200px; width:1200px;
        background-repeat:no-repeat;
        background-attachment: scroll}
    </style>
  </head>
  <body>
    <div class='scrollImage'> TRY SCROLLING!  </div>
  </body>
</html>

```



You can also have your image fixed, so that the text scrolls, [while your image does not](https://codepen.io/bdpastl/pen/pBJQqY)! 

```html
<!doctype html>
<html>
    <head>
        <style>
            .dontScroll { background-image:url('https://ichef.bbci.co.uk/images/ic/720x405/p0517py6.jpg'); height:1200px; width:1200px;
  background-repeat:no-repeat;
  background-attachment: fixed}
        </style>
    </head>
    <body>
        <div class='dontScroll'> TRY SCROLLING!!  </div>
    </body>
</html>
```



##### Background position: 

You don't always want to have your background chilling in the top left of your page. That's boring. Pur yours wherever you [want with `background-position`](https://codepen.io/bdpastl/pen/wZaREL) :

```html
<!doctype html>
<html>
  <head>
    <style>
      .dontScroll { background-image:url('https://ichef.bbci.co.uk/images/ic/720x405/p0517py6.jpg'); height:1200px; width:1200px;
        background-repeat:no-repeat;
        background-position: center }
    </style>
  </head>
  <body>
    <div class='dontScroll'> There's a cat in the center!   </div>
  </body>
</html>
```

You can position it to have the values: 

- [top](https://codepen.io/bdpastl/pen/BENvqe)
- [center](https://codepen.io/bdpastl/pen/wZaREL)
- [bottom](https://codepen.io/bdpastl/pen/ZZGVmp)
- [left](https://codepen.io/bdpastl/pen/MRwZZj)
- [right](https://codepen.io/bdpastl/pen/VNLqqB)

We'll come back to this, but you can also set your postiion by using pixels and percentages too! 



#### Text Formatting! 

We did some text formatting earlier, but let's take a deeper dive! 

##### Text Color

To change your text's color in an element, you can use the color property. You can name your colors with either the [color's name OR use the hex code value.](https://codepen.io/bdpastl/pen/MRaWQZ?editors=1000) 

```html
<!doctype html>
<html>
    <head>
        <style>
            .blue { color: blue }
            .blueHex { color: #0000FF }
        </style>
    </head>
    <body>
        <div class='blue'> my color's blue!!   </div>
        <div class='blueHex'> my color's also blue, but from using hex code!!   </div>
    </body>
</html>
```



##### Italics

Sometimes you want to italicise things. When you do that, you can use `font-style` property. This takes in either italic, oblique, or none [(italic and oblique are more or less the same thing)](https://codepen.io/bdpastl/pen/vMNYRy?editors=1000): 

```html
<!doctype html>
 <html>
    <head>
        <style>
            .italicsClass { font-style: italic }
            .obliqueClass { font-style: oblique }
        </style>
    </head>
    <body>
        <div class='italicsClass'> I'm italic!!   </div>
        <div class='obliqueClass'> I'm oblique!!   </div>
    </body>
</html>

```



##### Bolds

​    When you want to make something bold, you want to use the font-weight property! Font-weight takes the values of: [bold and normal](https://codepen.io/bdpastl/pen/ZZbExP?editors=1000)

```html
<!doctype html>
  <html>
    <head>
        <style>
            .boldMove { font-weight: bold }
        </style>
    </head>
    <body>
        <div class='boldMove'> I'm bold!!   </div>
    </body>
</html>

```



##### Underlines Overlines and Strikethroughs

​    When you want to underline, overline, or strikethrough things - we need to use another [property called text-decoration](https://codepen.io/bdpastl/pen/gyaOzx?editors=1000): 

```html
<!doctype html>
<html>
  <head>
    <style>
      .underline { text-decoration: underline }
      .overline { text-decoration: overline }
      .strikethrough { text-decoration: line-through }

    </style>
  </head>
  <body>
    <div class='underline'> I'm very important, so I'm underlined!!   </div>
    <div class='strikethrough'> I'm wrong, so I've got a line through me!!   </div>
    <div class='overline'> I've got a line over my head!!   </div>
  </body>
</html>
```



##### Font Properties!

###### Font-Size: 

​	    Font-Size - you guessed it - it changes the size of our font. Font-size takes in px values (pixel values, like 12px), but also has relatively normal values like xx-small, x-small, smaller, small, medium, large, larger, x-large, and xx-large. Using the px allows for a greater level of custimization, but if you just want some big font and don't want to play with what specific pixel amount you want, [go for the worded values](https://codepen.io/bdpastl/pen/VNvwdK?editors=1000)! 

```html
<!doctype html>
<html>
    <head>
        <style>
            .small { font-size: small }
            .medium { font-size: medium }
            .large { font-size: large }
            .px12 { font-size: 12px }
            .px20 { font-size: 20px}
            .px30 { font-size: 30px}
        </style>
    </head>
    <body>
        <div class='small'> I'm small </div>
        <div class='medium'> I'm medium... </div>
        <div class='large'> I'm large </div>

        <br />

        <div class='px12'> I'm 12 pixels! </div>
        <div class='px20'> I'm 20 pixels! </div>
        <div class='px30'> I'm 30 pixels! </div>
    </body>
</html>
```



###### Font Family: 

This is how you change the actual font (like Times New Roman, Helvetica, ect). Most browsers will be able to render most fonts, but sometimes a browser might not have the proper font installed. For you to ensure that your site looks good, you can include a whole list of fonts to make sure the browser will properly render your site. 

 Because font-family takes in a list of fonts, the values need to be comma separated. If your font has a space in the name, then we need to have the names wrapped in quotations: 

​    `div { font-family: "Fira Code", "Comic Sans", Helvetica, sans-serif }`

[Check out the code:](https://codepen.io/bdpastl/pen/yrYLEG?editors=1000) 

```html
<!doctype html>
 <html>
   <head>
     <style>
       div { font-family: "Fira Code", "Comic Sans", Helvetica, sans-serif }
       p { font-family: monospace, "Times New Roman" }
     </style>
   </head>
   <body>
     <div>Oh hey! What do you think my font will be? </div> 
     <p> What about me?</p>
   </body>
</html>
```

Notice that the div didn't find Fira code or comic sans and went to Helvitica? That's because Fira Code is a very special font that most browsers don't support, and comic sans is actually called "Comic Sans MS", give that a go and see how that works! 

##### Text Properties: 

###### Text align:

​            To align your text is where the text is aligned on your page (like in MS Word). The values we need to use are [left, center, right, and justify.](https://codepen.io/bdpastl/pen/LvpYBG) 

```html
<!doctype html>
<html>
  <head>
    <style>
      .center { text-align:center }
      .left { text-align:left }
      .right { text-align:right }
      .justify { text-align:justify }
    </style>
  </head>
  <body>
    <div class='center'>Let me tell you all a little about myself. My name is Matt Lane, and I grew up down in Imperial, Missouri. Back when I lived there the town was right off the highway, but only 1 block long.</div>
    <br/>
    <div class='left'>We had a local butcher named Harrel who used to make the best cuts of meat. Harrel would literally just have a whole cow hanging in the back room that you could see if you snuck around the counter.</div>
    <br/>
    <div class='right'>A few doors down from Harrel's butcher shop was the local barber. Now, when I was kid, this was back in the day when bleaching only the very tips of your hair was cool. I however, got my hair bleached entirely white. That's because at that time, I really liked dragon ball z. I would do my hair so that it looked like a super saiyan Goku (I thought I was really cool). </div>
    <br/>
    <div class='justified'>At my parents house, we lived across from a really big farm. There weren't many lights out, so you could see stars fill the sky. The downside about living next to a farm, though, was that when the cows would get out, they'd come eat my mom's flower garden (that is, if the deer didn't already get to the flower first). There were always lots of animals around. Most of them were cool, but we sure had a lot of spiders. So many spiders, in fact, that the priest's house at the church we used to go to had a spider infestation so bad, that the entire attic was filled with spiders from wall to wall. They had to fumigate the entire building. At that time, I hated spiders, but now, I actually love them! Many years later, when I worked for the botanical garden, we had dozens of different kinds of spiders to play with! 
    </div>
  </body>
</html>
```



###### Text indent: 

​            This will indent your text a new section of words according to its value! The values for the property are: [length and percentage](https://codepen.io/bdpastl/pen/axvbaz?editors=1000): 

```html
<!doctype html>
<html>
  <head>
    <style>
      .indent5percent { text-indent: 5%  }
      .indent10percent { text-indent: 10%  }
      .indent15px { text-indent: 15px }
      .indent3em { text-indent: 3em }
    </style>
  </head>
  <body>
    <div> If you look at the indent styles, you'll notice that not only are we using percentages but we're also using lengths!  </div>
    <div class='indent5percent'> When working with inputing certain lengths before, we've only used pixel length!</div>
    <div class='indent10percent'>As it turns out, we can use a ton of different types lengths (though pixels do work really well on their own)! </div>
    <div class='indent15px'> When using HTML, it's good to know that there are always a ton of options to do whatever it is that you want. Some of them may be better than others</div>
    <div class='indent3em'>While some may be better than others, just use what you're most comfortable with to begin! You'll come across other styles of coding in time and learn from there!</div>

    <br />
    <div style="text-align:left"> 
      Here are some examples of units to use! (There are many more! You can find a list <a href='https://www.w3schools.com/cssref/css_units.asp'>here</a> )                      
      <table> 
        <tr>
          <th>Unit</th>
          <th>Description</th>
        </tr>
        <tr>
          <td>cm</td>
          <td>centimeters</td>
        </tr>
        <tr>
          <td>mm</td>
          <td>millimeters</td>
        </tr>
        <tr>
          <td>in</td>
          <td>inches</td>
        </tr>
        <tr>
          <td>px</td>
          <td>pixels</td>
        </tr>
        <tr>
          <td>em</td>
          <td>Font size relation! 2 em would mean 2 times the size of the font</td>
        </tr>
        <tr>
          <td>%</td>
          <td>Font size relation as a percentage of the font in your parent element (a parent element is the one that your current element lives in. The parent element of this table data element is a table row element)</td>
        </tr>
      </table>

    </div>
  </body>
</html>

```



###### Text transform

​        Suppose you're feeling lazy, and don't want to type out a certain format in a sentence. Text transform takes the values [capitalize, uppercase, lowercase, and none](https://codepen.io/bdpastl/pen/OGyJoz?editors=1000).

```html
<!doctype html>

<html>
  <head>
    <style>
      .capitalize { text-transform: capitalize  }
      .lowercase { text-transform: lowercase  }
      .uppercase { text-transform: uppercase  }

    </style>
  </head>
  <body>
    <div class='capitalize'> the first letter of each word in my sentence will be capitalized!  </div>
    <div class='lowercase'>   EVEN THOUGH I TYPED THIS SENTENCE WITH CAPS LOCK ON, IT SHOWS UP LOWERCASED!  </div>
    <div class='uppercase'> this whole sentence was written in lowercased letters. the uppercase text-transform did all the work for me!   </div>
  </body>
</html>
```



#### Styling Lists 

You've seen this before, but let's style our lists not inline!    Lists are boring! So, we should style them in some way to spice them up a little bit! We can do this with list-style-type. This property can take a value of: [disc, circle, square, decimal, upper-roman, lower-roman,and upper-alpha](https://codepen.io/bdpastl/pen/BEoaqY?editors=1000). 

##### Bullets, numbers, etc: 

```html
<!doctype html>
 <html>
    <head>
        <style>
            .disc { list-style-type:disc } 
            .circle { list-style-type:circle }
            .square { list-style-type:square }
            .decimal { list-style-type:decimal }
            .upperRoman { list-style-type:upper-roman }
            .lowerRoman { list-style-type:lower-roman }
            .upperAlpha { list-style-type:upper-alpha }
        </style>
    </head>
    <body>

        <h2>Unordered Lists!</h2> <hr />
        <h4>Discs: </h4>
        <ul class='disc'>
            <li> Disc item </li>
            <li> Another disc item</li>
        </ul>

        <h4>Circles: </h4>
        <ul class='circle'>
            <li> A circle item! </li>
            <li> Another circle!</li>
        </ul>

        <h4>Squares: </h4>
        <ul class='square'>
            <li> Check out this square </li>
            <li> We're all squares here </li>
        </ul>

        <h2>Ordered Lists</h2> <hr />
        <h4>Decimals: </h4>
        <ol class='decimal'>
            <li> Numbers are fun! </li>
            <li> Especially when they count!
                <ol>
                    <li>This is great for when you have a lot of sub lists!</li>
                    <li>As a sublist, I agree!</li>
                </ol>
            
            </li>
        </ol>

        <h4>Uppercase Roman Numerals: </h4>
        <ol class='upperRoman'>
            <li> Roman numerals look very official</li>
            <li> You could use this to number your latin quotes! 
                <ol>
                    <li>CARTHAGO DELENDA EST! ("Carthage Must Be Destroyed") - Cato the Elder</li>
                    <li>VENI VIDI VICI ("I came I saw I conquered") - Julius Caesar </li>
                </ol>
            </li>
        </ol>

        <h4>Lowercase Roman Numerals: </h4>
        <ol class='lowerRoman'>
            <li> Lowercase roman numerals are also great!</li>
            <li> Who doesn't love counting with tiny i's? </li>
        </ol>

        <h4>Uppercase Letters: </h4>
        <ol class='upperAlpha'>
            <li> We're pretty used to alphabetical ordering </li>
            <li> A lot of text editors (like MS Word) default to this</li>
        </ol>

        <h2> YOU CAN MIX AND MATCH! </h2><hr />
        <ol class='upperRoman'>
            <li> Uppercase Roman numerals are great</li>
            <li> But why have them all the way down? Why not have subelements with DIFFERENT counting systems? 
                <ol class='lowerRoman'>
                    <li>LABOR OMNIA VINCIT ("Hard work conquers all!") - Virgil </li>
                    <li>PULVUS ET UMBRA SUMUS ("We are but dust and shadow")- Horace </li>
                </ol>
            </li>
            <li> By mixing and matching, it makes it easier to keep track of where you are! </li>
            <li class='decimal'> If you wanted to be crazy though, you could also mix classes mid-list - which I personally think is a bad idea, but don't let me stop you! 
                <ul class='square'>
                    <li>You can also add unordered lists to ordered lists as sublists, and vice versa</li>
                    <li>So many cool list possibilities!</li>
                </ul>
            </li>
        </ol>
    </body>
</html>

```



##### Custom List Images: 

​        Suppose you wanted to make a really bonkers list, and you wanted your own special list item image. What we're really doing is basically setting a background image for all of our list items and then we remove the actual list-style-tyle, [so that there aren't any bullets](https://codepen.io/bdpastl/pen/xewxQG?editors=1000): 

```html
<!doctype html>
<html>
    <head>
        <style>
           li {
               background-image:url('https://media.giphy.com/media/V0YMxvqOXOkEw/giphy.gif');
               background-repeat: no-repeat;
               list-style-type: none; /* this makes it so we don't show any bullets or numbers */
               padding-left:75px;
               padding-bottom:50px;
           }
        </style>
    </head>
    <body>
        <h2>Unordered Lists!</h2> <hr />
        <h4>CATS: </h4>
        <ul class='disc'>
            <li> Check out our cat list </li>
            <li> Cat lists are pretty dang cool</li>
            <li> Cat!</li>
        </ul>
    </body>
</html>
```



#### Adding Width and Height to Elements: 

​    You can add width and height to any element (we did this with images earlier!). We can set special elements to take up smaller amounts of space, or significantly larger! 

##### Width:

Takes a value of either some length or a perentage. If you don't specifically say what you want the width to be, the browser will automatically adjust it to [whatever it thinks the right size is.](https://codepen.io/bdpastl/pen/gyaOQG?editors=1000)     

```html
<!doctype html>

<html>
  <head>
    <style>
      .auto { width:auto } /* atomatic width - we don't need to put this in since it's default, but it's good to see*/
      .half { width: 50% }
      .pixel { width: 500px }
      .border { border: 2px solid black }
    </style>
  </head>
  <body>
    <div class='auto border'> I am an automatically scaled div </div>
    <div class='half border'> I'm half of the screen! </div>
    <div class='pixel border'> I'm 500 pixels wide!</div>
  </body>
</html>

```



##### Height:

This works the exact same as width, but It's mostly recommended to use pixels or some other length measurement. The downside is that height doesn't always work with auto and percentages (you'll see below). Try taking this code and opening it on a browser on your own machine [(that is, save it to a file called height.html and double click on it)](https://codepen.io/bdpastl/pen/MRaWzR?editors=1000): 

```html
<!doctype html>
 <html>
   <head>
     <style>
       .auto { height:auto } 
       .half { height: 50% }
       .pixel { height: 500px }
       .border { border: 2px solid black }
     </style>
   </head>
   <body>
     <div class='auto border'> I am an automatically scaled div, I should be the whole screen, but I don't always work like I should </div>
     <div class='half border'> I should be half of the screen! </div>
     <div class='pixel border'> I'm 500 pixels wide!</div>
   </body>
</html>
```





#### Borders: 

​    We've seen a lot of borders already. Borders take values of either, thin, medium, thick, and some value of length. Up to now, we've only been using solid borders, but borders can be: none, solid, dotted, ridge, inset, double, groove, outset, and dashed. You absolutely need to choose a type of border for it to work! [For the 3d borders, we need to add border-color too](https://codepen.io/bdpastl/pen/oOjNJz?editors=1000). 

```html
<!doctype html>
  <html>
    <head>
      <style>
        div { padding: 5px;
        }
        .badBorderNoType { border: 3px;}
        .solidBorder { border: 3px solid;}
        .dottedBorder { border: 3px dotted;}
        .doubleBorder { border: 3px double;}
        .dashedBorder { border: 3px dashed;}
        .insetBorder { border: 6px inset; border-color: green}      /* This is a 3d border - needs a border color defined*/
        .grooveBorder { border: 6px groove; border-color: teal}    /* This is a 3d border - needs a border color defined*/
        .outsetBorder { border: 6px outset; border-color: blue}    /* This is a 3d border - needs a border color defined*/
        .ridgeBorder { border: 6px ridge; border-color: purple}      /* This is a 3d border - needs a border color defined*/

      </style>
    </head>
    <body>
      <div class='badBorderNoType'> I am a bad border, since I have no type, so my border won't render  </div> <br />
      <div class='solidBorder'> I'm a solid border. You've seen me before. </div><br />
      <div class='dottedBorder'> I'm a dotted border! </div><br />
      <div class='doubleBorder'> Double borders! Just in case you wanted to circle something twice!</div><br />
      <div class='dashedBorder'> I'm surrounded by dashes! </div><br />
      <div class='ridgeBorder'> Check out my ridges </div><br />
      <div class='grooveBorder'> Groovey </div><br />
      <div class='insetBorder'>  I'm INSET - does it look like inside the page? </div><br />
      <div class='outsetBorder'> I'm OUTSET - does it look like I'm coming out of the page?</div><br />
    </body>
</html>
```



​    You can change specific parts of the border width by adding a direction:  [top, right, bottom, left](https://codepen.io/bdpastl/pen/bJVGOK?editors=1000): 

```html
<!doctype html>
    <html>
      <head>
        <style>
          .leftBorder {
            border-left-width: 3px;
            border-left-color: darkslateblue;
            border-left-style: solid;
          }

          .leftPadding { 
            padding-left: 5px
          }

        </style>
      </head>
      <body>
        <div class='leftBorder'>
          <h2 class='leftPadding'>I only have a left border!</h2>
          <div class='leftPadding'>We don't always want a full border! Maybe we just want a left border to make it look like we're quoting someone!</div>
        </div>
        <br />
        <div> Borders are extremly useful! Think about if you had a table! You'd need a border to show which cells are which! </div>
      </body>
</html>

```



#### Spacing Margins and Padding! 

 You've probably noticed that we've been adding padding on some of our examples to be a bit more clear! Let's go over that now! 

Margins are the spacing AROUND the element (like OUTSIDE of our border)

Padding is the spacing INSIDE the element ( like INSIDE of our border)

Just like 'border', we can access specific sides for our [margins and padding](https://codepen.io/bdpastl/pen/gyaOqX?editors=1000): 

- margin-left
-  margin-right
- margin-top
- margin-bottom
- padding-left
- padding-right
- padding-top
- padding-bottom

```html
<!doctype html>
<html>
  <head>
    <style>
      .margin { margin: 15px; border: 2px solid slateblue }
      .padding { padding: 15px; border: 2px solid darkred }
    </style>
  </head>
  <body>

    <div class='margin'> I have a margin of 15 pixels, look at where my border is!</div>
    <div class='padding'> I have padding of 15 pixels, look at where my border is!</div>
    <div> Both of the above divs have 15 pixels above and below them, but notice that the margin has the extra space outside of the border while the padding has the extra space inside the border!</div>
  </body>
</html>

```







#### Changing Mousetype! 

​            If you want to have a mouse cursor that's different than just the normal mouse, you can create your own! This may be for when your site's loading, it may just be because you want to have something different! 

​            There are a some cursors that you can use that are pre-supplied values: crosshair, default,  help, move, text, wait, and resize elements: [(n-resize, s-resize, e-resize, w-resize, ne-resize, nw-resize, se-resize, and sw-resize)](https://codepen.io/bdpastl/pen/jRbOdQ)

```html
<!doctype html>
<html>
  <head>
    <style>
      .border { border: 1px solid black; 
        padding: 25px;
        width:10px;
        height:10px }
      .crosshair { cursor: crosshair }
      .help { cursor: help }
      .move { cursor: move }
      .text { cursor: text }
      .wait { cursor: wait }
      .resizeN { cursor: n-resize }
      .resizeS { cursor: s-resize }
      .resizeW { cursor: w-resize }
      .resizeE { cursor: e-resize }
      .customFox { cursor: url('https://www.cursor.cc/cursor/850/82/cursor.png'), auto}
      .customRainbow{ cursor: url('https://66.media.tumblr.com/365bb77e17bd28f0e65b884ebd61370c/tumblr_inline_mywcw3nnGD1qellpe.gif'), auto}
      .customThinkingEmoji { cursor: url('https://www.cursor.cc/cursor/236/89/cursor.png'), auto}
    </style>
  </head>
  <body>
    <div>
      Anything outside of the table here has a normal cursor!
    </div>
    <table>
      <tr class='border'>
        <td class='crosshair border'> CROSSHAIR </td>
        <td class='help border'> HELP</td>
        <td class='move border'> MOVE </td>
        <td class='wait border'> WAIT </td>
      </tr>
      <tr class='border'>
        <td class='resizeN border'> N-RESIZE  </td>
        <td class='resizeS border'> S-RESIZE </td>
        <td class='resizeE border'> E-RESIZE  </td>
        <td class='resizeW border'> W-RESIZE  </td>
      </tr>
      <tr class='border'> 
        <td class='text border'> TEXT </td>
        <td class='customFox border'> CUSTOM: FOX </td>
        <td class='customRainbow border'> CUSTOM: RAINBOW </td>
        <td class='customThinkingEmoji border'> CUSTOM: THINKING EMOJI </td>
      </tr>
    </table>

  </body>
</html>
```





#### Display!

​    Display is a very powerful property that we'll use more in the future, once we start working with javascript, but for now, we'll just look at a few things we can do with display.

​    Turn any non-block element into a block element: 

​        Remember how we used `<strong>` to make words bold? Strong only surrounded a given word, and that was it. It didn't take up any more space than it needed. We can change that, though, with the display property. [This works for literally any non-block element](https://codepen.io/bdpastl/pen/NmGWJB?editors=1000)! 

```html
<!doctype html>
<html>
  <head>
    <style>
      .block{ display: block; 
        border: 2px solid black}
    </style>
  </head>
  <body>
    <div>Regularly, when using a <strong>strong</strong>, we don't have to worry about it taking up more space than it needs. Sometimes, we want a <strong class='block'>strong</strong> to take up way more space than it needs!</div>
  </body>
</html>


```

​    Vice Versa, sometimes we don't want block elements to take up an entire section! [We can then use the value 'inline' for the display property to take care of that!](https://codepen.io/bdpastl/pen/vMNYMZ?editors=1000) 

```html
<!doctype html>
<html>
  <head>
    <style>
      .inline{ display: inline;
        border: 2px solid black 
      }
    </style>
  </head>
  <body>
    <div>Regularly, when using a <div>div</div> it takes up all the space because it's a block element! If we use the inline value on the display property our <div class='inline'>div</div> won't take up any more than we need! 
    </div>
  </body>
</html>
```



 Suppose we wated our inline block to have a certain amount of width? It won't work because display's inline value takes away all [width, height, margin-top, margin-bottom, and float properties](https://codepen.io/bdpastl/pen/WWQNWa?editors=1000). 

```html
<!doctype html>
<html>
  <head>
    <style>
      .inline{ display: inline;
        border: 2px solid black;
        width: 100px;
      }
    </style>
  </head>
  <body>
    <div>Regularly, when using a <div>div</div> it takes up all the space because it's a block element! If we use the inline value on the display property our <div class='inline'>div</div> won't take up any more than we need! 
    </div>
  </body>
</html>
```

 To get around this, we can use the [inline-block value!](https://codepen.io/bdpastl/pen/dLYyEN?editors=1000) 

```html
<!doctype html>
<html>
  <head>
    <style>
      .inline{ display: inline-block;
        border: 2px solid black;
        width: 100px;
        height: 25px;
        text-align: center;
      }
    </style>
  </head>
  <body>
    <div>Regularly, when using a <div>div</div> it takes up all the space because it's a block element! If we use the inline value on the display property our <div class='inline'>div</div> won't take up any more than we need! 
    </div>
  </body>
</html>
```





#### Float! 

 Let's say you want your divs to all be right next to each other, but don't want to constantly be using display's inline-block value. We can get around this by using float! 

​            [Remember that divs are block elements, so they take up as much space as possible (width wise)](https://codepen.io/bdpastl/pen/pBjomY?editors=1000):

```html
<!doctype html>
<html>
  <head>
    <style>
      .border{ border: 2px solid black; margin: 5px}
    </style>
  </head>
  <body>
    <div class='border'>I am a block element! </div>
    <div class='border'>I am ALSO a block element</div>
  </body>
</html>
```

​            When we use float, though, we're able to get around the whole "divs taking up the entire width of the page, thing" in a more dynamic way than using display: inline-block. [Let's check it out:](https://codepen.io/bdpastl/pen/bJVGPj?editors=1000) 

```html
<!doctype html>
<html>
  <head>
    <style>
      div { float: left }
      .border{ border: 2px solid black; margin: 5px}
    </style>
  </head>
  <body>
    <div class='border'>I am a block element! </div>
    <div class='border'>I am ALSO a block element</div>
  </body>
</html>
```

​        Making divs right next to each other is neat, but what's the point? Well, let's say we wanted to have a cool photo blog? Instagram is great and all, but I want to have my own special site. [Let's try to make one of those](https://codepen.io/bdpastl/pen/BEoyaV?editors=1000): 

```html
<!doctype html>
<html>
  <head>
    <style>
      div { float: left }

      .border{ border: 2px solid black; margin: 5px}

    </style>
  </head>
  <body>
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
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/luna.JPG' /></div>
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/morphoScales.png' /></div>
    <div><img src='https://raw.githubusercontent.com/LaneMatthewJ/lanematthewj.github.io/master/img/moth.JPG' /></div>
  </body>
</html>

```

​            We haven't done any extra work to make sure our images are all similar sizes. Let's try again, by adding a [width to our images in css](https://codepen.io/bdpastl/pen/qwOEEq)

```html
<!doctype html>
<html>
  <head>
    <style>
      div { float: left }
      img { width: 500px; height: 500px }
      .border{ border: 2px solid black; margin: 5px}

    </style>
  </head>
  <body>
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

​    This looks a lot better. Let's add some padding to get some borders around our images! [Also, let's add a title](https://codepen.io/bdpastl/pen/QPvPZw?editors=1000):

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



#### FlexBox! 

[Flex box does a lot of this for us!](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) Let's take a look! 

- [Simple Layouts](https://codepen.io/bdpastl/pen/yrLPwY)
- [Gridlist](https://codepen.io/bdpastl/pen/EJxooE)
- [MORE](https://codepen.io/bdpastl/pen/mgdpvd)

