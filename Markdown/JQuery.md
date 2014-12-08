<div class="hidden"><meta property="og:image" content="http://the-dining-philosophers.github.io/code-weekend/assets/img/logo.png"><link rel="shortcut icon" href="assets/images/favicon.png"><link rel="stylesheet" href="http://netdna.bootstrapcdn.com/font-awesome/4.0.3/css/font-awesome.css"><link rel="stylesheet" href='http://fonts.googleapis.com/css?family=Open+Sans:300italic,400italic,600italic,700italic,400,300,600,700' type='text/css'><link rel="stylesheet" href="assets/css/typography.css"><link rel="stylesheet" href="assets/css/markdown.css"></div>

JQuery

JQuery is a helpful Javascript library that makes possible to bring webpages to life without going insane. It provides helpers for DOM manipulation, event binding, AJAX requests, and even animations. JQuery is compatible with nearly all browsers (including oldies like IE) and has a wide range of plugins available that extend its functionality even further.

This guide will assume some knowledge of programming and HTML/CSS but extensive practice of Javascript will not be required to understand it. However, the better you know the language the more dangerous you’ll be when you sit down to program. For an excellent primer in the Javascript language (as well as a look at how miserable events are without JQuery!), [go here](http://eloquentjavascript.net/).

1. Getting set up
This part is easy. Just put 
<script src="//ajax.googleapis.com/ajax/libs/jquery/1.10.1/jquery.min.js"></script>
right before the </body> tag in your HTML. This loads the JQuery script  onto the page and lets you call its methods with $. Of course, can also provide it yourself rather than relying on Google, but this is the easiest way.

Right under that snippet, put another script tag, like so: 

<script>
    $(‘document’).ready(function(){
        //Your JQuery and Javascript code goes here
}); 
</script>

This tells JQuery to wait until the document is loaded, and then run whatever code you put in the body of the function.


2. DOM Manipulation

Check out the [HTML/CSS](./css.html) page to learn about the DOM.

JQuery makes it really easy to add, remove, and change DOM nodes. For instance, if we wanted to create a new <h2> element that said “PennApps rocks,” we would write

$(‘<h2>’).html(‘PennApps rocks’); 
Now, while this has created a new DOM node like we wanted, it isn’t actually inserted into the DOM anywhere. To do that, we would write:

var header = $(‘<h2>’).html(‘PennApps rocks’); 
$(‘body’).append(header);

This will insert the header at the very end of the body. If we had wanted it at the beginning, we could have used prepend. 

But for every yin, there must be a yang; and so to balance the power of insertion, we must wield the power of deletion. To remove the header element from the DOM: 

header.remove();

Finding nodes in the DOM

One of the most common tasks you’ll use JQuery for is finding all nodes in the DOM that match certain criteria. For instance, you might want to find all paragraphs in order to change their style or make some other changes.

For this, it helps to know some CSS selectors, because JQuery can find nodes just the same way a style sheet does. In CSS you could color all paragraphs red with:

p /* ← this is the selector! */ {
    color: red;
}

You could do the same thing in JQuery as well, in much the same way: 

$(‘p’).css(‘color’, ‘red’);

You use the same ‘p’ selector here as in the CSS, and in both it selected all <p> tags in the DOM. Two other common selectors are the class selector ‘.class-name’ and the id selector ‘#id-name.’ For a list of more advanced selectors in JQuery please see http://api.jquery.com/?s=selectors.

Method Chaining
It would be a real pain to have to write out the same selector over and over just to change multiple properties on an element. Luckily, JQuery has a neat trick; every one of its methods returns the original JQuery object that you create when you write the selector! This way, you can just chain the methods one after another, like so:

var myNode = $(‘#myID’).css(‘color’, ‘red’).attr(‘width’, ‘500px’).css(‘border’, ‘1px solid blue’); 

Event Binding (clicks, keypresses, and more)

JQuery makes it easy to make something happen when a user clicks the a button or presses a key. Once you’ve selected the node you want to bind the event to (either via selectors as shown above, or by creating the node in the Javascript and storing it as a variable), you can use the .click(), .keypress(), and a host of other event binding methods to do some seriously cool stuff. Google and Stack Overflow will be your best bet for finding out how to do something specific (like binding only to the ‘up’ arrow for example).

JQuery also supports touch events, although unfortunately not with a nice helper method like ‘click().’ You have to bind to touch events manually like so: 

$(‘#myButton’).on(‘touchstart’, function(){
    alert(‘You touched the button! Hooray!’);
});

This will open a popup window when a user touches the button with id=”myButton” (but not clicks with a mouse).

You can also use .on() to bind to custom events that you can name yourself. This can be really useful in a lot of situations; for instance, you might have a ‘save’ event that gets triggered every time the user clicks a save button. Here is an example of such a setup:

$(‘#savebutton’).on(‘save’, function(){
    alert(‘Saving’);
});
$(‘#savebutton’).trigger(‘save’); //Alerts ‘Saving’

This can be really useful for situations in which you need a few events, or you need a lightweight ‘event bus’ that you can hook into different parts of your application. Such a use case is actually a little beyond JQuery, but if you’re interested, check out some frameworks like Backbone that have a more robust event system keyed into model data.


Animations

Rather from simply inserting elements into the DOM, JQuery provides a few functions to make their entrance and exit a little more polished. The simplest of these are fadeIn() and fadeOut(), which are pretty self explanatory; the element is phased from invisible to visible, or vice-versa. But you can also program custom animations based on CSS properties via the animate() function, or chain multiple animate() calls. Now, with only JQuery loaded you can only animate numerical properties; but if you want to animate colors or other properties, you should check out some...

JQuery Plugins

JQuery is open source and fully extensible, and it has a lot of really great plugins to extend its core functionality. Some are pretty much libraries in their own right, like JQuery UI, a collection of extremely useful interactive components; some are much smaller and a lot less documented (such as verdict.js). Plugins can be loaded with a <script> tag the same way as JQuery itself, and there is virtually guaranteed to be a plugin for anything you can think of. 


<div class="footer"><p>&copy; PennApps 2014. Page design by <a href="http://pvrnav.com">Pranav Vishnu Ramabhadran</a>. Resources compiled by PennApps Mentoring.</div>

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