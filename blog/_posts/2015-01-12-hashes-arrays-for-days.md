---
layout: post
title:  "Hashes & Arrays for Days"
date:   2015-01-12
categories: Technical, Featured
---


Enumerable is simply a collection of methods that iterate through a collection of objects and run the following block. I am sure that went over your head so let me break it down for you. Lets start with iterating this is the act of separating each element and providing it an action is what is called a block. I will give you an example.


{% highlight ruby %}
  arr = ["Hello", "World", "He is crazy", "Wait", "What"]
  arr.each { |element| puts element }
{% endhighlight %}
Alternitevly we could say
{% highlight ruby %}
  arr = ["Hello", "World", "He is crazy", "Wait", "What"]
  arr.each do |element|
    puts element
  end
{% endhighlight %}

This is saying go through each element in arr which is an array and print each value on to the screen. Now back to the collection of objects which is in this scenario arr it can either be an array or hash. The curly braces after the each method is the block which is creating a temporary variable of <i>element</i> and telling to print each element of the array. This is a great way to make 1 line solutions and have it very human readable.


###Group_by
I will now go through one of my more favorite enumerable methos which is ```group_by```. Is simple ```group_by``` does eaxtly that by the value that you ask for. As ruby explains it
<blockquote>
  "Groups the collection by result of the block. Returns a hash where the keys are the evaluated result from the block and the values are arrays of elements in the collection that correspond to the key.
  &nbsp;
  If no block is given an enumerator is returned."
</blockquote>


As an example I will group an array and a hash so let's start with an array.

{% highlight ruby %}
  array = [10,45,18,33,59,78,43,100,8,12,83]
  array.group_by {|element| element % 2 == 0}
{% endhighlight %}
####**Output:**
{% highlight ruby %}
  [10,18,78,100,8,12]
{% endhighlight %}

The syntax is almost identical to the each method we used earlier but we used ```group_by``` instead. What I am asking here is for each element in the array that's modulo (The remainder) is equal to 0. This is a complicated way of saying return each integer that is an even number. There is another method that we could add here to refactor our code. I will explain refactoring later.
{% highlight ruby %}
    array.group_by {|element| element.even?}
  {% endhighlight %}


the ```.even?``` method returns every number that is even in the given object. This is a great way to make your code easily readible for someone new to your project or new to coding in general. Now I will give you an idea for hashes. Knowing that hashes have accessible keys and values unlike arrays this will give us a little more creative example.

{% highlight ruby %}
  hash = {"Strawbery" => "fruit", "Potato" => "vegetable", "Orange" => "fruit", "Grape" => "fruit", "Lettuce" => "vegetable"}
  hash.group_by { |key, value|  value }
{% endhighlight %}
####**Output:**
{% highlight ruby %}
  {"fruit"=>[["Strawbery", "fruit"], ["Orange", "fruit"], ["Grape", "fruit"]], "vegetable"=>[["Potato", "vegetable"], ["Lettuce", "vegetable"]]}
{% endhighlight %}

Similarily to the array it grouped our hash by the object we ask. The biggest difference is in the temporary variables we set. In this example I used ```key``` and ```value``` for easy identification. After we say key and value we ask for it to group by similar values. In this example we would see ```fruit=>``` and ```vegetable=>``` these are the like values and we can see that Strawberry, Orange and Grape are all fruits.


I am sure you could imagine why this is a good method. It will take a lot of required code and logic and bundle it up into a nice short and readable method. To touch on refactoring real quick. In a simple format refactoring is looking at your initial solution and finding ways to make this easier to read, remove any un neccessary logic, variables or loops. In our industry it impartative for us to write readable code, 9 times out of 10 some one else will eventually take a look at your code and nobody wants to spend hours just trying to understand what you are doing.


I hope you have some time to play around with some enumerables and find great uses for ```group_by``` and ```each```. Just remember if you are trying to write easy to read code always try to remove the ```do``` and ```end``` when there is a enumerable method available.