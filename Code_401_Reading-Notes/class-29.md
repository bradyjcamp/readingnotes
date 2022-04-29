# useReducer

- `useReducer` is another type of hook used in a React app.
- The `useReducer` Hook is used to store and update states, just like the useState Hook 
- It accepts a reducer function as its first parameter and the initial state as the second.
- It is also a pure function.
- [Let's take a look at how to instantiate and use it.](https://blog.logrocket.com/react-usereducer-hook-ultimate-guide/)

```js
const initialState = { count: 0 }

const [state, dispatch] = useReducer(reducer, initialState)
```

- The reducer function itself accepts two parameters and returns one value.
  - The first parameter is the *current state*, and the second is the *action*
  - The state is the data we are manipulating
  - The reducer function receives an action, which is executed by a dispatch function
- Here is a full scale look at the [function:](https://reactjs.org/docs/hooks-reference.html#usereducer)

```js
const initialState = {count: 0};

function reducer(state, action) {
  switch (action.type) {
    case 'increment':
      return {count: state.count + 1};
    case 'decrement':
      return {count: state.count - 1};
    default:
      throw new Error();
  }
}

function Counter() {
  const [state, dispatch] = useReducer(reducer, initialState);
  return (
    <>
      Count: {state.count}
      <button onClick={() => dispatch({type: 'decrement'})}>-</button>
      <button onClick={() => dispatch({type: 'increment'})}>+</button>
    </>
  );
}
```