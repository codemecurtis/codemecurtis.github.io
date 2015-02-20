---
layout: post
title: "Stay Starped with Jekyll and Twitter Bootstrap"
date: 2015-02-19
author: Curtis Seaton
categories: Technical

---

I am going to put the fair warning out there I don't know just how short I can keep this post. At the beginning of the week I took a look at Jekyll played around with it and couldn't get what I wanted in the time that I wanted so I went on to the good ol [Twitter Bootstrap][Twitter Bootstrap]. If you don't know what bootstrap is it is a html, css and JS framework that allows you to rapidly prototype websites.

###[Twitter Bootstrap][Twitter Bootstrap]
I had built my desired design in static html in week 4 or so, I had an idea on what I wanted to do. With a few tweaks here and there I had the design I was looking for. I ran into a lot of issues with the skills section. I wasn't all to familiar with [Twitter Bootstrap][Twitter Bootstrap] so I took a look at the documentation and quickly found their grid system. After changing from ```col-md-5``` to ```col-md-4``` I had the inline style I was looking for but it wasn't centered, great another problem. Quickly took a look at chrome dev tools and realized I need to add some empty column on each side.

The CSS on this was very simple with bootstrap. I used about 120 lines of CSS for both the desktop and responsive code, yes this website is mobile friendly so go grab your iPad, iPhone, android and go take a look. I had the most fun working with the image rotation on the homepage, I used a couple different CSS attributes such as ```transform```, ```transition```, and more. There is not one bit of javascript making the image flip, well appear to flip. I don't want to go into to much detail so we will keep it at that.

Next issue was the mobile friendly CSS, this wasn't as bad As doing it from scratch because [Twitter Bootstrap][Twitter Bootstrap] has already thought of this for us this is where the html classes ```col-md```, ```col-sm```, ```col-lg``` these have to do with the way the responsive design will be handled. This brings me to my next issue with the skills section, On a vertical iPad they were stacking on top of each other which I was not a fan of but for some reason in the landscape view it was fine, great get out the hood of docs again. Duh, ```col-sm``` and ```col-md``` this has to play with the CSS so if we want them to be in columns on a sm(Small) device then use the ```col-sm```, genius!

I also used [Google Fonts][Google Fonts] & [Font Awesome][Font Awesome]


By the end of everything I was very satisfied with the mobile and the desktop versions. Images are crisp, text readable, color scheme matching but what about the blog, who wants to make a html post every time a new blog is due or add each link every time, nope ok back to Jekyll, I felt I did my homepage pretty quick so why not take a fresh look.

###[Jekyll][Jekyll]
Jekyll is simple a framework to turn your plain text into static websites and blogs. It is great because of a couple different reasons. As I mentioned before I did not plan on completing this challnge in Jekyll however it was almost neccessary after doing so much work on the homepage. What was ahead of me may have changed my mind had I know I was going to ahve these issues.

-1. You don't have to worry about any databases
-2. Built on the Ruby framework
-3. Fast and when I say fast I mean blazing
-4. Post can be written in Mardown, Textile, Liquid and HTML & CSS

After getting through the install process with a breeze I ran into my first hiccup, Understanding the file and folder structure. I am familiar with NVC file structure but the more and more I look at them not 1 languages file and folder structure is the same. Luck for me there are [Jekyll Docs][Jekyll Docs]. Jekyll's main files use are in the ```_layout``` and ```_includes``` folder. I am sure you can figure out what these are but in the ```_layout``` folder
it has out blog index page, post and page layouts. The ```_include``` folder contains the header, footer and head tag which allows for all pages to dynamically get connent through something called handlebars which is a HTML extender. Let me not forget about the ```_post``` folder which of course holds all the markdown posts.

Adding a new CSS file was fun J/K. I first started by creating a new file in the ```_site/css/``` folder but everytime I ran ```jekyll serve``` it would remove the file from the directory. I assumed it was thank I did not link the file in the head file, so off to add that which was relativley simple using their main.css link. Still didn't work so i noticed another folder which had a .scss file extension I knew this was [Sass][Sass] so I was hesitant to add the file but I did anyways, updated the head link and ran ```jekyll serve``` wha lah everything was still there and I could see an empty file for this link, so I added some CSS everything still worked. I quickly got a ove on this tweaking the header and content but that is enough of that I am trying to keep this short for mine and your sake.


Ok so we got Jekyll running in one directory and we have bootstrap running in another directory so in therory the next step is to combine the 2 into 1 beautiful cohesive unit. Oh how is sounds so appealing but we have a few issues here. Bootstrap and Jekyll both look for the index.html file for the homepage.Ok no problem we will put the jekyll files in to a subdirectory called blog and eveyrhting will work, WRONG! For starters I couldn't figure out how to test this locally so I tried pushing it up to [Github pages][Github pages] and received an email almost instantly saying hey bud this isn't going to work because of the main.scss file great freaking [Sass][Sass] is out to get me again.

I searched on the web and fount that I needed to add a samll piece of coe tried that and still nothing. After about 20 commits I came across a post which said that he was expiereincing the issue but that Jekyll needed to be in the root directory. We this brings me back to my original index page so i change the name of that file real quick solve an issue with the ```_config.yaml``` file and finally I have my blog up! However this si not what I am looking for I want my homepage back.

I took a couple hour break did a pairing on some Ruby stuff and came back with the genius idea to change the name of the jekyll index and put the old file back, commit & push this and the homepage is there! No way can't be that easy so i renamed the blog index to take a guess..... blog.html I changed the blog link on the homepage to the right file. Commit, Push and refresh everything is still working but the all so coveted blog link, I click it and takes me exactly to what I wanted. I could not believe it was that easy.


Needless to say there was a whole bunch of trial and error here but all in all I am absolutely in love with my new website that I can't wait to finish this post and see how much time I am going to save on each and every post. Bootstrap, Jekyll and Google fonts will allow me to keep a streamlined view on all devices and browser which as a developer you could not ask for anything more. As always I have future versions pre planned and other updates I want to do but hey time is a venture and with DBC starting on Monday I think I better get my head into some JS and Ruby.


[Twitter Bootstrap]: http://getbootstrap.com/
[Google Fonts]: https://www.google.com/fonts/
[Font Awesome]: http://fortawesome.github.io/Font-Awesome/
[Jekyll]: http://jekyllrb.com/
[Jekyll Docs]: http://jekyllrb.com/docs/home/
[Sass]: http://sass-lang.com/
[Github pages]: https://pages.github.com/