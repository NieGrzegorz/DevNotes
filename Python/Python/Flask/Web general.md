What is a web server? 
Piece of hardware
Piece of software designed to accept incomming web request 

HTTP verbs
When user tries to acces a page (google.com), the browser sends a following 

GET / HTTP/1.1
Host: www.google.com

This is a get request

GET - a HTTP verb, what is expeted from the server
/ - a path requested (root in this case)
HTTP/1.1 - Protocol 

The most important http verbs: 
GET - retrieve something
POST - Receive data and use it 
PUT - make sure that something is there (update or create )
DELETE - remove something 

REST API principles: 
- REST API is a way of thinking about how a web server responds to your requests 
- It does not respond with just data 
- It responds with resources 

Resources - similar to OOP, think of server as having resources and each is able to interact with the pertinent request 

Singular endpoint can be a resource and we can GET POST PUT DELETE to use it 

REST is or supposed to be stateless - a single request cannot depend on any other request 
The server only knows about the current request and not any previous requests 

How to do login without a state: 
The web server does not know that the user is logged it (since it does not remember any state )

The web app must send enough data to identify the user in EVERY reqyest, or the server won't associate the request with the user 


