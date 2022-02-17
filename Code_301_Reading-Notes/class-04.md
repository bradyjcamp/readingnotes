# React and Forms

## React Docs - Forms

- A **Controlled Component** is a component that handles form data with the React component instead of my the DOM.
- We should not wait to sore the users responses from the form into state and we should update the state with their responses as they enter becuase this makes the REact state the source of the truth and allows us to pass the value to other UI elements.
- We can target what the user is entering by targeting that value through the event.

- Example Code:

```js
class NameForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {value: ''};

    this.handleChange = this.handleChange.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }

  handleChange(event) {
    this.setState({value: event.target.value});
  }

  handleSubmit(event) {
    alert('A name was submitted: ' + this.state.value);
    event.preventDefault();
  }

  render() {
    return (
      <form onSubmit={this.handleSubmit}>
        <label>
          Name:
          <input type="text" value={this.state.value} onChange={this.handleChange} />
        </label>
        <input type="submit" value="Submit" />
      </form>
    );
  }
}
```

- [Source](https://reactjs.org/docs/forms.html)

## The Conditional (Ternary) Operator 

- We use the **Ternary Operator** to shorten our `if` statments.
- In the example below we refactor the `if`, `else` statement:

```js
if(x===y){
  console.log(true);
} else {
  console.log(false);
}

// Ternary Operator Statement
x===y ? true: false
```

- First you must identify the *condition* you are testing.
  - The result will either ring **true** or **false**
- After the statement is where you impliment the `?` and always right after the `?` is what is executed if the statement is `true`.
- Then after the true outcome you place a `:` then follow it with what will be executed if the statement is `false`

## Things I want to know more about

- I would love to know more about Controlled Components and what they should be used for besides forms or other UI fields.