HTTP Requests and Responses
Answer the following questions about the HTTP request and response process.


What type of architecture does the HTTP request and response process occur in? HTTP is based on client-server architecture model and a stateless request/response protocol that operates by exchanging messages across a reliable TCP/IP connection.


What are the different parts of an HTTP request? Request line, request headers, request bodies


Which part of an HTTP request is optional? Request body


What are the three parts of an HTTP response? Request line, Request header and request body


Which number class of status codes represents errors? 400, 500


What are the two most common request methods that a security professional will encounter? Get and Post.
HTTP provides a number of techniques for performing activities on the web server (the HTTP 1.1 standard refers to them as methods but they are also commonly described as verbs). While GET and POST are by far the most popular methods for accessing information from a web server, HTTP also supports a number of other (and less well-known) methods. If the web server is set incorrectly, several of these can be utilized for malicious purposes.
Most online apps, on the other hand, just have to answer to GET and POST requests, with user data being received in the URL query string or attached to the request, respectively. The standard <a href=""></a> style links as well as forms defined without a method trigger a GET request; form data submitted via <form method='POST'></form> trigger POST requests. JavaScript and AJAX calls may send methods other than GET and POST but should usually not need to do that. Because the other ways are so infrequently utilized, many developers are unaware of or fail to examine how the web server's or application framework's implementation of these methods affects the program's security features


Which type of HTTP request method is used for sending data? Post


Which part of an HTTP request contains the data being sent to the server? Request body


In which part of an HTTP response does the browser receive the web code to generate and style a web page? Response body



Using curl
Answer the following questions about curl:


What are the advantages of using curl over the browser? Able to manage request/response in a programmatic way
Able to automately test HTTP requests. abe to support numerous protocols without UI.


Which curl option is used to change the request method? curl-X


Which curl option is used to set request headers? curl h


Which curl option is used to view the response header? curl -i


Which request method might an attacker use to figure out which HTTP requests an HTTP server will accept?
Get or options


Sessions and Cookies
Recall that HTTP servers need to be able to recognize clients from one another. They do this through sessions and cookies.
Answer the following questions about sessions and cookies:


Which response header sends a cookie to the client? The Set-Cookie HTTP response header is used to send a cookie from the server to the user agent, so the user agent can send it back to the server later.
HTTP/1.1 200 OK
Content-type: text/html
Set-Cookie: cart=Bob


Which request header will continue the client's session?The HTTP keep-alive header maintains a connection between a client and your server, reducing the time needed to serve files.
GET /cart HTTP/1.1
Host: www.example.org
Cookie: cart=Bob



Example HTTP Requests and Responses
Look through the following example HTTP request and response and answer the following questions:
HTTP Request
POST /login.php HTTP/1.1
Host: example.com
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Content-Type: application/x-www-form-urlencoded
Content-Length: 34
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Linux; Android 6.0; Nexus 5 Build/MRA58N) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.132 Mobile Safari/537.36

username=Barbara&password=password


What is the request method? Post


Which header expresses the client's preference for an encrypted response? accept-Encoding: gzip, deflate, br


Does the request have a user session associated with it? No


What kind of data is being sent from this request body? Login credentials


HTTP Response
HTTP/1.1 200 OK
Date: Mon, 16 Mar 2020 17:05:43 GMT
Last-Modified: Sat, 01 Feb 2020 00:00:00 GMT
Content-Encoding: gzip
Expires: Fri, 01 May 2020 00:00:00 GMT
Server: Apache
Set-Cookie: SessionID=5
Content-Type: text/html; charset=UTF-8
Strict-Transport-Security: max-age=31536000; includeSubDomains
X-Content-Type: NoSniff
X-Frame-Options: DENY
X-XSS-Protection: 1; mode=block

[page content]


What is the response status code? 200


What web server is handling this HTTP response? Apache server


Does this response have a user session associated to it? yes, SessionID=5


What kind of content is likely to be in the [page content] response body? Web code


If your class covered security headers, what security request headers have been included? strict Transport Security 




Monoliths and Microservices
Answer the following questions about monoliths and microservices:


What are the individual components of microservices called? Services


What is a service that writes to a database and communicates to other services? API Service


What type of underlying technology allows for microservices to become scalable and have redundancy? Load balancers



Deploying and Testing a Container Set
Answer the following questions about multi-container deployment:


What tool can be used to deploy multiple containers at once? Docker compose


What kind of file format is required for us to deploy a container set? YAML files



Databases


Which type of SQL query would we use to see all of the information within a table called customers? SELECT column_name FROM customers


Which type of SQL query would we use to enter new data into a table? (You don't need a full query, just the first part of the statement.)
INSERT INTO table_name (column_1, column_2, column_3) VALUES (value_1,'value_2', value_3)


Why would we never run DELETE FROM <table-name>; by itself? it will delete the entire table