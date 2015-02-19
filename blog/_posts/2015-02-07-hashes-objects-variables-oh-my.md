---
layout: post
title:  "Hashes, Objects, Variables Oh My"
date:   2015-02-07
categories: Technical, Featured
---

After spending the last 4 weeks (6 if you count our break) studying the ins and out’s of Ruby, DBC introduced the almighty Javascript or ECMAScript for you vintage coders. I have very little prior experience with JavaScript typically I push this off to my freelance developers in my current position but none the less I still learned a lot. I first learned that there is in fact 2 names for JavaScript as I mentioned before, whether any ones uses the latter option is beyond me but hey it is still learning right ?! Ruby and JavaScript have a lot of the same  methods/functions and syntactically look similar with some small changes. My job is to show you those changes and we will start by working with Ruby Hashes and JavaScript Objects.

###Hashes vs Objects

Ruby hashes are quite handy when building a program they allow you to have a key and value pair. Meaning you can ask the ruby hash for the value of the key which could have many great uses. The Ruby hash is created using the curly braces```{}``` with either a  hash rocket ```=>``` or a colon ```:``` to separate the key and value.

{% highlight ruby %}
myHash = {
  “Key” => “Value”,
  “Key”: “Value”
}
{% endhighlight %}


Now there is no preferred method wether you use the hash rocket or the colon but to each is own. I like to use the hash rocket because there are other uses for the colon in Ruby and t just plain out looks cooler.

###Objects

JavaScript objects are what provided ruby it’s idea for hashes actually. They have quite a bit of similarities but do have some differences as well. Just like hashes javaScript objects are used for key value pairs.Syntactically these look a small bit different but they do both use the curly braces ```{}```, so here we go.


{% highlight javascript %}
var myObject = {
name : “Curtis”
};
{% endhighlight %}


This method of defining a object is called object literal notation. Notice I have separated these on to multiple lines.  could just as simply put this all on one line like this.


{% highlight javascript %}
var myObject = { name : “Curtis”, age: 23};
{% endhighlight %}


There is no differences here but there is also the constructor based syntax ```var myObject = {}```which will simply just create a new blank object unlike Ruby where we use the ```myHash = Hash.new```and you can add properties to the object later. Which actually brings me to the fact that how we referenced hashes as the key and value, JavaScript developers typically call them properties and values of an object. So to add a property to an object after it has been created is quite simple.


{% highlight javascript %}
myObject.location = “DBC” ;
{% endhighlight %}


A simple as it looks this adds the location property to the properties and assigns it a value of DBC. So our object would now look like.


{% highlight javascript %}
var myObject = {
name : “Curtis”,
age: 23,
location: “DBC”
};
{% endhighlight %}


Pretty cool right?! Well we can delete just as simply as saying ```delete myObject.location``` and this will remove what we just added. One last note for objects is that you are always welcome to create an object as a value of a property.


###Defining Variables


If you read any of my other posts on Ruby I am sure we touched on variables, thy are probably one of the most important parts of Ruby because it holds a value for the life of the program or allows you to change it’s value later down the program. You can define a variable by simply ```myVariable = true ```. Pretty simple and straight forward how ever in JavaScript you would define a variable like so, ```var myVariable = true;```. The 2 difference s are the fact that in JavaScript you always will use a semi-colon to end the variable definition and you will always begin with the letters ```var``` this is short for variable and this is what tells Javascript that we would like to define a variable. Again pretty similar to Ruby but those small differences can easily be forgot when coding in both JavaScript and Ruby on the same project.


###The Docs.


Unless I was some kind of kid genius that was born with JavaScript and Ruby knowledge i have to use resources to learn just like any other human being. One of the most used resources are the language docs. These are typically written by the people who write the language and know ever in and out of it. Docs are the most detailed resource for programming languages and provides many different use cases and common errors.


###<a href="http://ruby-doc.org/">Ruby Docs</a>
![ruby_docs](/imgs/ruby_docs_homepage.png)


Ruby Docs are simply put, a mess. It is not the most user friendly website to use but after some practice you realize that a designer did not go creating this website, yet a bunch of computer science nerd who couldn’t tell you matching colors if they had to!



You can see form this homepage that there really isn’t much to be said here besides a simple getting started guide (This is not like your mothers printer you set u for her either) and a couple different version options. Once you finally realize that you should click the ruby version you are using. If you don’t know, go over to the terrifying command line and simple type ```$ ruby -v``` this will out the version of ruby in my case it is 2..0 don’t worry about all those weird numbers and letters after for now.
![ruby_v](/imgs/ruby-v.png)



Once you select the version of Ruby you have it brings you to another mess of a list but if you scroll down a little ways you will see a filter which is sometimes helpful as long as you know which method you want, or you can scroll for miles looking for something logical to what you need. Once you elect the method it gets very detailed on how everything happens what it does etc. It is just a bit of a task trying to get there at first.


###[JavaScript Docs][js_docs]
![JavaScript MDN](/imgs/JavaScript_MDN_homepage.png)

Just starting with the homepage of JavaScript docs you can see it was properly though out. I mean after al this was created by the great people over at Mozilla and they are revolutionizing the web world! From noon we will refer to the docs as MDN just to save me some arthritis :).



MDN has docs for almost all languages but this is most importantly used for JavaScript in this article. You can see at the top of the page that they initially list which version of JavaScript is currently supported by all browsers no selecting the version just getting right to it, which brings me to the [JavaScript guide][js_docs]. This is what my boss likes to say “The Horizontal part of learning” this gives you hands down the best idea of what JavaScript can be used for and all the syntax you need to start coding. Once you finish that you have the wide scale of what javaScript is from there the docs go into a much more detailed “Vertical” learning style.



I have only had so much time with MDN but it has been a much more pleasant experience than with ruby docs. The amount of examples, use cases and explanations of these are great, they have really took their time with designing these docs and providing useful examples. At the end of the day Docs are Docs they are there for your information to learn not to look pretty and dazzle your creative brain.

[js_docs]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide