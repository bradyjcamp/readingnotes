# Node Ecosystem, TDD, CI/CD

## .map()

- The [`.map()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map) method iterates through every index of an array and applies some sort of function to each value in the array.
- It then returns a new array.

## .reduce()

- The [`.reduce()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce) method also iterates through an array and applies a callback function. You can set starting points based on different indexes and returns an accumulator value.

## superagent()

- [`Promise` and `.then`](https://codefellows.github.io/code-401-javascript-guide/curriculum/prework/promises/DEMO.html)

```js
superagent.get('http://demo8340031.mockable.io/stuff')
  .then( data => {
    console.log(data.body);
  })
  .catch(err => console.error(err));
```

- [`async` and `await`](https://codefellows.github.io/code-401-javascript-guide/curriculum/prework/async-await/DEMO.html)

```js
async function getStuff() {
  let results = await superagent.get('http://demo8340031.mockable.io/stuff');
  console.log(results.body);
}

getStuff();
```

- *Promises* are a way to oversee of manage asynchronous functions or actions. This means they let a function go ahead and do what it needs to do while the promise goes ahead and continues to execute.

- Callback functions are not considered to be asynchronous by nature. They are functions that pass arguments to another and are called later. More often than not asynchronous calls are often callback functions.
