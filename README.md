# Introduction to JavaScript

JavaScript is a programming language that is used to add interactivity to web pages. These notes provide a basic introduction to some simple JavaScript statements and how to add JavaScript to a web page.

## Creating a JavaScript (.js) file
* Open a text editor. Create a new file and copy in the following code:
```javascript
alert("hello world");
```
* Save this file as *test.js*. JavaScript files have a .js extension.
* Create the following basic HTML page and save it in the same folder as *test.js*.

```html
<!DOCTYPE HTML>
<html lang="en">
<head>
<title>Add a title here</title>
<meta http-equiv="content-type" content="text/html;charset=utf-8">
</head>
<body>
All the content for the page must go here.
<script type="text/javascript" src="test.js"></script>
</body>
</html>
```

* Test this web page in a browser. You should see an 'alert' box displaying the text 'hello world'.   
* The *script* tag is used to insert JavaScript into a web page, it works in a similar way to linking to a CSS file using the *link* element.
```html
<script type="text/javascript" src="test.js"></script>
```
* We specify the type of the file we are linking to and the src (URL) to the file.

> Important!
> Although we can use the *script* element anywhere in the page, for now we should always place it just before the closing body tag.

## Some simple JavaScript
The following pieces of code are some of the basic commands that we will use in JavaScript over and over again. They allow use to gather data from the user, output a message and change basic properties of the HTML page.

### Generating Output
Often when writing JavaScript we want to output some kind of a message to the user. There are a number of JavaScript commands that allow us to do this.

```javascript
alert("message goes in here");
```
Produces a simple alert box containing the text within the brackets. This text needs to be placed within quotation marks either single or double.

```javascript
console.log("type new content in here");
```
This code writes the text in the brackets to the browser's console. In Chrome (or Firefox), right-click on the page, select *inspect*, and then *console* to view the output.

### Gathering Data from the User
The most basic way in which we can gather data from the user is by using a prompt box

```javascript
prompt("What is your name?");
```

This line of code prompts the user for a response to the question what is your name?

### Setting Basic Properties
There are a number of properties of the browser window and HTML page that we can set using JavaScript

```javascript
document.body.style.backgroundColor="red";
```

This line of code changes the background colour of the HTML document to red. We are actually changing the CSS of the body element, specifically the *background-color* property. We can manipulate any CSS property in this way. E.g.

```javascript
document.body.style.fontFamily="Verdana";
```

If the CSS property consists of two words hyphenated e.g. *font-family*, they are combined into a single word with a capital letter for the second word i.e. *fontFamily*

### Comments
Often when writing programs we want to add comments to our code. Comments are lines that the browser will ignore, but are useful to us as a way of adding notes to our code.  We add a comment simply by putting two forward slashes at the start of a line e.g.

```javascript  
alert("this is an alert");
//This is a comment
alert("this is another alert");
```

In most text editors there is a shortcut for adding comments, *Ctrl* + */* i.e. *ctrl* and the forward slash key.

We can also have multi-line comments using /* and */ to mark these out e.g.

```javascript  
alert("this is an alert");
/*
This is a comment
that stretches
over multiple lines
*/
alert("this is another alert");
```

### Semicolons
If you look at the above examples of JavaScript you will see that every line of code ends with a semicolon(;). The semicolon is used to indicate the end of a JavaScript statement. JavaScript isn't very strict about the use of semicolons but it is good practice to include them.

### Basic Errors
One of the most frustrating aspects of learning how to program is when your program doesn’t work and you can’t work out why. Here is a list of the most common beginner mistakes

* Case-sensitivity - JavaScript is a case sensitive programming language. Generally most of the JavaScript we write is written entirely in lower case but there are exception (some statements are written using **camelCaps**) so thoroughly check the code you have written against your notes.
* Missing Quotation Marks -Text that we output needs to be contained within quotation marks otherwise the browser tries to interpret it as being JavaScript code. If your programs don’t work check that you have closed all the quotation marks that you have opened.
* Too many quotation marks - Sometimes the text that we want to output also contains quotation marks.
```javascript
console.log("<a href='mypage.htm'>link to my page</a>")
```
The above  statement writes an anchor element to the console. The anchor element features a *href* attribute. The value for the *href* attribute needs to be contained within quotation marks. These quotation marks need to be single quotation marks so the browser knows they are a different set from those of the ```console.log()```.

Alternatively we can use the escape character (\\). The escape character is used to express non-printable characters.

```javascript
console.log("<a href=\"mypage.htm\">link to my page</a>")
```

## Exercises
1. Create a basic HTML document. Add JavaScript to this page that:-
  * Produces an alert box containing the text 'JavaScript is Great'
  * Changes the background colour of the page to green
  * Produces a prompt box that asks the user for their name  
  * Using console.log() output the following text - *The University of Huddersfield is a dynamic and expanding institution in a thriving West Yorkshire town.*
