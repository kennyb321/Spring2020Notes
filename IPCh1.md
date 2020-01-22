<h1>Chapter 1</h1>
<h2>Introduction to Computers and the Internet</h2>
<b>Client-Side Programming</b>
<ul><li>Technology designed to run on a users device</li>
<li>HTML</li>
<li>CSS</li>
</ul>
<b>Javascript</b>
Language of choice for implementing clioent-side Internet Applications<br><br>
<b>Server-Side Programming</b><ul>
<li>Applicationsd that respond to requests from client side web browsers</li>
<li>Examples:<ul>
<li>Searching the Internet </li>
<li>Checking Bank Account Balance</li>
<li>Ordering something from Amazon</li>
</ul></ul>
<br><br>
<b>Server-Side Technologys</b>
<ul>
<li>PHP</li>
<li>ASP.NET</li>
<li>C#</li>
<li>Visual Basic</li>
<Javascript Faces</li>
</ul>
<br>
<b>Moore's Law - </b> Every year or two the capabilities of computers double while the cost of
producing hardware becomes less.<br><br>
<b>HTML5 - </b>
<ul>
<li>markup language</li>
<li>designed to specify the content and structure of a web page</li>
</ul>
<br>
<b>CSS - </b>
<ul>
<li>Cascading Style Sheet</li>
<li>Used to specify the presentation of a web page</li>
</ul>
<br>
<b>JavaScript - </b>
<ul>
<li>Programming language for the Internet</li>
<li>Lets you build dynamic web pages</li>
<li>Enables Client Side web applications</li></ul>
<br>
<br>
<b>JQuery - </b>
<ul>
<li>Most popular Javascript library</li>
<li>Makes it easier to manipulate a webpages elements and interact with various browsers</li>
<li>Produces library of custom GUI controls</li>
<li>Can be used to enhance the look and feel of a website</li></ul>
<h3>Evolution of the Internet and the World Wide Web</h3>
<br>
<b>ARPA - </b>
<ul>
<li>Late 1960's</li>
<li>Advanced Research Projects Agency</li>
<li>Built by Universities to share research acrosss the country</li>
<li>Original Bandwith was 56 Kbps (56000 bits per second)</li>
</ul>
<br>
<b>Packet Switching</b>
<ul>
<li>ONe of the prium ary goals of ARPNET was to allow multiple users to send and recieve informatioin simultaneously.</li>
<li>Packet switchinig allows this by havibng data split ionto deifferent packets.</li>
<li>packets contained <ul><li>address</li>
<li>error-control</li>
<li>sequencing information</li></ul>
<li>allowed information to be routed to its correct destination</li>
<li>packets arrive in random order, and are re-organized at destion thanks to sequencing information contained within the packets</li>
<li>packet switching network designed to operate without a <b>centrilized control</b><ul><li>if one 
part of the network goes down, the network as a whole is satill function al</li></ul></ul>
<br>
<br>
<b>TCP/IP</b>
<ul>
<li>Protocol for communicating over the Internet</li>
<li>TCP = Transmission Control Protocol</li>
<li>IP = Internet PRotocol</li>
</ul>
<br>
<b>HTML</b>
<ul>
<li>Developed by <b>Tim Berners-Lee</b>, of CERN.</li>
<li> HTML = Hypertext Markup Language</li>
</ul>
<b>HTTP</b>
<ul>
<li>Devleoped by Tim Berners-Lee of CERN</li>
<li>HTTP = Hypertext Transfer Protocol</li>
<li>Communications Protocol used to send informatiuon over the web.
</li>
</ul>
<b>URL</b>
<ul>
<li>
Uniform Resource Locator</li>
<li>Used to find destinations over the web</li>
</ul>
<br>

<b>
HTTPS</b>
<ul>
<li>Hypertext Transfer Protocol Secure</li>
<li> A more secure way to send information over the web</li>
<li>Combines HTTP with <b>Secure Sockets Layer</b>(SSL) and more recent <b>Transport Layer Security (TLS)</b>
</li>
<li>performance is slower becaause of the encryption and decryption consume significant computer resources</li>
</ul>

<br>
<h3>Web Basics</h3>
<b>hyperlinks - </b> when clicked load a specified web document.
Internet is composed of nothing but millions of web pages connected to eachother through hyperlinks
<br>
-When a user clicks a link, a <b> web server </b> locates the requested web page and sends it to the users web browser.
<br>
<br>
<b> URL vs URI</b>
<ul>
<li>URI = Uniform Resource Identifier. USed to identify a resource on the internet.</li>
<li>URI's that start with 'http://' are called <b>Uniform Resource Locators</b>
</ul>
<br>
<b>Parts of a URL</b>
Example URL = 
http://www.deitel.com/books/downloads.html
<ul>
<li>http:// - indicates that the Hypertext Transfer PRotocol should be used to obtain the source</li>
<li>next is the URL's <b>hostname</b> - the name of the web-server computer on which the resource resides</li>
<li>the computer is referred to as the <b>host</b> because it houses and maintains the resources</li>
<li>Hostname is translated into an <b>IP Address</b><ul><li>numerical value that uniquley identifies the server on the internet</li></ul>
<li><b>Domain Name Server (DNS) </b> maintains a database of hostnames and their corresponding IP addresses and performs translations automatrivcally.</li>
<li>Remainder of the URL specifies the resources location  and name on the server.</li>
<li>Location could correspond to the actual name of location, however for security purposes, usually the address corresponds to a <b> virtual directory</b> and is re-translated to the actual address on the server</li>

</ul>
<br>


<b> Making a request and receiving a response</b>
<ul>
<li>When a URL is entered into a web browser, the browser usses HTTP tyo request the page from the server</li>
<li>request is </li>
</ul>


 >```GET /books/downloads.html HTTP/1.1```         

* **GET** is an **HTTP method** indicating that the client wihsies to obtain a resource from the server
* the rest of the command conatins the path name of the resource, and the protocols name and versiopn number (HTTP/1.1)
* any server thast undersatdns HTTP will be able to translate the request anbd respind appropiatly.
* server first sends a line of text that indicates the http version followed by a numeric code and a phrase that describes the status of the transaction,
	* ```HTTP/1.1 200 OK```
		* means success
	* ```HTTP/1.1 404 Not Found ```
		* informas the client the resource could not be located

### HTTP Headers
* Next, the server sends one of more **HTTP Headers**, which provide additional information abut the data that will be sent.
* in this case, the server is sending an HTML text document, so one HTTP header for this example would read
	* ``` Content-type: text/html ```
* this information specifies the **Multipurpose Internet Mail Extensions (MIME) type** of the content that the server is transmitting to the browser
* **MIME** standard sepcpfies formats, which programs can use to interpret data.
	* example: MIME type *text/plain* indicates the information is text
	* example: MIME type *image/jpeg* indicates an image is being sent.
* header or set of headers is followed by a blank line, which indicates the headers are done being sent.


### HTTP POST & GET
* two most common **HTTP request types**
	* AKA **request methods**
* **get** - retreieves informatiopn from a server
* **post** - sends data to a server
* **server-side handling** - prossess the data that posts to a server
* **Example** - ```www.google.com/search?q=deitel```
	* *q* is the name of a vairable in Googles search formats
	* *deitel* is search term
	* *?* is used to seperate the **query string** from the rest of the URL in a request.
	* *name/value* pair is passed to the server with the name and value sepereated by an equal sign(=)
	* if more than 1 *name/value* pair is submitted, each pair is seperated by an ampersand(&)
	* server uses data passed in a **query string** toi retrieve appropiate resource from the server
* **get** request can be initiated by:
	* submitting an HTML form whose **method** attribute is set to ''get''
	* typing the URL firexctly into the address bar
* **POST** request sends form data as part of the HTTP mesage 
	* get typically limits the **search query**, so its sometimes neccasary to obtain l;arge amounts of information throuigh the **post** method.
	* **post** sometimes preffered because it hides the submitted data from the user by embedding it in an HTTP message. 
	
	
	
### Client Side Caching
* Browsers often **cache**, or save webpages for quick reloading
* an hTTP response can iindicate the lengfth of the time for whicvh the content retains *fresh*

## Multi-tier Application Architecture

* **multi-tier application** - divide functionality into seperate **teirs**
* sometimes called **n-teir applications**
* teirs of web based applications often reside on seperate computers 
* **bottom tier** - maintains the applications data
	* aka - data teir / information teir
	* typically stores data in a relational database
* **middle teir** - implements buisness logic, controller logic, and presentaqtion logic to control interactions between the applications clients and its data.
	* the middle tier acts as an intermediarry between information tiers and applications clients.
	* **controller lofic**
		* proccesses client requests
		* retrieves dasta from the database
	* **business logic** in the middle tier enforces **buisness rules** and ensures data is reliable before the applicaztion nupdates a database 
	* example if busniess rule - busniess rule in the middle tier of a retail stoers web based application might ensure that all product quantities remain postivie.
* **top tier** - applications user interface
	* aka client tier

## Client-Side Scripting versus Server-Side Scripting
* **client-side** javascript can be used to
	* validate user input
	* interact wuth browser
	* enhance web pages
	* add cliennt/server communication betweeb a browser and web server
* **browser dependancy** - 	browser or **scripting host** must support the scripting languiage and capabilities
* **server side scripts** - programmers have more felxibility. 
	* server-side scritping languages have a wider range of p[rogramattic capabilities
	
	
## 
		





 































