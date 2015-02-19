---
layout: post
title:  "Ruby Classes"
date:   2015-01-22
categories: Cultural
---

It seems to be the obvious for me now a days but almost everything in Ruby is an object or ```Object```. All Object-Oriented languages use them so if you have prior experience with Java you may understand easier than others. Add ruby classes is not different than an object. I am sure in the enumerable methods post last week you work paying close attention to the ```.group_by``` well have you ever wondered how in the heck you can call this on an object. If you answered yes then great we will move forward with the learning (Those who said no can hit the “I hate this” button below to exit). A Ruby class is a collection of variables, methods and their specific behaviors. In the next couple of paragraphs I will “Lay down the law” for classes.


###Instance variables


Instance variables are created at any point in your class but they are accessible by any method that you create inside of a class. And these are created by using the @ or “at sign” some people may refer to it as an ampersand but rest assured an Ampersand is this & back to the important stuff. I will now show you an example of instance variables in action.


{% highlight ruby %}
class TvShows

  def initialize(show, channel, time)
    @show = show
    @channel = channel
    @time = time
  end

  def favorite
    puts "My favorite show is #{@show} and it comes on #{@channel} at #{@time}"
  end

end
{% endhighlight %}


Not the most interesting but I love the show Vikings and the premiere is right around the corner. :) Now I will explain.



We started out by naming our class ```TvShows``` and asked for 3 initial arguments. That would be the T.V. Show name, the channel it is on and the time it comes on. After that we created a new instance method by the name of ```favorite``` and passed a simple string.



We also used a nice feature of ruby called string interpolation that is the ```#{@show}``` in the method ```favorite```. I am not going to go into full detail about this but I am sure I will have another post about this in the future.
*Hint make sure initialize is spelled correctly, Ruby does not take lightly to misspelling.*


###The Output and Description



The above code is probably the most simple example that anyone could think of but it works for us beginners. So you are probably wondering well now how the heck do I use this, that is my job to show you. When I was first starting out with classes I had a huge issue with forgetting to start with the ```.new``` before anything so I will make it my focus.



In order to get the process started you need to set a variable to the new object like so.
You may remember the ```Array.new```, yeah well it is a lot like that. Form there we will use this to initialize the values of ```show```, ```channel```, ```time```. Now what it the method inside of our class do? good question.


{% highlight ruby %}
  favorite_show = TvShows.new("Vikings", "History", "10:00 P.M")
{% endhighlight %}


we can now say ```favorite_show.favorite``` and the output should go as follows


{% highlight ruby %}
  Output => My favorite TV Show is Vikings. It comes on at 10:00 P.M on History channel.
{% endhighlight %}


Again note this as the most simple example that classes are used for, As my experience grows yours will grow with it. I see a post in the near future displaying how we can make a game for instance like Bingo or a guessing game or why not even “peek a boo”.Classes can grow pretty long in size just like the original ```Array``` class but it is always to keep in mind to break methods up into small pieces of code for other to understand. You will probably spend a lot of time with refactoring classes just because there are so many methods and uses for classes. With that being said what are you still doing here!!! Go out there and practice cause as they say it will make you perfect.

