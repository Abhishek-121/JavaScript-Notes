# JavaScript-Notes

## History of JavaScript

* JavaScript was created by Brendan Eich in 1995 during his time at Netscape Communications. It was inspired by Java.
* JavaScript has become the de-facto standard programming language of the Web, not only because of its first-mover advantage, but because it is open, standardized, and, most importantly a very good language; well-suited to the Web with its dynamic nature and tight integration with the DOM.

![jshistory](https://user-images.githubusercontent.com/56202291/113093554-ca3a9880-920d-11eb-9469-06db4b9640c7.jpeg)

### The unique circumstances of the birth of the language, including:
* the aforementioned marketing ploy,
* time-compressed initial development,
* a prejudice that development for the Web was not “serious”,
* the ubiquitous and “unbreakable” deployment environment (the Web), and
* the inclusion of language design elements unfamiliar to most developers


## How the Browsers works 

* The browser's high level structure

### 1.The user interface:
This includes the address bar, back/forward button, bookmarking menu, etc. Every part of the browser display except the window where you see the requested page.
### 2.The browser engine: 
Marshals actions between the UI and the rendering engine.
### 3.The rendering engine : 
It is responsible for displaying requested content. For example if the requested content is HTML, the rendering engine parses HTML and CSS, and displays the parsed content on the screen.
### 4.Networking:
For network calls such as HTTP requests, using different implementations for different platform behind a platform-independent interface.
### 5. UI backend: 
It is used for drawing basic widgets like combo boxes and windows. This backend exposes a generic interface that is not platform specific. Underneath it uses operating system user interface methods.
### 6. JavaScript interpreter. 
Used to parse and execute JavaScript code.
### 7. Data storage. 
This is a persistence layer. The browser may need to save all sorts of data locally, such as cookies. Browsers also support storage mechanisms such as localStorage, IndexedDB, WebSQL and FileSystem.

![Browser](https://user-images.githubusercontent.com/56202291/113097325-5354ce00-9214-11eb-953a-46049a374263.png)


## How the Web Works 

### The journey from code to webpage: 
let’s walk through that Github search to see how we go from a URL typed into an address bar to a running web page:

1) You type a URL into your browser

2) The browser parses the information contained in the URL. This includes the protocol (“https”), the domain name (“github.com”) and the resource (“/”). In this case, there isn’t anything after the “.com” to indicate a specific resource, so the browser knows to retrieve just the main (index) page.

3) The browser communicates with your ISP to do a DNS lookup of the IP address for the web server that hosts www.github.com. The DNS service will first contact a Root Name Server, which looks at https://www.github.com and replies with the IP address of a name server for the “.com” top-level domain. This address is sent back to your DNS service. The DNS service does another outreach to the “.com” name server and asks it for the address of https://www.github.com.

4) Once the ISP receives the IP address of the destination server, it sends it to your web browser.

5. Your browser takes the IP address and the given port number from the URL (the HTTP protocol defaults to port 80 and HTTPS defaults to port 443) and opens a TCP socket connection. At this point, your web browser and web server are finally connected.

6) Your web browser sends an HTTP request to the web server for the main HTML web page of www.github.com.

7) The web server receives the request and looks for that HTML page. If the page exists, the web server prepares the response and sends it back to your browser. If the server cannot find the requested page, it will send an HTTP 404 error message, which stands for “Page Not Found”.

8) Your web browser takes the HTML page it receives and then parses through it doing a full head to toe scan looking for other assets that are listed, such as images, CSS files, JavaScript files, etc.

9) For each asset listed, the browser repeats the entire process above, making additional HTTP requests to the server for each resource.

10) Once the browser has finished loading all other assets that were listed in the HTML page, the page will finally be loaded in the browser window and the connection will be closed


## Painting the final picture

Now that your browser has the resources comprising the website (HTML, CSS, JavaScript, images, etc), it has to go through several steps to present the resources to you as a human-readable webpage.

Your browser has a rendering engine that’s responsible for displaying the content. The rendering engine receives the content of the resources in small chunks. Then there’s an HTML parsing algorithm that tells the browser how to parse the resources.

Once parsed, it generates a tree structure of the DOM elements. DOM stands for Document Object Model and it is a convention for how to represent objects located in an HTML document. These objects — or “nodes” — of every document can be manipulated using scripting languages like JavaScript.

                                            DOM TREE 
   ![Dom Tree](https://user-images.githubusercontent.com/56202291/113097857-484e6d80-9215-11eb-860d-913824a8e6e9.jpeg)

* So how do all the packets know how to get to their destination without getting lost?
  The answer is TCP/IP.

## Introduction to JavaScript
* JavaScript accepts both double and single quotes
* JavaScript and Java are completely different languages, both in concept and design.
* JavaScript was invented by Brendan Eich in 1995, and became an ECMA standard in 1997.
* ECMA-262 is the official name of the standard. ECMAScript is the official name of the language.

* While writing JS include the content within the <script> tag within the same file.
* For External Js :
   <script src =“./index.js	></script>
  
## Variables 

* JavaScript variables are containers for storing data values.

```jsx
var x = 5;
var y = 6;
var z = x + y;
```
* It's a good programming practice to declare all variables at the beginning of a script.

* Since JavaScript treats underscore as a letter, identifiers containing _ are valid variable names:
*  Eg : var _name = 'Abhishek'

-- Three ways of defining a variable :
 
1. var - functionally scoped , can be changed
2. const -block scoped, cannot  be changed
3. Let  - block scoped, can be changed

* var a = 10; // variable declaration statement
* console.log(a); //function call statement

* {
    ...   //Code block…
    ...
   }

* Declaring a variable : 
Generally start with small alphabet or use Camel-case Notation(like iLikePizza)  or snake case(like i_like_pizza) also include 2 special character($and_).

 
- Anything which is in Global scope attached to the Window object.
- const and let are not attached to the window object even if they are declared in global scope while var get attached.


![let var const](https://user-images.githubusercontent.com/56202291/113098954-d2e39c80-9216-11eb-9a56-31420015a8db.jpeg)


## Types of Variables : 

* String
* Number
* Object
* Boolean
* Undefined
* Symbol : Always gives a guaranteed unique identifier
* Null

### Note : Everything except Object is Primitive type, Object is special one.

Six other escape sequences are valid in JavaScript:
```jsx
Code	Result
\b	Backspace
\f	Form Feed
\n	New Line
\r	Carriage Return
\t	Horizontal Tabulator
\v	Vertical Tabulator
```
### Note :The 6 escape characters above were originally designed to control typewriters, teletypes, and fax machines. They do not make any sense in HTML.


### Strings :

-- 3 ways to create strings:

* using single quotes:

const first = 'Soumya';

* using double quotes:

const middle = "Ranjan";

* using backticks:

const last = `Mohanty`;

### String Methods

![SMethod](https://user-images.githubusercontent.com/56202291/113101854-d7aa4f80-921a-11eb-8ad5-6ac0e559cb62.jpeg)


### Numbers 
 Eg : var x = 20;
 
 ### Methods
 ![Number](https://user-images.githubusercontent.com/56202291/113101012-cdd41c80-9219-11eb-8777-55db7a579da5.jpeg)

 
### Objects 

-- In JavaScript, almost "everything" is an object.
Booleans can be objects (if defined with the new keyword)
Numbers can be objects (if defined with the new keyword)
Strings can be objects (if defined with the new keyword)
Dates are always objects
Maths are always objects
Regular expressions are always objects
Arrays are always objects
Functions are always objects
Objects are always objects
All JavaScript values, except primitives, are objects.

* Objects are variables too. But objects can contain many values.

* The values are written as name : value pairs (name and value separated by a colon).

```jsx
Example
var person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
```

-- There are different ways to create new objects:

* Define and create a single object, using an object literal.
* Define and create a single object, with the keyword new.
* Define an object constructor, and then create objects of the constructed type.


![objects](https://user-images.githubusercontent.com/56202291/113101532-771b1280-921a-11eb-8aeb-51165cbe5b9b.png)

```jsx
Example
var person = {
  firstName: "Abhishek",
  lastName : "Maheshwari",
  id       : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};
```
* In a function definition, this refers to the "owner" of the function.

* In the example above, this is the person object that "owns" the fullName function.

* In other words, this.firstName means the firstName property of this object.

## Note : Methods are functions stored as object properties.

* You access an object method with the following syntax:
```jsx
objectName.methodName() 
```

### Null vs Undefined 
Null means an empty or non-existent value. Null is assigned, and explicitly means nothing. while undefined typically means a variable has been declared but not defined yet.

```jsx
let a = null;
console.log(a);// null

let b;
console.log(b); // undefined
```
** Both null and undefined are primitive values. Here is a full list:
1. Boolean
2. Null
3. Undefined
4. Number
5. String
6. Symbol

** In JavaScript there are only six falsy values. Both null and undefined are two of the six falsy values. Here’s a full list:
* false
* 0 (zero)
* “” (empty string)
* null
* undefined
* NaN (Not A Number)
* Any other value in JavaScript is considered truthy.

## Booleans and Equality:
A boolean variable can be either true or false .
```jsx
* Example:

const age = 18;
const ofAge = age > 18;
console.log(ofAge); // false
```

* Equal signs:

* = sign: used for assignment/ updation of values

```jsx
let name = 'Soumya';
name = 'Raja';
Out of == and ===, you should almost always use ===.

== and === are used for equality comparison.

console.log(age === 18); // true
== vs === :
```

* === checks both type & value.
* == only checks value.

```jsx
10 === "10" // false as values are same but types are not
10 == "10" // true as values are same
```

## Functions:

- A JavaScript function is a block of code designed to perform a particular task.
- A JavaScript function is executed when "something" invokes it (calls it).
- By defining the code we can use it multiple times.

* Syntax : 
function name(parameter1, parameter2, parameter3) {
  // code to be executed
}

```jsx
Example 
function myFunction(p1, p2) {
  return p1 * p2;   // The function returns the product of p1 and p2
}
```

### Built In Function
JavaScript has five functions built in to the language. They are eval, parseInt, parseFloat, escape, and unescape.

1. eval(Expression)

* Examples:
var x = 2
var y = 39
var z = "42"
println(eval("x + y + 1")) 
println(eval(z))
// Both will print 42

2. parseInt: Parses a string argument and returns an integer of the specified radix or base. 
```jsx
Syntax:

parseInt(string)
parseInt(string, radix)
string is a string that represents the value you want to parse.
radix is an integer that represents the radix of the return value.
```
3. parseFloat :Parses a string argument and returns a floating point number. 
* Syntax:
  parseFloat(string)

4. escape: Returns the hexadecimal encoding of an argument in the ISO Latin-1 character set. 
 * Syntax:
   escape("string")
 Example : the following returns "abc%26%25":
           escape("abc&%")

5. unescape : Returns the ASCII string for the specified value. 
* Syntax:
  unescape("string")
  string is a String object or literal.

### Arguments & Parameters:

* Parameters are like placeholders for data that will be passed to a function.
* Arguments are the actual values passed to a function while calling it.

```jsx
function calculateBill(billAmount, taxRate) { // here billAmount, taxRate are parameters
  const total = billAmount + billAmount * taxRate 
  return total;
}

calculateBill(100, 0.13); // here 100, 0.13 are arguments
```

![function](https://user-images.githubusercontent.com/56202291/113105825-a7b17b00-921f-11eb-8227-132588c2641c.jpeg)

* Parameters are variables local to the function; available only inside the function.
* You can also pass variables as arguments during a function call.

* Different ways of declaring a function :

1. Normal function :      
```jsx
function name([param[, param[, ... param]]]) {
   statements
}
```
2. Anonymous function : Function without name.

```jsx
Syntax : 
var myFunction = function() {
    statements
}
```

 3. IIFE (Immediately Invoked Function Expression): When functions are used only once.IIFE are function expressions that are invoked as soon as the function is declared.

```jsx
Eg : var result = (function () {
    var name = "Barry";
    return name;
})();
// Immediately creates the output:
result; // "Barry"
```

4. Arrow Function Expression :

```jsx

//Traditional Function
function (a){
  return a + 100;
}

// Arrow Function Break Down

// 1. Remove the word "function" and place arrow between the argument and opening body bracket
(a) => {
  return a + 100;
}

// 2. Remove the body brackets and word "return" -- the return is implied.
(a) => a + 100;

// 3. Remove the argument parentheses
a => a + 100;

Eg :
// Traditional Function
function (a, b){
  return a + b + 100;
}

// Arrow Function
(a, b) => a + b + 100;

```

## Scope

1. Local Variables Scope : Variables declared within a JavaScript function, become LOCAL to the function.

* Local variables have Function scope: They can only be accessed from within the function.

```jsx
Example
// code here can NOT use name

function loconav() {
  var name = "Volvo";
  // code here CAN use name
}
```

2. Global Variables Scope : A variable declared outside a function, becomes GLOBAL.

* A global variable has global scope: All scripts and functions on a web page can access it.

```jsx
Example
  var name = "Volvo";
// code here can use name
function loconav() {
  var name = "Volvo";
  // code here CAN also use name
}
```

![scope](https://user-images.githubusercontent.com/56202291/113106871-e136b600-9220-11eb-8111-4f2a7b9dfe9d.png)


## Hoisting

* It is a JavaScript mechanism where variables and function declarations are moved to the top of their scope before code execution.

<img width="641" alt="Hoisting" src="https://user-images.githubusercontent.com/56202291/113107554-b13be280-9221-11eb-8706-ea87dc1942c7.png">

## Closure

* A function bind together with its lexical environment. Or A function along with its lexical scope.

### Def : It is the combination of function bundled together (enclosed) with reference to its surrounding state (lexical env) .

```jsx
Eg : function x(){
 var a =7;
 function y(){
  Console.log(a);
 }
y();
}
x();

*  We can return the function as well.
Eg : function x(){
 var a =7;
 function y(){
  Console.log(a);
 }
 return y;// Here we are returning the function.
}
var z = x();
Console.log(z) ;
 // Output : function y(){console.log(a);}
 
 ```

* Uses Of Clauses :
1. Module design pattern.
2. Currying
3. Functions like once
4. Memorize
5. Maintaining state in async world
6. Set timeouts
7. Iterators.




## The DOM - Working with HTML and CSS:

### Def: is a platform and language-neutral interface that allows programs and scripts to dynamically access and update the content, structure, and style of a document. 

-- With the object model, JavaScript gets all the power it needs to create dynamic HTML:

* JavaScript can change all the HTML elements in the page
* JavaScript can change all the HTML attributes in the page
* JavaScript can change all the CSS styles in the page
* JavaScript can remove existing HTML elements and attributes
* JavaScript can add new HTML elements and attributes
* JavaScript can react to all existing HTML events in the page
* JavaScript can create new HTML events in the page


![DOM](https://user-images.githubusercontent.com/56202291/113106127-04149a80-9220-11eb-9804-b4c5e1bd4895.png)

-- DOM standard is separated into 3 different parts:

1. Core DOM - standard model for all document types
2. XML DOM - standard model for XML documents
3. HTML DOM - standard model for HTML documents

* Elements properties and methods:
  For details about element properties, visit the below link https://www.w3schools.com/jsref/dom_obj_all.asp

* Nodes properties and methods:
  For details about node properties, visit the below link https://developer.mozilla.org/en-US/docs/Web/API/Node

















