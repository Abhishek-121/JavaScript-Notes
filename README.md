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


Painting the final picture



```jsx
Example
document.getElementById("demo").innerHTML = "Hello JavaScript";
```
