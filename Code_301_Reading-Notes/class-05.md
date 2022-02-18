# Thinking in React

- The following questions are answered below:
  - What is the single responsibility principle and how does it apply to components?
  - What does it mean to build a ‘static’ version of your application?
  - Once you have a static application, what do you need to add?
  - What are the three questions you can ask to determine if something is state?
  - How can you identify where state needs to live?

## Steps to Creating a Mock in React

- Step 1
  - Break up the potential components into a hierarchy.
  - How to determine what should be it's own component?
    - Use the **single responsibility principle**.
      - This principle basically means that every individual class or function should each contribute just a single part of the functionality of the app.
      - This means that a *component* should only do one task.
      - Remember that it is always best practice to come back and refactor if the *component* gets bigger.
- Step 2
  - Build a *static* version in React
    - This means that you are implementing all of the needed statements to achieve the visual of the app, not the functionality or UI aspects.
    - Ensure that for this you use **props** and do not use **state** because state is used mostly for interactivity or data that changes.
- Step 3 
  - Identify The Minimal Representation of UI State
  - This is where you bring in **state**
    - **State** will allow UI interactivity to change the state of the underlying data.
    - It helps to think about all of the pieces of data you will need in your App.
      - Then go through each one and determine if it is **state** data.
      - Ask yourself the following questions to help understand which one is **state**:
        - Is it passed in from a parent via props? If so, it probably isn’t state.
        - Does it remain unchanged over time? If so, it probably isn’t state.
        - Can you compute it based on any other state or props in your component? If so, it isn’t state.
          - [source](https://reactjs.org/docs/thinking-in-react.html)
- Step 4
  - Identify Where your State Should Live
    - Use these steps to help with that determination:
      - For each piece of state in your application:
        - Identify every component that renders something based on that state.
        - Find a common owner component (a single component above all the components that need the state in the hierarchy).
        - Either the common owner or another component higher up in the hierarchy should own the state.
        - If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.
          - [Source](https://reactjs.org/docs/thinking-in-react.html)
- Step 5
  - Add Inverse Data Flow
    - This is achieved by using the `onChange` event calling `setState()` on that data. 
- All of these steps where found in this [link](https://reactjs.org/docs/thinking-in-react.html)

## Higher-Order Functions

- The following questions are answered below:
  - What is a “higher-order function”?
  - Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?
  - Explain how either map or reduce operates, with regards to higher-order functions.
- Higher-Order Functions
  - It is defined as:
    > Functions that operate on other functions, either by taking them as arguments or by returning them, are called higher-order functions.
    - [Source](https://eloquentjavascript.net/05_higher_order.html#h_xxCc98lOBK)
  - Let's take a look at an example:

        ```js
        function greaterThan(n) {
          return m => m > n;
        }
        let greaterThan10 = greaterThan(10);
        console.log(greaterThan10(11));
        ```

    - [source](https://eloquentjavascript.net/05_higher_order.html#h_xxCc98lOBK)
- On line 2 we see the function returning a value that if `m` in this case is greater than `n` then it is `true`
- We then see another function being defined called `greaterThan10`.
  - This function is being assigned to the value of the prior function with an argument passed through of 10.
- Using map with higher-order functions will invoke the function on all values in the array and also invoke the function as one of the parameters of the original function.