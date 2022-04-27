# Understanding Hooks

## [Making Sense of React Hooks](https://medium.com/@dan_abramov/making-sense-of-react-hooks-fdbde8803889)

- Hooks let us organize logic inside of a component into reusable units.

- Hooks apply the React philosophy (explicit data flow and composition) inside a component, rather than just between the components.

> **Do Hooks Make React Bloated?**
Before we look at Hooks in detail, you might be worried that we’re just adding more concepts to React with Hooks. That’s a fair criticism. I think that while there is definitely going to be a short-term cognitive cost to learning them, the end result will be the opposite.

## [Example](https://reactjs.org/docs/hooks-state.html)

```js
import React, { useState } from 'react';

function Example() {
  // Declare a new state variable, which we'll call "count"
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
```

