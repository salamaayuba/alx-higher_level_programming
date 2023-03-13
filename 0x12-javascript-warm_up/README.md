avaScript basics
Previous
Overview: Getting started with the web
Next
JavaScript is a programming language that adds interactivity to your website. This happens in games, in the behavior of responses when buttons are pressed or with data entry on forms; with dynamic styling; with animation, etc. This article helps you get started with JavaScript and furthers your understanding of what is possible.

What is JavaScript?
JavaScript is a powerful programming language that can add interactivity to a website. It was invented by Brendan Eich.

JavaScript is versatile and beginner-friendly. With more experience, you'll be able to create games, animated 2D and 3D graphics, comprehensive database-driven apps, and much more!

JavaScript itself is relatively compact, yet very flexible. Developers have written a variety of tools on top of the core JavaScript language, unlocking a vast amount of functionality with minimum effort. These include:

Browser Application Programming Interfaces (APIs) built into web browsers, providing functionality such as dynamically creating HTML and setting CSS styles; collecting and manipulating a video stream from a user's webcam, or generating 3D graphics and audio samples.
Third-party APIs that allow developers to incorporate functionality in sites from other content providers, such as Twitter or Facebook.
Third-party frameworks and libraries that you can apply to HTML to accelerate the work of building sites and applications.
It's outside the scope of this article—as a light introduction to JavaScript—to present the details of how the core JavaScript language is different from the tools listed above. You can learn more in MDN's JavaScript learning area, as well as in other parts of MDN.

The section below introduces some aspects of the core language and offers an opportunity to play with a few browser API features too. Have fun!

A "Hello world!" example
JavaScript is one of the most popular modern web technologies! As your JavaScript skills grow, your websites will enter a new dimension of power and creativity.

However, getting comfortable with JavaScript is more challenging than getting comfortable with HTML and CSS. You may have to start small, and progress gradually. To begin, let's examine how to add JavaScript to your page for creating a Hello world! example. (Hello world! is the standard for introductory programming examples.)

Warning: If you haven't been following along with the rest of our course, download this example code and use it as a starting point.

Go to your test site and create a new folder named scripts. Within the scripts folder, create a new text document called main.js, and save it.
In your index.html file, enter this code on a new line, just before the closing </body> tag:
<script src="scripts/main.js"></script>
Copy to Clipboard
This is doing the same job as the <link> element for CSS. It applies the JavaScript to the page, so it can have an effect on the HTML (along with the CSS, and anything else on the page).
Add this code to the main.js file:
const myHeading = document.querySelector("h1");
myHeading.textContent = "Hello world!";
Copy to Clipboard
Make sure the HTML and JavaScript files are saved. Then load index.html in your browser. You should see something like this:
Heading "hello world" above a firefox logo
Note: The reason the instructions (above) place the <script> element near the bottom of the HTML file is that the browser reads code in the order it appears in the file.

If the JavaScript loads first and it is supposed to affect the HTML that hasn't loaded yet, there could be problems. Placing JavaScript near the bottom of an HTML page is one way to accommodate this dependency. To learn more about alternative approaches, see Script loading strategies.

What happened?
The heading text changed to Hello world! using JavaScript. You did this by using a function called querySelector() to grab a reference to your heading, and then store it in a variable called myHeading. This is similar to what we did using CSS selectors. When you want to do something to an element, you need to select it first.

Following that, the code set the value of the myHeading variable's textContent property (which represents the content of the heading) to Hello world!.

Note: Both of the features you used in this exercise are parts of the Document Object Model (DOM) API, which has the capability to manipulate documents.

Language basics crash course
To give you a better understanding of how JavaScript works, let's explain some of the core features of the language. It's worth noting that these features are common to all programming languages. If you master these fundamentals, you have a head start on coding in other languages too!

Warning: In this article, try entering the example code lines into your JavaScript console to see what happens. For more details on JavaScript consoles, see Discover browser developer tools.

Variables
Variables are containers that store values. You start by declaring a variable with the let keyword, followed by the name you give to the variable:

let myVariable;
Copy to Clipboard
A semicolon at the end of a line indicates where a statement ends. It is only required when you need to separate statements on a single line. However, some people believe it's good practice to have semicolons at the end of each statement. There are other rules for when you should and shouldn't use semicolons. For more details, see Your Guide to Semicolons in JavaScript.

You can name a variable nearly anything, but there are some restrictions. (See this section about naming rules.) If you are unsure, you can check your variable name to see if it's valid.

JavaScript is case sensitive. This means myVariable is not the same as myvariable. If you have problems in your code, check the case!

After declaring a variable, you can give it a value:

myVariable = "Bob";
Copy to Clipboard
Also, you can do both these operations on the same line:

let myVariable = "Bob";
Copy to Clipboard
You retrieve the value by calling the variable name:

myVariable;
Copy to Clipboard
After assigning a value to a variable, you can change it later in the code:

let myVariable = "Bob";
myVariable = "Steve";
Copy to Clipboard
Note that variables may hold values that have different data types:

Variable	Explanation	Example
String	This is a sequence of text known as a string. To signify that the value is a string, enclose it in single or double quote marks.	let myVariable = 'Bob'; or
let myVariable = "Bob";
Number	This is a number. Numbers don't have quotes around them.	let myVariable = 10;
Boolean	This is a True/False value. The words true and false are special keywords that don't need quote marks.	let myVariable = true;
Array	This is a structure that allows you to store multiple values in a single reference.	let myVariable = [1,'Bob','Steve',10];
Refer to each member of the array like this:
myVariable[0], myVariable[1], etc.
Object	This can be anything. Everything in JavaScript is an object and can be stored in a variable. Keep this in mind as you learn.	let myVariable = document.querySelector('h1');
All of the above examples too.
So why do we need variables? Variables are necessary to do anything interesting in programming. If values couldn't change, then you couldn't do anything dynamic, like personalize a greeting message or change an image displayed in an image gallery.

Comments
Comments are snippets of text that can be added along with code. The browser ignores text marked as comments. You can write comments in JavaScript just as you can in CSS:

/*
Everything in between is a comment.
*/
Copy to Clipboard
If your comment contains no line breaks, it's an option to put it behind two slashes like this:

// This is a comment
