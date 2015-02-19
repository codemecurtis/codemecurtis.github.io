---
layout: post
title:  "Hashes & Arrays for Days"
date:   2015-01-12
categories: Technical, Featured
---


Enumerable is simply a collection of methods that iterate through a collection of objects and run the following block. I am sure that went over your head so let me break it down for you. Lets start with iterating this is the act of separating each element and providing it an action is what is called a block. I will give you an example.


###Arrays

  Arrays can contain multiple different values such as strings, integers and even other arrays. Those arrays inside of arrays are considered sub arrays, pretty clever right? Your probably thinking well what how do I use these values or even sperate them. Vey good question and below you will see example 1.1(Empty Hash) and 1.2(Standard Hash).


  ```my_array = []```
Example 1.1

  ```my_array = ["A String", 10, ["Sub array string"]]```
Example 1.2

  As you can see above that I seperated my values inside the array with a simple *,* somehow some wat ruby knows how to seperate them but that goes with everything else ruby does on it's own :). Now that you know how to create an array go have some funa and see if you can find a god use before paragraph 3 when I show you examples.


  Accessing array values is just as simple as creatinf them. In example 1.3(Accessing array values) I will show you how to do this.


```my_array[0]```
Exmaple 1.3

I specifically used this example because I want you to understand that in programming almost all the time you will start couting at 0. If you take a look back at example 1.2 I will break this down for you. "A String" is the first value or [0], the number 10 is the scond value or [1] and so on so forth. I like to remember to start my count at 0 but some people may prefer to take the what I would call real world number and subtract 1. As a programmer we would say well that thought should be refactored, catch my drift? All in all arrays are pretty simple for now but later on down the road I am sure I will have a lot more to say about their complextiy.


###Hashes

Hashes are a lot like arrays as well, they both have a value but hashes have a more visible key as well. In example 2.1 I am showing you how to create new hash. This will create a a hash with the key and value of *nil*. There are nemours ways to create a hash but in example 2.2 I will show you our most used method so far.


```Hash.new```
Example 2.1

```my_hash = { "Jane Doe" => 10, "John Doe" => 6 }```
Example 2.2

As you can see the *my_hash* example makes a little more sense to look at so we will reference this for now. You can see here that both the Jane Doe and John Doe are the keys. Which makes the two integers 10 and 6 are the values. In hashes the key and value are seperated by a *=>*. In order to access these values take a look at example 2.3. The semi colon can replace the quotes in this situation and this goes for creating them as well.


```grades["Jane Doe"]<span>or</span>grades[:jane Doe]```
Example 2.3

The biggest difference between hashes and arrays are how they are created obviously but beyond that I am sure you noticed that hashes have a key and value pair rather than just a value. I am sure you can imagine how this will be helpful. Arrays are also an ordered list where as hash values are related to their key. Though not as fun as hashes, arrays have keys as well but they are integer based meaning the numbers I showed you earlier are the keys.