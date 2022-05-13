# Redux Toolkit

**RTK** is the toolset to compliment Redux usability.

- RTK was made due to assist devs in using Redux.
  - Redux requires a lot of installed dependencies and boiler plate code and the toolkit helps alleviate these pains.

[**Installation**](https://redux-toolkit.js.org/)

- `npm install @reduxjs/toolkit`
- Included Methods
  - `configureStore()`

  ```js
  import { configureStore } from '@reduxjs/toolkit'

  const store = configureStore({ reducer })
  ```

  - `createReducer()`
    - This makes the process of implementing reducers speedier

```js
  import { createAction, createReducer } from '@reduxjs/toolkit'

const increment = createAction('counter/increment')
const decrement = createAction('counter/decrement')
const incrementByAmount = createAction('counter/incrementByAmount')

const initialState = { value: 0 }

const counterReducer = createReducer(initialState, (builder) => {
  builder
    .addCase(increment, (state, action) => {
      state.value++
    })
    .addCase(decrement, (state, action) => {
      state.value--
    })
    .addCase(incrementByAmount, (state, action) => {
      state.value += action.payload
    })
})
```


  - `createSlice()`

```js
import { createSlice } from '@reduxjs/toolkit'

const initialState = { value: 0 }

const counterSlice = createSlice({
  name: 'counter',
  initialState,
  reducers: {
    increment(state) {
      state.value++
    },
    decrement(state) {
      state.value--
    },
    incrementByAmount(state, action) {
      state.value += action.payload
    },
  },
})

export const { increment, decrement, incrementByAmount } = counterSlice.actions
export default counterSlice.reducer
```


