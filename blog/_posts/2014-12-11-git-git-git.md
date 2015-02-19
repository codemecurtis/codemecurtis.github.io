---
layout: post
title:  "Git, Git, Git"
date:   2014-12-11
categories: Technical, featured
---

What are the best practices associated with using classes vs. ids?



CSS is a very important part of building a website. CSS is like the interior design of your house what good is a house without paint, shingles, a ceiling etc. if you ask me it is not very good at all but some people are different. Today I am going to explain exactly when and how to use ID's or Classes in your HTML. before I begin about that I feel the need to explain why we add these to the HTML and not the CSS file.
CSS uses a very easy way to connect to HTML through something called a link. A link tells the HTML to use "This file" for it's CSS. Here is an example:



```<link rel="stylesheet" type="text/css" href="your-style-sheet.css" />```



Pretty simple to get the files connected but then how does the the CSS know what to target. This is where classes and ID's come in. In order for use to target a certain element in CSS we need to use the html code such as div, p, h1, h2 etc. In this model we will only be using classes and id's to easily undertsnad. to add a class to your HTML it is as simple as



```<div class="your-class">Hello World!</div>```


and for ID


```<div id="your-id">Hello World!</div>```



You can target classes in CSS with a simple:


```.your-class```

And ID


```#your-id```



so now that we know how to add a CSS class and ID and how they talk to eachother let's talk about when to use which one.


ID's are almost like a dishwasher you really only need 1 dishwasher in your house. Id's can only be referenced once for each page. ID's should only be used in a couple scenarios:


If you are setting a link to be targeted on the same page.
```<a href="#about">``` This will reference a element id of about and will move you to that portion of the website.


Refering to an item that will not be like others and have unique features. Refering to the unique part of ID's.


Classes are like the light bulb of your house. Classes are not unique and can be used as many times as you'd like. Classes really come in handy when you are moving thing to left or the right for instance. You can make your CSS look like so:


```.right{float:right;}``` This will move an element to the furthest right point and you can add this class to any element you would like on the right side.


You can also add multiple classes to 1 element. Like So:


```div class="right about-me small"``` This shows multiple clsses by the name of right, about-me and small. A simple space inbetween classes will solve this for you.


Moral of the story on classes and ID's is simple. You will use classes a lot more than you will ID's. If the element is completely unique to anything that you will be creating on the site you should use an id. In any other scenario use a class.
