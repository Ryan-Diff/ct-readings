- http Basics (https://code.tutsplus.com/tutorials/http-the-protocol-every-web-developer-must-know-part-1--net-31177)
* Hyper Text Transfer Protocol
* HTTP is a stateless protocol
* HTTP Verbs include the most popular: GET, POST, PUT, DELETE
* There are different error codes for various types of common errors
* A request is sent with header information, request and response messages can also have a body
* Chrome with Webkit inspector is a favorite too to monitor HTTP communication

## How DNS works (https://howdns.works/ep1/)
* Turns words into ip addresses
* When a pages is searched for, the browser and os check their cache to see if they know
* If not, it goes to a resolver online, it checks its cache, if not it checks the Top Level Domain Server
* If the TLD Server doesn't know, it checks one of 13 root name servers that exist today, labled a - m.root-servers.net
* The .com root server is one of the largest and created in 1985
* Other types have country codes, generic like .net .org .edu
* Today many new generic ones are being created
* If the root server doesn't know, it will give the authoritative name server for that site name
* When a domain is created the registrar creates the name and communicates to the TLD
* The authoritative name servers can be searched with a WHOIS query

## http and rest
* API: Application Program Interface
* Structured request and response (the Messenger)
* REST: Representational State Transfer
* Architecture style for designing networked applications
* Almost always relies on HTTP
* Treats server objects as resources that can be created or destroyed
* Can be almost any language (format to send message)
* Endpoints are the URI/URL where api can be accessed by a client or app

# http reference (https://code-maze.com/the-http-reference/)
* CONNECT: to use with a proxy that can dynamically switch to being a tunnel
* DELETE: requests a resource to be deleted
* GET: retrieves information
* HEAD: just like HEAD except the server MUST NOT return a message body in response
* OPTIONS: requesting communications options available
* POST: requests that the server accept the information as new information (creates)
* PUT: requests the information be stored (updates)
* TRACE: invokes a remote, application layer loop back of the request message

