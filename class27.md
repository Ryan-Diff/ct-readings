## Understanding set-state https://css-tricks.com/understanding-react-setstate/

### setState Explained (https://css-tricks.com/understanding-react-setstate/)
* setState() is the only legit way to update state in react, do not modify state directly
* setState() will update only the information on the page that changes
* setState() only updates once so any conflicting declarations happening within the function will replace each other and then apply
* the new state will not be updated until it is re-rendered, so you will need to use an updater. prevState can be used to access what the state was before setState() was ran.
* When updating state multiple times, pass a function

### Lists and Keys (https://reactjs.org/docs/lists-and-keys.html)
* map can be used to create multiple JSX elements to add to the page
* do not use indexes for the keys if the order of the items might change
* keys are used by react to figure out which children of an element have changed
* keys must be unique among siblings
* map can be used within {} inside JSX to create the elements

### Typechecking Props (https://reactjs.org/docs/typechecking-with-proptypes.html)
* propTypes can be added to props to check the type
* example: Greeting.propTypes = { name: PropTypes.string }
* propTypes are only checked in development mode and if the types are incorrect it lets you know in the console
* propTypes can check for array, bool, func, number, object, string, symbol
* Prop.Types.element can specify that only a single child can be passed to a component as children
* defaultProps can set default prop values

### Components and Props (https://reactjs.org/docs/components-and-props.html)
* Components let you split the UI into independent, reusable pieces and think about each piece in isolation
* components are like functions, props are like parameters
* React elements can represent user-defined components by passing props

### handling events (https://reactjs.org/docs/handling-events.html)
* React events are named with camelCase
* With JSX you pass a function as the event handler, rather than a string
* preventDefault needs to be called to prevent the default
* When using this. with JSX callbacks this.handleClick needs to be bound and passed to the onClick or it will be undefined 
* to avoid using bind, you can add it in the class fields: <button onClick={this.handleClick}> or <button onClick={() => this.handleClick()}>
* with the second example above, another callback is created each time the user clicks so avoid this when you can.
* arguments can be passed to event handlers: <button onClick={(e) => this.deleteRow(id, e)}>Delete Row</button> or <button onClick={this.deleteRow.bind(this, id)}>Delete Row</button>

### snapshot testing (https://jestjs.io/docs/en/snapshot-testing)
* snapshot tests are to make sure your ui doesnt change unexpectedly
* snapshot tests test the output of the component by itself, it doesnt test the data that will go into it
* when a change happens that breaks the test and the snapshot needs to be updated run 'jest --updateSnapshot'
* you need prettier installed to use inline snapshots
* Jests asymmetric matcher needs to be used to test properties
* treat snapshots as code and commit and change them as your code changes
* Date.now = jest.fn(() => 1482363367071); can be used to make sure a date is always passing, but changes in the app
* use descriptive snapshot names

### React Testing Library (https://kentcdodds.com/blog/introducing-the-react-testing-library)
* tests should test what your functions do, not implementation details
* react-testing-library encourages better testing practices
* it tests dom nodes and queries it in the same way a user would
* tests should test how the user would use the app