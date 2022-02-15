# State and Props

- State
  - local or only inside a specific component or child
- Props
  - Data passed from parent to child
  - arguments to a function
  - pass props into a component we want to render
  - can be changed by parent component

### Questions and Responses

- What types of things can you pass in the props?
  - arguments.
- What is the big difference between props and state?
  - props are passed into a component and handled outside of the component where as state is handled inside the component.
- When do we re-render our application?
  - When state is changed then the application will rerender
- What are some examples of things that we could store in state?
  - state can be used to increment or decrease a counter that is defined inside the component.

## React Lifestyle

- In react, you can define components as either classses or functions, the methods usd on those are called **lifecycle events**.
- The three phases are called **Mounting**, **Updating**, and **Unmounting**.

### Mounting

- This is the phase where an instance of a component is being made and put into the DOM.
  - *constructor, getDericedStateFromProps, render, componentDidMount*

### Updating

- This is when an update or state is changed to a component then rerendered.
  - *getDerivedStateFromProps, shouldComponentUpdate, render, getSnapshotBeforeUpdate, componentDidUpdate*

### Unmounting

- Final phase called when component is being removed from DOM.
  - *componentWillUnmount*

#### constructor()

- Called before mounted
- Must call super(props) if the component is a subclass.
>
 ```js
class FishTableRow extends React.Component {

  constructor() {
    super(props); //gives us access to props
      //Don’t call this.setState() here
    this.state = { //intitialize local state
    showDescription: false
  }; 
}
```

- [Source](https://medium.com/@joshuablankenshipnola/react-component-lifecycle-events-cb77e670a093)

#### render()

- Required method in a class component. 
- Examines this.props and this.state when called

#### componentDidMount()

- Invoked right after component is mounted

> Here we use componentDidMount() to connect to the YouTube API and get videos when the components is rendered.

```js
componentDidMount() {

  console.log(‘got videos’);
  this.getVideos(‘cats’);
}

getVideos(query) {

  var options = {
    key: this.props.YOUTUBE_API_KEY,
    query: query
  };
}
```

- [Source](https://medium.com/@joshuablankenshipnola/react-component-lifecycle-events-cb77e670a093)

#### shouldComponentUpdate()

- React will rerender after every state change by default.
  - This method being set to false prevents that.

#### componentDidUpdate()

- Takes in network requests after change

>
```js
componentDidUpdate(prevProps) {

// Typical usage (don’t forget to compare props):
  if (this.props.userID !== prevProps.userID) {
    this.fetchData(this.props.userID);
  }
}
```

- [Source](https://medium.com/@joshuablankenshipnola/react-component-lifecycle-events-cb77e670a093)

### Questions and Responses

- Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?
  - *render* with happen first.

- What is the very first thing to happen in the lifecycle of React?
  - *constructor method*

- Put the following things in the order that they happen: componentDidMount, render, constructor, componentWillUnmount, React Updates
  - *constructor, render, React Updates, componentDidMount, componentWillUnmount*

- What does componentDidMount do?
  - it is used to load anything using a network request or to initialize the DOM.

## Things I want to know more about

- I would like to see more examples of what state looks like and what props look like
