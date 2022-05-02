# Context API

## Context

- [**Context**](https://reactjs.org/docs/context.html) allows data to be passed to a component without having to pass props down from one child to the next.
- Let's look at an example from the [react docs](https://reactjs.org/docs/context.html) on how **context** is used to pass data down the component tree without passing props from one to the next:

```js
// Context lets us pass a value deep into the component tree
// without explicitly threading it through every component.
// Create a context for the current theme (with "light" as the default).
const ThemeContext = React.createContext('light');

class App extends React.Component {
  render() {
    // Use a Provider to pass the current theme to the tree below.
    // Any component can read it, no matter how deep it is.
    // In this example, we're passing "dark" as the current value.
    return (
      <ThemeContext.Provider value="dark">
        <Toolbar />
      </ThemeContext.Provider>
    );
  }
}

// A component in the middle doesn't have to
// pass the theme down explicitly anymore.
function Toolbar() {
  return (
    <div>
      <ThemedButton />
    </div>
  );
}

class ThemedButton extends React.Component {
  // Assign a contextType to read the current theme context.
  // React will find the closest theme Provider above and use its value.
  // In this example, the current theme is "dark".
  static contextType = ThemeContext;
  render() {
    return <Button theme={this.context} />;
  }
}
```

## API

`React.createContext`

```js
const MyContext = React.createContext(defaultValue);
```

- This is used to create a *Context Object*.
- A component need to subscribe to that object then read the value of it from the closest matching `Provider` above it in the tree.

`Context.Provider`

```js
<MyContext.Provider value={/* some value */}>
```

- Every Context object comes with a Provider component allowing them to subscibe to context changes.
- [From React Docs](https://reactjs.org/docs/context.html) **:**

>The Provider component accepts a **value** prop to be passed to consuming components that are descendants of this Provider. One Provider can be connected to many consumers. Providers can be nested to override values deeper within the tree.

`Context.Consumer`

```js
<MyContext.Consumer>
  {value => /* render something based on the context value */}
</MyContext.Consumer>
```

- This allows for components to subscribe to a *context* within a **function component**.
- The `value` will equal the value of the closest `Provider`, if there is no value then it will go with the **default value** from the `createContext` object.

`Context.displayName`

```js
const MyContext = React.createContext(/* some value */);
MyContext.displayName = 'MyDisplayName';

<MyContext.Provider> // "MyDisplayName.Provider" in DevTools
<MyContext.Consumer> // "MyDisplayName.Consumer" in DevTools
```

