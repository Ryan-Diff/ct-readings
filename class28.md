## Architectural Styles and Architectural Patterns (https://medium.com/@mlbors/architectural-styles-and-architectural-patterns-c240f7df88a0#:~:text=Architectural%20Patterns%20VS%20Design%20Patterns&text=In%20a%20few%20words%2C%20while,and%20mechanisms%20of%20a%20system.)
* An Architectural pattern is general recurring solution to a recurring problem
* They look at the high level strategies for large scale components
* The layered pattern tends to have a presentation, application, business logic, and data access layers
* event driven patterns look at consumers and emitters of events
* the business domain is where all the business logic and processes are
* pipes and filters transform, filter, and connects data
* pumps are data sources and sinks are final targets
* microservice is an application built by many independent apps.
## Container and Presentation Patterns (https://alchemycodelab.github.io/fsjs-notes/05_react/patterns/container_presentation/)
* container components are concerned with how things work
* presentation components are concerned with how things look

## Container Details (https://alchemycodelab.github.io/fsjs-notes/05_react/patterns/container_presentation/container-details)
* independent state changes can be passed to setState() as an object
* dependent state changes (like a button increment) can be passed as a function that takes in state
* containers can also be written as hooks instead of components

## Presentation Details (https://alchemycodelab.github.io/fsjs-notes/05_react/patterns/container_presentation/presentation-details)
* presentation components are responsible for how a section of the page looks
* they are written as functional components and return the markup that is going to get rendered to the dom
* they usually receive props to make them reusable and we shoudl use prop-types to specify the props the component receives

## functional vs class components (https://medium.com/@Zwenza/functional-vs-class-components-in-react-231e3fbd7108)
* the big difference is that you need a class component for state
* when you dont need state, functional components are easier to read and test and might be faster in the future

## Conditional Rendering (https://reactjs.org/docs/conditional-rendering.html)
* conditional rendering is when you use different components based on conditions to make the page look different
* you can use it inline with && for if
* for if else use a ternary
* returning null can hide a component
