## react custom hooks (https://reactjs.org/docs/hooks-custom.html)
* a custom hook starts with use and can call other hooks
* two components using the same hook do not share state
* data can be passed between hooks with the parameters

## hook rules (https://reactjs.org/docs/hooks-rules.html)
* only call hooks at the top level
* put any conditions inside the hook

## custom hooks - all you need to know (https://www.telerik.com/kendo-react-ui/react-hooks-guide/#toc-custom-react-hooks)
* never call hooks from a regular function
* hooks clean up our jsx code to make it match the DOM better
* functional components can have a const above the jsx
* the reducer hook returns the accumulation of something

## 10 essential react hooks (https://blog.bitsrc.io/10-react-custom-hooks-you-should-have-in-your-toolbox-aa27d3f5564d?gi=c4033b42b5da)
* useArray, yarn add react-hanger, import {useArray} from 'react-hanger', this comes with array methods
* react-use-form-state, npm i react-use-form-state, simplifies complex state management
* react-fetch-hook, npm i react-fetch-hook, makes ajax calls
* useMedia, tracks the state of a css media query
* react-useportal, yarn add react-useportal, renders children into a DOM node that is outside the DOM hierarchy of the parent
* react-firebase-hooks, npm i react-firebase-hooks, firebase authentication or storage
* use-onClickOutside, tells when a user clicks on anything besides a specific element
* useIntersectionObserver, npm i react-use-intersection-observer, asynchronously watches changes between an element and an ancestor or document viewport
* use-location, gets the location of the browser
* use-redux, yarn add use-redux, redux reader