---
layout: post
title:  "My Reaction to reactJS"
date:   2015-02-11
categories: Technical, Featured
---

[React.JS][React JS] is an open-source JavaScript library that was built by our friends over at Facebook. They took years of failing their UI (User Interface) on both desktop and mobile applications when it came to rendering data to the user alas react. React is the V (View) in MVC (Model View Controller) it is not an entire language or framework like Angular or Backbone.

The fashion that react updates the DOM is great because they guarantee that they will only re render what was changed and they do this through the virtual DOM. React uses the virtual DOM diff implementation for ultra-high performance. meaning what ever is different from it’s previous state will now be included when the user asks for it. This sounds quite confusing even to myself because we are so use to making the page refresh when we need something changed, this eliminates all of that and renders your changes lightning fast. React’s also has an optional resource called JSX this is a really helpful tool and I will tell you more now.

###What is JSX?
JSX is a XML style object oriented programming language. with react you have the choice of using vanilla JavaScript or you can use JSX. Syntactically JSX is a little easier to right for newer developers but we will work with both styles.

###How to use [React?][React JS]
React is most commonly paired with Angular or Backbone which i great because both of those JavaScript frameworks have a less focus on their views. So we could use backbone models and controllers to serve data to our react code and have use a very fast rendering of let’s say an autocomplete form but that is a bit much for us now so lets start with a simple Hello World We of course will need to download the library so head over to React’s website and download the latest version. To get started we will need to include 2 SJ files in our HTML.

  {% highlight html %}
    <!DOCTYPE html>
    <html>
      <head>
        <script src="build/react.js"></script>
        <script src="build/JSXTransformer.js"></script>
      </head>
      <body>
        <div id="example"></div>
      </body>
    </html>
{% endhighlight %}

This is how we are going to get all the fancy new features I will be showing you. This is the simplest for of a use for react. It seems like a lot more coding that if we just declared an HTML document and put an H1 with the value of "hello world".

{% highlight html %}
      <!DOCTYPE html>
      <html>
        <head>
          <script src="build/react.js"></script>
          <script src="build/JSXTransformer.js"></script>
        </head>
        <body>
          <div id="example"></div>
          <script type="text/jsx">
            React.render(
              <h1>Hello, world!</h1>,
              document.getElementById('example')
            );
          </script>
        </body>
      </html>
{% endhighlight %}

Hello, world!





Nothing really to fancy here but the future is what we have to think of. What if we want to change the h1 to the user’s name once they login then it makes a lot more sense. So let’s see if we can figure out how to do this but first let’s see our options. We of course could do something really cool where the user’s name is already stored in a database somewhere and we can ask the database for the information but that is a little beyond my knowledge right now so let’s go with a simple input for to update the information.

{% highlight javascript %}
<script>
  var converter = new Showdown.converter();

  var MarkdownEditor = React.createClass({
    getInitialState: function() {
      return {value: 'Type some *markdown* here!'};
    },
    handleChange: function() {
      this.setState({value: this.refs.textarea.getDOMNode().value});
    },
      render: function() {
      return (
        <div className="MarkdownEditor">
          <h3>Input</h3>
          <textarea
            onChange={this.handleChange}
            ref="textarea"
            defaultValue={this.state.value} />
          <h3>Output</h3>
          <div
            className="content"
            dangerouslySetInnerHTML={
              __html: converter.makeHtml(this.state.value)
            }
          />
        </div>
      );
    }
  });
      React.render(<MarkdownEditor />, mountNode);
</script>
{% endhighlight %}

This will give use a texture as an put and an out put below it. You can find a working example on Reacts website.

First off we are setting a variable converter to the value of a new showdown converter.

We then start getting into the juiciness. We created a variable and passed an initial state value of "Type some *markdown* here". Once we have the initial state we need to created the "changer" in this case the handleChange method. this is setting a new state of the text area to the provided value.

Now we need to render the textarea and the output. We are going to use that oh so friendly method render. We will then create a div with the a title and the textarea we are going to be changing. We use the onChange method from the request of our earlier code handleChange.

By the end of all of this we have to finally show the initial state output and then change it once we see it fit. So we will create a new div by the name of "content" and set the html value tot he new states value.

This is a pretty nice example of just how quick you can get things up and running once you learn the syntax of React. Again this is only about a weeks worth of reading on React with a mix of all DBC work so don’t kill me if I didn’t explain every little detail of the program.

###Who is using React?
Of course Facebook uses react but who else is using react and how can we find out. Almost all of Instagram’s front-end rendering was rebuilt in react when they got bought out by Facebook back in April or 2012.

The easiest way to find a website using react of course would be to go here but you can also use our good friend Chrome Dev Tools and see if the react.js library is included somewhere between the head tags. Some companies may choose to place this at the bottom of the page in the footer or may have about 100 different tags in their head so it will be tough to find.

I will leave you guys with a couple of my favorite examples and showcases and let you work your magic from here.

This neat example shows how you can use different colors to change the class of the t-shirt, doesn’t it render almost immediately? yea well go thank React for this.

[Custom Ink][Custom Ink] design lab
Next is a product i use for work called hip chat is has a lot of nice features and uses react quite heavily. Unfortunately to show you, you will need an account on HipChat but it is free if you want to look at the source code.

[Hip Chat][Hip Chat]

[Hip Chat]: https://www.hipchat.com/
[Custom Ink]: http://www.customink.com/
[React JS]: http://facebook.github.io/react/