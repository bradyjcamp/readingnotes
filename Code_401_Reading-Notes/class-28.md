# Component Lifecycles: Effect Hook

- Effect Hooks let you perform side effects in a function component.
  - See an example below from the [React docs](https://reactjs.org/docs/hooks-effect.html)

```js
import React, { useState, useEffect } from 'react';

function Example() {
  const [count, setCount] = useState(0);

  // Similar to componentDidMount and componentDidUpdate:
  useEffect(() => {
    // Update the document title using the browser API
    document.title = `You clicked ${count} times`;
  });

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

- When using a hook, you are setting up something to be done after `render`.
  - This then gets called after the DOM updates.
- **Hooks are called inside components**
  - This is so the function is in scope and no API call needs to made.
- Let's break down this code example from the [React docs](https://reactjs.org/docs/hooks-effect.html)

```js
function Example() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    document.title = `You clicked ${count} times`;
  });
}
```

- The useEffect function is placed inside the `Example` function where useState is also set up.
- useEffect takes in a function which is the *effect*.
  - since it is scoped within the function it is within scope and will be remembered everytime the DOM is updated.
