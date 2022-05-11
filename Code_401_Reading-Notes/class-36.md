# Redux

> Redux is a predictable state container for JavaScript apps.

[From this article quoting docs](https://www.freecodecamp.org/news/understanding-redux-the-worlds-easiest-guide-to-beginning-redux-c695f45546f6)

- In my own words, Redux is a global conatainer for state that your react app can use in all of its components.
- There is a lot of back and forth between Redux and it is not used by everyone for everything.
  - In fact there are a lot of devs that do not like Redux.
  - The main use case would be for larger applications that have a lot of moving pieces.
  - In these large applications, keeping track of state and how to pass it around properly can be tricky.
  - That is why having global state can be very useful.

- To use this you want to create a **Redux store** in your application:

```js
import { createStore } from "redux"; //an import from the redux library
const store = createStore();  // an incomplete solution - for now.
```

- Creating the store takes in a reducer.

## Reducers

- A reducer takes in an *accumulator* and a *current value*. 
- **Redux Reducers** are functions that take in *state* and an *action*


```js
function createStore(reducer) {
    var state;
    var listeners = []

    function getState() {
        return state
    }
    
    function subscribe(listener) {
        listeners.push(listener)
        return unsubscribe() {
            var index = listeners.indexOf(listener)
            listeners.splice(index, 1)
        }
    }
    
    function dispatch(action) {
        state = reducer(state, action)
        listeners.forEach(listener => listener())
    }

    dispatch({})

    return { dispatch, subscribe, getState }
}
```

