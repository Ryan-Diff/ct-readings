##  Hooks API (https://reactjs.org/docs/hooks-overview.html)
* Hooks let you use state without class and are backwards compatible
* useState() is a hook and is similar to this.setState()
* hooks do not work in classes
* only call hooks at the top level, not inside loops, conditions or nested functions
* only call hooks from function components
* they are named as useSomething

## State Hook (https://reactjs.org/docs/hooks-state.html)
* you can use hooks in a functional component above the return
* the initial value of state gets set in the parenthesis useState(<here>) and doesnt have to be an object, but can be
* const [variableName, functionToChangeValue] = useState()
* this.state.variableName reads it
* functionToChangeValue(variableName + 1) will increment it

## Effects Hook (https://reactjs.org/docs/hooks-effect.html)
* useEffect does something after every render
* every render will create a new function call and replace the previous instance
useEffect(() => {
    document.title = `You clicked ${count} times`;
  });

## Hooks API Reference (https://reactjs.org/docs/hooks-reference.html)
* useReducer(reducer, initialArg, init) is usually better than useState when you have complex state logic or when next state depends on the previous one
* useMemo will only recompute if the dependencies have changed