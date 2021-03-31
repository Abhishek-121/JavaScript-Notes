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


```jsx
Example
document.getElementById("demo").innerHTML = "Hello JavaScript";
```
