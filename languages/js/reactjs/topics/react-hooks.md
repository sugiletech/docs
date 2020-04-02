# React Hooks

- Enable developer to use state and other `React features without writing a class`.
- Let you to reuse stateful logic without chaning your component hierarchy.
- Let you use more of React's feature without classes.
- Supported in `version 16.8`

## In-built Hooks

### State Hooks - useState()

- Does not merge old and new state together, unlike `this.setState()`
- React assumes that useState() declaration and calls are in the same order during every render
- Pass a function (instead of new value) in `setState` if new value depends on previous value
- Rerender will be skipped if the new value is same as previous value
- Eg: `const [counter, setCounter] = useState(0)`

### Effect Hook - useEffect()

- Adds the ability to perform side effects from a function component.
- Effects are able to access function properties like props and state.
- Runs after every render - including first render
- Effects run in the order they are defined inside function
- `componentDidMount` + `componentDidUpdate` + `componentWillUnmount`
- Skip Effect: You can tell react to `skip` applying an effect if certain values have not changed between re-renders.
  `useEffect(() => {}, [counter, status])` re-runs the effect only if `either counter or status changes`.
- Make sure that dependencies array includes all values from component scope only that changes over time.
- Passing empty array `[]` ensures that effect runs `only once`.
- Syntax: `useEffect(() => {})`

### Context Hooks - useContext()

- Lets you subscribe to React context without introducing nesting.
- Eg: `const locale = useContext(LocaleContext)` or `const theme = useContext(ThemeContext)`

### Reducer Hooks - useReducer()

- Lets you manage local state of complex components with a reducer
- Re-render happens only with there is change in previous and new state returned by reducer
- Eg: `const [state, dispatch] = useReducer(reducer, initialArg, init)`

### Callback Hooks - useCallback

- Returns memorized callback
- `useCallback(fn, deps)` == `useMemo(() => fn, deps)`
- Eg: `useCallback()`

### Memory Hooks - useMemo

- Returns memorized version of value
- Recomputes only if either of deps has changed
- Recomputes on every render if no deps provided
- Eg: `useMemo(() => computeExpensiveValue(a, b), [a, b])`

### Reference Hooks - useRef

- Returns mutable ref object whose `.current` property is initialized to the passed argument `initialValue`
- Returned object will persist for the full lifetime of the component
- Common use case is to access a child imperatively
- Can be used to keep any mutable value around similar to instance fields in class
- Changing `.current` property does not re-render
- Eg: `const refContainer = useRef(initialValue)`

## Rules of Hooks

- Only call Hooks `at the top level`. Don't call Hooks inside loops, conditions, or nested functions.
- Only call Hooks `from React function components`. Don't call Hooks from regular JavaScript functions.

## Custom Hooks

- Lets you reuse stateful logic into multiple components
