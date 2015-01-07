<div class="hidden"><meta property="og:image" content="http://2015s.pennapps.com/assets/images/logo.png"><link rel="shortcut icon" href="http://2015s.pennapps.com/assets/images/logo.png"><link rel="stylesheet" href="assets/css/global.css"><link rel="stylesheet" href="http://netdna.bootstrapcdn.com/font-awesome/4.0.3/css/font-awesome.css"><link rel="stylesheet" href='http://fonts.googleapis.com/css?family=Open+Sans:300italic,400italic,600italic,700italic,400,300,600,700' type='text/css'></div><div class="nav-items"><a href="index.html"><img src="assets/img/logo.svg"></a><a href="#why-chrome-devtools" class="nav-item">Why Chrome</a><a href="#in-depth-guide-to-all-your-devtools-needs" class="nav-item">Guide</a><a href="#opening-up-devtools" class="nav-item">Opening</a><a href="#chrome-devtools-tabs" class="nav-item">The Tabs</a><a href="#elements-tab" class="nav-item">Elements Tab</a><a href="#sources-tab-and-the-debugger" class="nav-item">Sources and Debugger</a><a href="#javascript-console" class="nav-item">The Console</a><a href="#conclusion-and-further-resources" class="nav-item">Conclusion &amp; Resources</a></div>
 
Chrome DevTools for Debugging <a id="setup-section"></a>
==================================
The first steps to making your website.
--------------------------


### Why Chrome DevTools?


Be it a hackathon or an internship, being good at debugging is an extremely useful skill to have. It’s very rare that a program you write runs perfectly the first time you write it, and therefore as coders we have to spend a lot of time debugging and trying to identify what parts of the code cause problems in our program. IDEs(Integrated Development Environments) like Eclipse provide users with built in debuggers to make this process easier, but what do you do when it comes to web programming? Most people use a text editor like Sublime when programming for the web, and these editors don’t come with powerful debugging capabilities. 

Especially at a hackathon like PennApps where time is very valuable, you wouldn’t want to waste 10 hours trying to figure out what’s wrong with your code. Luckily, Chrome has very powerful and easy to use tools built in for debugging purposes. Other browsers have tools similar to this too, however I had a fairly easy time starting out with Chrome DevTools due to the great resources available on the web. 

So now that we know why Chrome DevTools could be a valuable resource, let’s begin!

###An In-Depth Guide to All Your DevTools Needs

The guide you’re reading now will be covering some of the most basic and important features of DevTools. If you happen to have a couple of hours free, and would like to delve more into the capabilities of DevTools, I strongly recommend taking this free Code School course. It’s basically a series of short videos that explain different features of DevTools, all followed with a Challenge section that gets you to actually use that feature. It’s very informative and easy to follow, and by the end you will have a much better idea of how to use DevTools to your advantage.

If you don’t think you have the time, don’t worry. This guide assumes this is your first time working with Chrome DevTools.

###Opening up DevTools

After opening up Chrome, there are two ways you could pull up DevTools.

First way: Click the icon on the top right of your Chrome window (three horizontal lines lined up vertically), go to Tools → Developer Tools






Second way: You can also Right Click anywhere on the screen and select Inspect Element.




You should get something like this on the bottom half of your screen: 





###Chrome DevTools Tabs

Now that you have DevTools open, let’s take a look at the tab names and what they are primarily used for.

Elements - This is the tab that’s currently open on the screenshot above. It’s used to see the different HTML elements on your document along with the CSS properties that apply to them. One of the great features the Elements panel offers is the ability to live-edit HTML or CSS and see the changes immediately reflected on your browser. 

####Resources 
This tab shows the resources (HTML, CSS, JavaScript files, images, storage, etc)  that were loaded for your web page. We won’t be dealing a lot with this tab in this guide, however it’s useful to see whether you’re loading everything you want to the page and check other things such as the sizes of your images.

####Network 
I personally find this to be an incredibly useful panel. If you go to the Network panel and refresh your page, you will see all of the resources loaded for your page, along with their sizes, load times, and when they started loading. If something goes wrong with loading up a resource or another operation in your web app (such as an HTTP request), you will see a status code on this tab telling you what went wrong. This is a great way to see how long your web app takes to load up or how long different operations in your web app take to fire up. 

####Sources 
This is probably the tab I spend the most time in as I try to debug a web app I’m working on. You can use the JavaScript debugger built into Chrome DevTools through this tab. The debugger allows you to set breakpoints in certain parts of your code and shows you what the state of your web app is at a certain line in your program. 

####Timeline 
The timeline panel is mostly used for testing the performance of your web app. If you want to check with how much memory your web app is taking up or how fast it’s performing, it’s likely that you’ll use this tab. However, if you’re not dealing with a realtime app or a memory intensive app (such as a web app that makes use of 3D graphics) for the hackathon, you don’t need to worry about this tab for now.

####Profiles 
Another tab that’s mostly useful for inspecting performance. For instance, you can run a JavaScript CPU Profile for a certain amount of time and then see what functions take up how much time. In this case the JavaScript profile could be useful in spotting which functions seem to be the slowest in your app, and how you could go about making them faster.

####Audits 
This is basically a tab that offers you advice on how to improve your performance and network times. The terminology in some of these advices could be a bit confusing, so don’t worry about it if it doesn’t make a whole lot of sense. We won’t be focusing on this tab in this guide.

####Console 
This brings up a JavaScript console that you can interact with. It’s useful for testing out whether some of your methods work as expected, to inspect different elements in the DOM (Document Object Model), or to check some of your JavaScript objects.

Since this is more of an introductory guide to the most essential features of DevTools, I’ll try to explain to you some of the tools I use the most and how it could help you out when you’re working on your app. I’ll mostly focus on Elements and Sources, and touch a bit on Profiles and Console. Again, if you wish to check out all these features, I highly recommend the Code School course I posted earlier.


###Elements Tab

The Elements Tab is made up of two parts: the left side which shows the HTML elements in a nice tree format, and the right side which shows what styles and properties are applied to the currently selected HTML element. 

As you might have already noticed, if you hover your cursor over different HTML elements of the tree while in the Elements panel, you will see different parts of the page being highlighted in blue. This is a handy feature that allows the user to see which HTML element is currently being selected. Clicking on one of these elements will update the right part of the Elements tab to reflect the styles and properties that apply to the selected element.

Another really cool feature of this tree-view is that you can double click on any tag or text to edit it in your browser. This is very useful if you simply want to make a small change in your HTML and see what it does, since the change will be immediately reflected on your browser view. However keep in mind that the change you made will not be reflected in the code you have on your computer, so if you want to keep the change you have to go back and make the same change in your text editor.
 
Now let’s take a look at the right side of the elements panel. If you’re familiar with CSS, you will see that on the right side of the elements panel currently shows all the styles that apply to the selected element. It will show which styles are inherited from which elements, which could also be useful in figuring out weird bugs you have with your styling. Like the tree-view, you can edit styles and see their changes reflected on the page instantly. Simply click on the attribute name (like border-radius) or the value (like 30px) and edit it as you wish. For changing colors, Chrome offers you a color picker so you might find that useful too. You can also add your own attributes by simply clicking on the white space between the `{ }` brackets. 

In addition to that, the right panel also displays information about the margins and paddings of the given element, under Metrics. You can click on different parts of the different boxes to edit your margins, borders and paddings instantly. 

I believe that these are the most useful features of the Elements tab, but if you want more information or a more detailed explanation of the discussed features, you should check out this page on the Chrome Developers website.

###Sources Tab and the Debugger

First, I just want to briefly explain why you might find the DevTools JavaScript Debugger useful. As your web application gets bigger and bigger, you will have functions that call other functions, that call other smaller functions. You might have used print statements or console.log statements in the past to figure out which point the program runs up to. In smaller applications, this might be a fine way of debugging, but I assure you learning to work with a debugger will save you a lot of precious time. After you become comfortable with it, you will figure out bugs that would take hours to figure out with print statements in minutes. 

The basic concept to understand when using a debugger is the concept of breakpoints. The debugger allows you to set breakpoints on any line of code you want. After being set, a breakpoint will be triggered when the program runs up to that point. Triggering a breakpoint will freeze the application, and this is why it’s so useful to use them. 

At this point you can actually follow which lines are being called in your code by using the Step Over button, which will skip that line and go to the next line in your code that’s being called. Using Step Into will go into the function call that is on the current line. So let’s say you’re on a line that calls a function foo(), Step Over will skip over the call and take you to the next line of code, while Step Into will take you into foo. Step Out is the direct opposite of Step Into and will take you out of the function you’re currently in. 

Let’s say you set up two breakpoints far from each other, and your program came to the first one. If you don’t want to step over every line until the second break(although you certainly can), you can simply press the Play button to resume the program, until it triggers another breakpoint. The Pause and Play buttons can also be useful in situations where you have a game or animation that looks off in certain parts of gameplay, since you can just Pause and the program will pause at that state.

With what you know so far, you can see which lines of code are being executed in your code. However the real power of debugging comes from being able to see the state of every variable in your code when a breakpoint is triggered. When a breakpoint is triggered, the right panel of the Source tab will show you a list of variables or objects. You can actually go into these and observe what their state is at a given line of code. This is an incredibly useful feature, since you can pinpoint exactly what’s wrong with your code at a given line if you analyze all the variables involved and can tell what’s wrong with their values. 

This was more of an introduction to using a Debugger, because I wanted to direct you to the Chrome Developers page that has a great step by step guide on how to use the Debugger. I recommend reading through the “Debugging with Breakpoints” part. I don’t think you need to worry about the parts after that if this is your first time with debuggers or a browser debugger. The Code School course also does a great job in explaining how to use the Debugger in an interactive way. 


###JavaScript Console

The JavaScript console could be a useful tool in debugging, since if you have any console.log statements in your actual code, this is where you will see the output. I know I mentioned earlier that the debugger is much more powerful, however there are still times where going with some console.log statements could make sense. Let’s say there is a 3D animation in your web app, and you want to see how your object changes its position over time. You could set a breakpoint in your method that gets called every frame, and check the position using the debugger. However this could take a while and you might want to just see everything at once. A simple: `console.log(“Object position:” + object.position)` could be a much simpler way to see the change in position throughout the animation. The JavaScript Console would be where you would check the output of these calls. 

In addition to checking console.log output, you can also directly write into the JavaScript console. If you have an object called cube in your app, you could simply type in: `console.log(cube)` into your console and the console would output the properties of the object cube. Or let’s say you want to access an element in your HTML, you could simply type: `document.getElementById(“button”)` to get the element with the id of ”button”(If you’re familiar with jQuery, the Chrome JS console also works with statements like: `$(“#button”) )`.

Let’s say you want to test out whether a function you wrote, called foo, does what it’s supposed to. You could type: foo() into your console and see whether it works as it should. This can be a powerful tool if you end up having too many little functions in your app and you just want to test out whether one of these work right.

If you want to learn more about the JavaScript console, take a look at this Chrome Developers page. You can skip the “Using the Console API” part, but the “Basic operation” and “Using the Command Line API” parts contain some information that might help you out. 

###Conclusion and Further Resources

And with that, we’re done! I hope you found this guide as a helpful introduction to some of the most important features of Chrome DevTools. It might be a hard to get into it at first, but once you get in a habit of using Developer Tools (in any browser), it will save you a lot of time when debugging or when you’re just completely lost.

As I’ve said multiple times throughout this guide, if you want to learn more about DevTools, these two resources are very helpful:
1. Discover DevTools on Code School: Easy to understand, split up into different sections, each section followed by a simple yet effective interactive challenge.
2. Chrome Developers page on DevTools: This is the official documentation on DevTools, and if you want to know something about DevTools, it’s guaranteed to be on here. Some parts might talk about things you might not know, but don’t be intimidated by that. It contains information for both beginners and more advanced users of DevTools.

This information was created by [Emre](http://emretanirgan.com)

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
