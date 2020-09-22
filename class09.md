## Using Express Routing (https://expressjs.com/en/guide/routing.html)
* Routing refers to how an applications endpoints (URI's) respond to client requests
* You can define routs using methods of the Express app object that corresponds to HTTP methods (get, post, delete, etc)
* These methods specify a callback/handler function
* Routing methods can have more than one callback function and are called with next()
* ap*all() is used to load middleware functions for all HTTP methods
* Route paths can be strings, string patterns, or regular expressions
* Route parameters are named URL segments that target a specific route

## Supertest (https://github.com/visionmedia/supertest)
* npm i supertest --save-dev
* called with require('supertest')

## Using Express Middleware (https://expressjs.com/en/guide/using-middleware.html)
* Middleware functions have access to the request object (req), response object (res), and the next middleware function in the application's request-response cycle
* They can execute any code, make changes to the req/res objects, end the req/res cycle, or call the next middleware function in the stack
* If the middleware function doesnt call next or end the req/res cycle the request will be left hanging
* An Express application can use these types of middleware: Application-level, Router-level, Error-handling, Built-in, or Third-party

## Express Middleware (https://www.tutorialspoint.com/expressjs/expressjs_middleware.htm)
* Middleware is called in order
* body-parser can be used to parse the body of requests that have payloads
* cookie-parser parses cookie header and populates req.cookies with an object keyed by cookie names
* express-session creates a session middleware with given options

## Express Middleware List (https://expressjs.com/en/resources/middleware.html)
* Express middleware modules list that are maintained by the Expressjs team