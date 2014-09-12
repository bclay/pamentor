<div class="hidden"><meta property="og:image" content="http://the-dining-philosophers.github.io/code-weekend/assets/img/logo.png"><link rel="shortcut icon" href="assets/images/favicon.png"><link rel="stylesheet" href="http://netdna.bootstrapcdn.com/font-awesome/4.0.3/css/font-awesome.css"><link rel="stylesheet" href='http://fonts.googleapis.com/css?family=Open+Sans:300italic,400italic,600italic,700italic,400,300,600,700' type='text/css'><link rel="stylesheet" href="assets/css/typography.css"><link rel="stylesheet" href="assets/css/markdown.css"></div>

OOP && Java <a id="setup-section"></a>
==================================

### What is Object-Oriented Programming?
In essence, object-oriented programming (OOP) is a programming paradigm where data and the functions (often called methods) to use the data are connected. The data and its associated methods are packaged together in a single unit, called an object. Because of this, the main program in many OOP apps is often small, instead simply instantiating (creating) several objects and then calling their associated methods to make them interact.

###What is Java?

Java is a multi-faceted object-oriented programming language designed to allow developers to “write once, run anywhere”. When Java code is compiled, it is not converted to machine code like in many other languages; instead, it is converted to Java “bytecode”; this bytecode is then executed on the Java Virtual Machine, a program which is available for a wide variety of platforms. As result, Java can be run in the same way on any machine with the JVM installed. While sometimes maligned for being syntactically verbose, Java is nonetheless a popular language with millions of developers and hundreds of millions of users. Developed in the early 90’s by Sun Microsystems (now a part of Oracle), Java is one of the most widely used languages for apps of any size!

###Hello the Hard Way

Here is an example of a rather complex “Hello World!” program in Java. In this example, we will take advantage of the extensive Java Swing library, an extensive GUI library which can be used in a wide variety of apps. (All credit to Wikipedia for the program)
import javax.swing.JFrame;  //Importing class JFrame
import javax.swing.JLabel;  //Importing class JLabel
public class HelloWorld {
    	public static void main(String[] args) {
            	JFrame frame = new JFrame();       	//Creating frame
            	frame.setTitle("Hi!");             	//Setting title frame
            	frame.add(new JLabel("Hello, world!"));//Adding text to frame
            	frame.pack();                      	//Set size to smallest
            	frame.setLocationRelativeTo(null); 	//Centering frame
            	frame.setVisible(true);            	//Showing frame
    	}
}
 
Though seemingly complex, this program will allow us to examine the ways the object-oriented features of Java work.

First, note the “import” statements up at the top. Like “include” in C, this instructs the compiler to compile the public libraries for javax.swing.JFrame and javax.swing.JLabel (Note: if we wanted to include ALL of the swing library, we could have used “import javax.swing.* ”).
Next, notice the line “public static void main(String[] args) { ”. While it is not vital to know what every word in this line means, it suffices to say that this line must appear once, and only once, in every Java program. We call this the “main method” and it begins the execution of every Java program. Once inside the main method, we will make calls to other objects to finish the logic of our program.

Next, notice the line “JFrame frame = new JFrame();”. This line provides an example of the essence of OOP. Somewhere else, the library JFrame has been created. In our program, we want to use the JFrame to display our image. Therefore, after importing the package, we have to make a JFrame; to do so, we start by declaring to the compiler that we are making a new JFrame named frame (i.e. “JFrame frame”). Next, we associate that JFrame with a JFrame which we instantiate (create) using the “new” keyword (i.e. “ new JFrame()”). After this line is executed, we have a fully functioning JFrame object called frame which we can manipulate later.

Next, notice the line “frame.setTitle(“Hi!”);”. This allows us to see two more important Java characteristics. First, methods (like “setTitle” are passed as follows: “objectName.methodName(argumentsToMethod)”). Second, notice the camelCase. This is just common Java style for naming. Instead of separating multiple words in a method name or object name, we use the notation firstSecondThirdEtc to differentiate between different words in the name.

We won’t explain the entire rest of the program here, but use the tips here to dissect and absorb it!

###Java Resources
http://docs.oracle.com/javase/tutorial/
http://www.oracle.com/technetwork/topics/newtojava/overview/index.html
http://en.wikipedia.org/wiki/Javadoc
http://www.java.com/en/download/faq/whatis_java.xml
http://en.wikipedia.org/wiki/Java_(programming_language)
 

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
