## MVC (https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller)
Model view controller is a software design pattern that divides the app into three elements
* Model manages the data, logic and rules
* View represent information (charts and tables)
* Controller accepts inputs and coverts them to commands for the model or view

## Architecting Single Page Applications (https://hackernoon.com/architecting-single-page-applications-b842ea633c2e)
There are 4 layers to manage for single page applications
* View has the presentational and container components 
* Application Services interprets the state and manages external operations
* Store holds the state and notifies about changes
* Domain represents the state and manages business logic

## React MVC (https://blog.testdouble.com/posts/2019-11-04-react-mvc/) 
* When apps are totally rewritten in hooks, the components had too much information. they knew API backend data model and business logic and the components had to be updated whenever any of those changed
* MVC was the answer and it breaks down to a presentation layer and a UI data model.

## Reconciliation (https://reactjs.org/docs/reconciliation.html)
* keys make react stable across different renders
* reorders will be slow if the key is the iterator or always changing
* keys should be stable predictable, and unique
