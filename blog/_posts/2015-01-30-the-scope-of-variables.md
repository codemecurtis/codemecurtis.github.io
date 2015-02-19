---
layout: post
title:  "The Scope Of Ruby Variables"
date:   2015-01-30
categories: Technical
---


###[Local Variables][Local Variables]


Local variables are exactly as they sound, local to the method that they occur in. If you don't remember how to create a method here you go:


{% highlight ruby %}
def my_variable
  # Do Stuff
end
{% endhighlight %}

Now to declare a local variable is it relatively simply:

{% highlight ruby %}myVariable = “Curtis”{% endhighlight %}


If you notice one specific thing about my variable names, they all start with the a lowercase letter. Later we will touch on variables that are all caps but in order for a local variable to be local it will need a lowercase letter. Now I will show you a more exciting sample:


{% highlight ruby %}
def my_method
  name = “Curtis”
  age = “23”
  hometown = “Concord”

  puts “My name is #{name} and I am a #{age} year old, from #{hometown}, CA.”
end
{% endhighlight %}

####**output:**
{% highlight ruby %}
  =>  My name is Curtis and I am a 23 year old, from Concord, CA.
{% endhighlight %}


when working with local variables there are 2 things to remember, they always start with a lowercase letter and they cannot be used out side the ```def``` and ```end``` tags.


###[Global Variables][Global Variables]


Global variables are just that, Variables which can be accessed globally within any part of the program. The can be defined in side a method, outside a method and in a class or even top-level which is outside of the class. In order to write a local va=riable it is just as easy as others just use the ```$```:

{% highlight ruby %}
def global_method
  $global_varaiable = 100
end
{% endhighlight %}


You probably won’t find yourself using global variables very often in ruby especially since they can cause warnings or errors. Global variables can change their values anywhere in the program which will make it tremendously difficult to keep track of the current value unless you start from the beginning and try to find the source problem.



If you do not initialize a global variable and try to call it then the value is uniquely set to ```*nil*```.



Global varaibles can also be traced by a ruby program so their is something called variable value(s) and these are special suffix to the ```$```. Here is a list for you to review.




<table border="1"><tbody><tr><td>```$!``` </td><td> latest error message </td></tr>
<tr><td>
```$@``` </td><td> location of error </td></tr>
<tr><td>
```$_``` </td><td> string last read by ```gets``` </td></tr>
<tr><td>
```$.``` </td><td> line <em>number</em> last read by interpreter </td></tr>
<tr><td>
```$&amp;``` </td><td> string last matched by regexp </td></tr>
<tr><td>
```$~``` </td><td> the last regexp match, as an array of subexpressions </td></tr>
<tr><td>
```$```<em>n</em> </td><td> the <em>nth</em> subexpression in the last match (same as ```$~[```<em>n</em>```]```) </td></tr>
<tr><td>
```$=``` </td><td> case-insensitivity flag </td></tr>
<tr><td>
```$/``` </td><td> input record separator </td></tr>
<tr><td>
```$\``` </td><td> output record separator </td></tr>
<tr><td>
```$0``` </td><td> the name of the ruby script file </td></tr>
<tr><td>
```$*``` </td><td> the command line arguments </td></tr>
<tr><td>
```$$``` </td><td> interpreter's process ID </td></tr>
<tr><td>
```$?``` </td><td> exit status of last executed child process</td></tr></tbody></table>



My only recommendation if you decide to use global variables is that you make your variable names as descriptive as possible and do not change their values later in the program. Get out there and play around with globals and see if there is something you can teach me.



###[Instance Variables][Instance Variables]


Instance variables seem to look cooler and their function is pretty cool as well, they all start with the ```@``` symbol. Instance variables can be declared in many different ways so let me go ahead show you and I will explain each one.



{% highlight ruby %}
class MyClass

  def initialize(name)
    @name = name
  end

end


class MyClass

  @instance = “I am an Instance Vairable”

  def initialize
    # Do Something
  end
end


class MyClass
attr_accessor  :instance_variable

  def initialize
    #Do Something
  end

end

{% endhighlight %}

The first example is one of the most common use cases. This class when called will need and argument or parameter some kind of name. It will then set ```@name``` equal to whatever argument you pass when you call the class.


The second example is just simply setting this variable to a string and allowing it to be declared anywhere inside the class or methods in the class.


The third example is a little more confusing but it isn’t as confusing or odd as it seems. This is the ```attr_accessor``` there is also ```attr_reader``` and ```attr_writer``` they are all similar but have slight differences. ```attr_accessor``` is accessible anywhere in the module or class and can be manipulated however you’d like. ```attr_reader``` is accessible in the entire module as well except that it will only allow you to read what the ```Instance Variable``` is set to. Last but not least the ```attr_writer``` is accessible by the entire module once again but is only writeable meaning it cannot be read and should only be used to write information in between methods, that is not our focus though.


###[Class Variables][Class Variables]


Identical to ```instance variables``` ```class variables``` are declared using the ```@@```. Here is an example for ```class variables```


{% highlight ruby %}
class MyClass

  @@class_variable = Class

  def initialize
    @instance_variable = “Instance”
  end

  def use_case
    puts “This is a #{@instance_variable}”
    puts “This is a #{@@class_variable)”
  end

end
{% endhighlight %}

{% highlight ruby %}
  class = MyClass.new
  class.use_case
{% endhighlight %}


####**Output:**

{% highlight ruby %}
  =>  This is a Instance
  => This is a Class
{% endhighlight %}


just as expected. I like to use these for the counter when trying to iterate through arrays but that is not the only reason to use class variables. Note that they are used a lot less than instance variables but ruby wouldn't have them if they weren’t needed.


###[Constant Variables][Constant Variables]


Constant variables are a almost like a global local variable. They can be used globally if called out side of a class or module and within the class if the declared or set inside a class or module, they however cannot be declared or used inside of a method. Constants are declared just like any other variable only it starts or contains capital letters:


```
Constant = “I am a constant”
```

I am sure you could imagine what this will output but I am sure wondering why and when you would use these. Well just a fair warning ```Constants``` are variable in which ruby recommends not to change the value. Like all things in ruby it is abut readability right? So when using a ```Constant``` someone new to your code base can easily understand the value of this will most likely stay the same the entire time of the program.


These are the variable scopes that ruby has to offer. There are many different use cases for these variables but they all come with time. I am still working on my own knowledge of when and where to use which style of variable.

[Local Variables]: http://www.techotopia.com/index.php/Ruby_Variable_Scope#Ruby_Local_Variables
[Global Variables]: http://www.techotopia.com/index.php/Ruby_Variable_Scope#Ruby_Global_Variables
[Class Variables]: http://www.techotopia.com/index.php/Ruby_Variable_Scope#Ruby_Class_Variables
[Instance Variables]: http://www.techotopia.com/index.php/Ruby_Variable_Scope#Ruby_Instance_Variables
[Constant Variables]: http://www.techotopia.com/index.php/Ruby_Variable_Scope#Ruby_Constant_Scope