# CSS Media Queries

 <a href="#">iPhone</a> ~ <a href="#ipad">iPad</a> ~ <a href="#macbook">Macbook</a> ~ <a href="#apple-watch">Apple Watch</a> ~ <a href="#galaxy">Galaxy</a> ~ <a href="#galaxy-tab">Galaxy Tabs</a>

## iPhone 4 && 4s

<pre><code>@media only screen 
  and (min-device-width: 320px) 
  and (max-device-width: 480px)
  and (-webkit-min-device-pixel-ratio: 2) {
}</code></pre>

####Portrait

<pre><code>@media only screen 
  and (min-device-width: 320px) 
  and (max-device-width: 480px)
  and (-webkit-min-device-pixel-ratio: 2)
  and (orientation: portrait) {
}</code></pre>

####Landscape

<pre><code>@media only screen 
  and (min-device-width: 320px) 
  and (max-device-width: 480px)
  and (-webkit-min-device-pixel-ratio: 2)
  and (orientation: landscape) {
}</code></pre>

## iPhone 5 && 5s


<pre><code>@media only screen 
  and (min-device-width: 320px) 
  and (max-device-width: 568px)
  and (-webkit-min-device-pixel-ratio: 2) {
}</code></pre>

####Portrait

<pre><code>@media only screen 
  and (min-device-width: 320px) 
  and (max-device-width: 568px)
  and (-webkit-min-device-pixel-ratio: 2)
  and (orientation: portrait) {
}</code></pre>

####Landscape

<pre><code>@media only screen 
  and (min-device-width: 320px) 
  and (max-device-width: 568px)
  and (-webkit-min-device-pixel-ratio: 2)
  and (orientation: landscape) {
}</code></pre>

## iPhone 6

<pre><code>@media only screen 
  and (min-device-width: 375px) 
  and (max-device-width: 667px) 
  and (-webkit-min-device-pixel-ratio: 2) { 
}</code></pre>

####Portrait

<pre><code>@media only screen 
  and (min-device-width: 375px) 
  and (max-device-width: 667px) 
  and (-webkit-min-device-pixel-ratio: 2)
  and (orientation: portrait) { 
}</code></pre>

####Landscape

<pre><code>@media only screen 
  and (min-device-width: 375px) 
  and (max-device-width: 667px) 
  and (-webkit-min-device-pixel-ratio: 2)
  and (orientation: landscape) { 
}</code></pre>

##iPhone 6+

<pre><code>@media only screen 
  and (min-device-width: 414px) 
  and (max-device-width: 736px) 
  and (-webkit-min-device-pixel-ratio: 3) { 
}</code></pre>

####Portrait

<pre><code>@media only screen 
  and (min-device-width: 414px) 
  and (max-device-width: 736px) 
  and (-webkit-min-device-pixel-ratio: 3)
  and (orientation: portrait) { 
}</code></pre>

####Landscape

<pre><code>@media only screen 
  and (min-device-width: 414px) 
  and (max-device-width: 736px) 
  and (-webkit-min-device-pixel-ratio: 3)
  and (orientation: landscape) { 
}</code></pre>


<div id="ipad"></div>#Ipads



## iPad mini

<pre><code>@media only screen 
  and (min-device-width: 768px) 
  and (max-device-width: 1024px) 
  and (-webkit-min-device-pixel-ratio: 1) {
}</code></pre>

####Portrait

<pre><code>@media only screen 
  and (min-device-width: 768px) 
  and (max-device-width: 1024px) 
  and (orientation: portrait) 
  and (-webkit-min-device-pixel-ratio: 1) {
}</code></pre>

####Landscape

<pre><code>@media only screen 
  and (min-device-width: 768px) 
  and (max-device-width: 1024px) 
  and (orientation: landscape) 
  and (-webkit-min-device-pixel-ratio: 1) {
}</code></pre>



## iPad 1 and 2

<pre><code>@media only screen 
  and (min-device-width: 768px) 
  and (max-device-width: 1024px) 
  and (-webkit-min-device-pixel-ratio: 1) {
}</code></pre>

####Portrait

<pre><code>@media only screen 
  and (min-device-width: 768px) 
  and (max-device-width: 1024px) 
  and (orientation: portrait) 
  and (-webkit-min-device-pixel-ratio: 1) {
}</code></pre>

####Landscape

<pre><code>@media only screen 
  and (min-device-width: 768px) 
  and (max-device-width: 1024px) 
  and (orientation: landscape) 
  and (-webkit-min-device-pixel-ratio: 1) {
}</code></pre>



## iPad 3 and 4

<pre><code>@media only screen 
  and (min-device-width: 768px) 
  and (max-device-width: 1024px) 
  and (-webkit-min-device-pixel-ratio: 2) {
}</code></pre>

####Portrait

<pre><code>@media only screen 
  and (min-device-width: 768px) 
  and (max-device-width: 1024px) 
  and (orientation: portrait) 
  and (-webkit-min-device-pixel-ratio: 2) {
}</code></pre>

####Landscape

<pre><code>@media only screen 
  and (min-device-width: 768px) 
  and (max-device-width: 1024px) 
  and (orientation: landscape) 
  and (-webkit-min-device-pixel-ratio: 2) {

}</code></pre>



<div id="macbook"></div># Laptops

#### Non-Retina Screens

<pre><code>@media screen 
  and (min-device-width: 1200px) 
  and (max-device-width: 1600px) 
  and (-webkit-min-device-pixel-ratio: 1) { 
}</code></pre>

#### Retina Screens

<pre><code>@media screen 
  and (min-device-width: 1200px) 
  and (max-device-width: 1600px) 
  and (-webkit-min-device-pixel-ratio: 2)
  and (min-resolution: 192dpi) { 
}</code></pre>



<div id="apple-watch"></div># Wearables

#### Apple Watch

<pre><code>@media
  (max-device-width: 42mm)
  and (min-device-width: 38mm) { 
}</code></pre>


<div id="galaxy"></div>#Galaxy Phones


## Galaxy S3

<pre><code>@media screen 
  and (device-width: 320px) 
  and (device-height: 640px) 
  and (-webkit-device-pixel-ratio: 2) {
}</code></pre>

####Portrait

<pre><code>@media screen 
  and (device-width: 320px) 
  and (device-height: 640px) 
  and (-webkit-device-pixel-ratio: 2) 
  and (orientation: portrait) {
}</code></pre>

####Landscape

<pre><code>@media screen 
  and (device-width: 320px) 
  and (device-height: 640px) 
  and (-webkit-device-pixel-ratio: 2) 
  and (orientation: landscape) {
}</code></pre>



## Galaxy S4

<pre><code>@media screen 
  and (device-width: 320px) 
  and (device-height: 640px) 
  and (-webkit-device-pixel-ratio: 3) {
}</code></pre>

####Portrait

<pre><code>@media screen 
  and (device-width: 320px) 
  and (device-height: 640px) 
  and (-webkit-device-pixel-ratio: 3) 
  and (orientation: portrait) {
}</code></pre>

####Landscape

<pre><code>@media screen 
  and (device-width: 320px) 
  and (device-height: 640px) 
  and (-webkit-device-pixel-ratio: 3) 
  and (orientation: landscape) {
}</code></pre>



## Galaxy S5 && S6

<pre><code>@media screen 
  and (device-width: 360px) 
  and (device-height: 640px) 
  and (-webkit-device-pixel-ratio: 3) {
}</code></pre>

####Portrait

<pre><code>@media screen 
  and (device-width: 360px) 
  and (device-height: 640px) 
  and (-webkit-device-pixel-ratio: 3) 
  and (orientation: portrait) {
}</code></pre>

####Landscape

<pre><code>@media screen 
  and (device-width: 360px) 
  and (device-height: 640px) 
  and (-webkit-device-pixel-ratio: 3) 
  and (orientation: landscape) {
}</code></pre>


<div id="galaxy-tab"></div> #Galaxy Tabs

## Galaxy Tab 10.1

<pre><code>@media 
  (min-device-width: 800px) 
  and (max-device-width: 1280px) {
}</code></pre>

####Portrait

<pre><code>@media 
  (max-device-width: 800px) 
  and (orientation: portrait) { 
}</code></pre>

####Landscape

<pre><code>@media 
  (max-device-width: 1280px) 
  and (orientation: landscape) { 
}</code></pre>



## Asus Nexus 7

<pre><code>@media screen 
  and (device-width: 601px) 
  and (device-height: 906px) 
  and (-webkit-min-device-pixel-ratio: 1.331) 
  and (-webkit-max-device-pixel-ratio: 1.332) {
}</code></pre>

####Portrait

<pre><code>@media screen 
  and (device-width: 601px) 
  and (device-height: 906px) 
  and (-webkit-min-device-pixel-ratio: 1.331) 
  and (-webkit-max-device-pixel-ratio: 1.332) 
  and (orientation: portrait) {
}</code></pre>

####Landscape

<pre><code>@media screen 
  and (device-width: 601px) 
  and (device-height: 906px) 
  and (-webkit-min-device-pixel-ratio: 1.331) 
  and (-webkit-max-device-pixel-ratio: 1.332) 
  and (orientation: landscape) {
}</code></pre>


