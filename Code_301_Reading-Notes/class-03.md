# Passing Functions as Props

## Lists and Keys

### Questions and Responses

- What does `.map()` return? 
  - Returns a new array with the results of each value in the original array after the function passed in has gone through them.
- If I want to loop through an array and display each value in JSX, how do I do that in React?
  - By using the `.map()` method
- Each list item needs a unique?
  - key
- What is the purpose of a key?
  - They help to identify which list items have changed.

- [Source](https://reactjs.org/docs/lists-and-keys.html)

## The Spread Operator

- Spread Operator
  - Used to combine arrays, add items, and spread arrays.
  - The syntax is three dots `...`
  - If a function is expecting separate arguments and instead gets an array it will return NaN
    - This is when you use `...`

  ```js
  Math.max(1,3,5)
  //returns 5
  Math.max([1,3,5])
  // returns NaN
  Math.max(...[1,3,5])
  // returns 5
  ```

- [Source](https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab)

- More Examples
  - Copy arrays

  ```js
  const numbers = [1, 2, 3, 4, 5];
  const copyNumbers = [...numbers];
  //returns [1, 2, 3, 4, 5];
  ```

  - Concatenating Arrays

  ```js
  [...arrayOne,...arrayTwo]
  //returns both arrays combined
  ```

### Questions and Responses

- What is the spread operator?
  - quick syntax shortcut `...`
- List 4 things that the spread operator can do.
  - can separate an array into separate arguments
  - copy and array
  - concatenate arrays
  - combine objects
- Give an example of using the spread operator to combine two arrays.
  - Notes example above
- Give an example of using the spread operator to add a new item to an array.
  - Notes example above
- Give an example of using the spread operator to combine two objects into one.

```js
const One = {firstName: 'Brady'}
const Two = {lastName: 'Camp'}
const Three = {...One, ...Two}
```

- [Source](https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab)

## Passing Functions Between Components

### Questions and Responses

- In the video, what is the first step that the developer does to pass functions between components?
  - Create a function within the object
- In your own words, what does the increment function do?
  - it maps through the array and increments the objects count
- How can you pass a method from a parent component into a child component?
  - as a prop
- How does the child component invoke a method that was passed to it from a parent component?
  - this.props.method

- [Video Source](https://www.youtube.com/watch?v=c05OL7XbwXU)
