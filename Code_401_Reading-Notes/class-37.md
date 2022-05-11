# Redux - Combined Reducers

## Combined Reducers

- [Video Reference](https://www.youtube.com/watch?v=gBER4Or86hE)
- Using the `combineReducers` method is a great way to group multiple reducers together and pass them around.

```js
const userReducer = (state={}, actions) => {
  switch(action.type){
    case "CHANGE_NAME": {
      {...state, name: action.payload}
      break;
    }
    case "CHANGE_AGE": {
      {...state, age: action.payload}
      break;
    }
  }
  return state;
};

const tweetsReducer = (state=[], actions) => {
  return state;
};

const reducers = combinedReducers({
  user: userReducer,
  tweets: tweetsReducer,
})

const store = createStore(reducers);

store.dispatch({
  type: "CHANGE_NAME",
  payload: "Will"
  })

store.dispatch({
  type: "CHANGE_AGE",
  payload: 35
  })

store.dispatch({
  type: "CHANGE_AGE",
  payload: 35
  })
```

## Redux Docs

- Here is how the [Redux docs](https://redux.js.org/usage/structuring-reducers/using-combinereducers/) has it noted:

```js
// reducers.js
export default theDefaultReducer = (state = 0, action) => state

export const firstNamedReducer = (state = 1, action) => state

export const secondNamedReducer = (state = 2, action) => state

// rootReducer.js
import { combineReducers, createStore } from 'redux'

import theDefaultReducer, {
  firstNamedReducer,
  secondNamedReducer
} from './reducers'

// Use ES6 object literal shorthand syntax to define the object shape
const rootReducer = combineReducers({
  theDefaultReducer,
  firstNamedReducer,
  secondNamedReducer
})

const store = createStore(rootReducer)
console.log(store.getState())
// {theDefaultReducer : 0, firstNamedReducer : 1, secondNamedReducer : 2}
```

then..

```js
import { combineReducers, createStore } from 'redux'

// Rename the default import to whatever name we want. We can also rename a named import.
import defaultState, {
  firstNamedReducer,
  secondNamedReducer as secondState
} from './reducers'

const rootReducer = combineReducers({
  defaultState, // key name same as the carefully renamed default export
  firstState: firstNamedReducer, // specific key name instead of the variable name
  secondState // key name same as the carefully renamed named export
})

const reducerInitializedStore = createStore(rootReducer)
console.log(reducerInitializedStore.getState())
// {defaultState : 0, firstState : 1, secondState : 2}
```
