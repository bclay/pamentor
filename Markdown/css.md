<div class="hidden"><meta property="og:image" content="http://the-dining-philosophers.github.io/code-weekend/assets/img/logo.png"><link rel="shortcut icon" href="assets/images/favicon.png"><link rel="stylesheet" href="http://netdna.bootstrapcdn.com/font-awesome/4.0.3/css/font-awesome.css"><link rel="stylesheet" href='http://fonts.googleapis.com/css?family=Open+Sans:300italic,400italic,600italic,700italic,400,300,600,700' type='text/css'><link rel="stylesheet" href="assets/css/typography.css"><link rel="stylesheet" href="assets/css/markdown.css"></div><div class="nav-items"><div class="nav-item" id="setup-menu">Intro</div><div class="nav-item" id="node-menu">CSS</div><div class="nav-item" id="apis-menu">Bootstrap</div><div class="nav-item" id="dbs-menu">Resources</div></div>

Web Design 101
============
Building your first (pretty) website
--------------------------

Intro to Websites <a id="setup-section"></a>
==================================
The first steps to making your website beautiful
------------------------------------

Welcome coders of all levels! Feel free to check out the [Code Weekend](the-dining-philosophers.github.io/code-weekend) website for a quick overview of HTML, CSS, and Javascript. In case you missed it, here's how the three come together to make websites work:

### What are HTML, CSS, and Javascript?

HTML (Hypertext Markup Language) is like the backbone of any webpage. It's where we add in all the information - what they webpage actually displays as well as information about the page itself such as its title.

CSS dresses up this information. Most (but really all) webpages link to a CSS file that stores information on how a browser should display the information it recieves in the HTML. While it is possible to add CSS code into the HTML document, it is never done as it makes it nearly impossible to keep track of code and also slows down the page.

Javascript is the fun part. It does dynamic things with your webpage, updates content on the fly and can animate just about anything. We'll talk about this later.

HTML <a id="node-section"></a>
==================================

HTML stands for HyperText Markup Lanuage. It is HyperText because it hyperlinks you to other text. It is a markup language because it is not written as plain text. It is marked up into the form of HTML elements called tags.

### What is the DOM?

Every webpage is built in the HTML DOM (Document Object Model). This means that every element in the HTML code is an element (or a Node, the mathematical kind - not to be confused with Node.JS). So we could call this paragraph an element in the DOM; the same is true of any of the images and pretty much everything else here.

![The DOM](http://courses.cs.washington.edu/courses/cse190m/07sp/lectures/slides/images/dom_tree.gif)


CSS <a id="node-section"></a>
==================================
Does your website have style?
------------------------------------

CSS is a really funny language with a lot of oddities. I'll go through a few of them here:

### Cascading

CSS stands for "Cascading Style Sheets". Go back to the idea of a DOM, and envision a website as a tree. "Cascading" just means that the same element can have the same property set to different values in different places (perhaps in different CSS files), but the most specific setting is the one followed on the page.

For example, your CSS may set all body text in the body tag to blue, but text surrounded by an h1 tag is set to black. The text will end up being black, since the h1 tag is more specific than the body tag.

### Margins and Padding

Roughly speaking, setting margins and padding to particular values will give cushions of space around your content. In general it won't matter which you set, but technically the margin is outside the "border" and the padding is within it. You can generally specifiy which margin/padding to set, or uniformly set them in every direction.

![Margins, Borders, and Padding](http://i.stack.imgur.com/PeSIJ.gif)

You should almost always put some kind of margin/padding around text. It's really difficult to read when words stretch all the way out to the edge of a box or page, so your eyes will appreciate the white space.

### Sizes

Sizes of elements can be set and adjusted in several ways.

- You can set exact sizes of elements by indicating the number of pixels you want it to take up (notated _px_). For example, a box can be _100px_ wide.

- It's good practice to set sizes using a percentage, which indicates what percent of the page you want your element to take up. A bar that stretches across the page would have a width property of _100%_. Using percentages makes your page responsive to the initial window size.

- _em_ can be used for fonts to indicate sizes relative to the original settings. For example, you can set a font size to _2em_, which will make it twice as big as it originally was.

### Colors

Colors can generally be set by just indicting a color name. To get a really specific color, you can use a color selector to find the hexadecimal representation of a color. Hexadecimal values are between 0 and 9 or a and f. The numbers are equivalent to, well, themselves, and the letters are two-digit numbers (a=10, b=11, c=12, et cetera). For example, _#1bb99a_ is the shade of green we use on the PennApps website. People generally use "color pickers" to find the hexadecimal version fo the colors they want.

If you want to change a box color, alter the _background_ property. Text color can be changed with the _color_ property.

### Aligning

Just like a Word document, you can align text and objects to the left, right, or center of a page. 

### Floating

You can set elements to "float" to some part of the page. For example, if you'd like to see a picture on the left of a text box, you can set _float:left;_. Be careful—there are a ton of nuances here.

### Animating

Yes, you can actually animate your CSS code. Blow is an animation that causes a circle to blink red:

	@keyframes blink {
  		50% {
    		background: radial-gradient(circle, red 15%, transparent 40%), #cc5;
  		}
	}

	/* in the actual CSS element */
	animation: blink .5s infinite;

Keyframes are just different snapshots of your animation. In the blinking example, the original keyframe is a white circle, and the second keyframe is a red circle.

Bootstrap <a id="api-section"></a>
==================================
The easiest shortcut to good design
------------------------------------

Poke around on [Bootstrap](http://getbootstrap.com/). There are two main ways to use it in a website.

- _Borrow Elements_: You can use page elements straight from Bootstrap, such as buttons, navigation bars, search bars, et cetera.

- _Adapt a Template_: You can take entire templates built by Bootstrap and change them for your own purposes.

You're welcome to download Bootstrap, but it's probably easier just to link to the website you want (or download just the files you want off the Internet).

Resources <a id="api-section"></a>
==================================
Time to realize that thievery isn't always wrong
------------------------------------

There are tons of resources out there to help with CSS and design:

- [W3Schools](http://www.w3schools.com/) is essentially the online dictionary of CSS.

- [Dash](https://dash.generalassemb.ly) has really great tutorials for learning CSS.

- [Treehouse](https://teamtreehouse.com/signup_code/hackru)



This guide was provided by Brynn Claypoole.

<div class="footer"><p>&copy; PennApps 2014. Page design by <a href="http://pvrnav.com">Pranav Vishnu Ramabhadran</a>. Workshop designed by <a href="http://github.com/bclay/">Brynn Claypoole</a>.</div>

<script src="http://code.jquery.com/jquery-1.11.0.min.js"></script>
<script src="assets/js/nav.js"></script>
<script src="assets/js/FlowType.js"></script>
<script type="text/javascript">
    $('body').flowtype({
        minimum   : 500,
        maximum   : 1000,
        minFont   : 16,
        maxFont   : 65,
        fontRatio : 40
    });
</script>
<script>
    $(window).load(function(){
        $('.loading').fadeOut('200');
    });
</script>