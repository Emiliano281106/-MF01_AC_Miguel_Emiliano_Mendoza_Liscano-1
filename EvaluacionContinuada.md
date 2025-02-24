# Evaluación Continuada/Emiliano Mendoza

# REACT

## Hooks 
- **What does it do?**
    * useState: manage `SIMPLE` variables and literal objects. Tracks the variables state.
    * useRef: `STORES` data betwween renders, ensuring it `PERSISTS` across renders. It can be used to store a mutable value that does not cause a re-render when updated.
    * useMemo: same as useRef but is better for handling complex operations.
    * useContext: `SHARES` data between `COMPONENTS`. We use it when different componenets need access to the same value.
    * useReducer: manage `large` volumes of objects, is like the "enhanced" version of the useState.
    * useEffect: `SYNCS` with actions(dependencies).

- **Syntax**
  
 - useState:
 ```j̀sx
const [state, setState] = useState(initialState);
```

- useRef:
```jsx
const ref = useRef(initialValue);
```

- useMemo:
```jsx
const cachedValue = useMemo(calculateValue, dependencies)
```

- useContext:
```jsx
const value = useContext(SomeContext)
```

- useReducer:
```jsx
const [state, dispatch] = useReducer(reducer, initialArg, init?)
```
- Dispatcher: function that sends an action to the reducer.
- Reducer: function that determines how the state should change in response to a given action and return a new state.
- Action : literal object with a field type thst describes the action, and other fields that contain the payloads.

  
- useEffect:
```jsx
useEffect(() => {
  // code to execute
  return () => {
  };
}, [dependencias]);
```
- If [] is empty, runs only once after first render.
- If [dependencies], runs after any of them changes.
- If don't specify, runs after every render.

# KEY CONCEPTS/TOOLS

## Render virtual DOM ()
  







  
  
 
  
      

