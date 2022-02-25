# Functional Programming

- What is functional programming?

> Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data

[Source](https://en.wikipedia.org/wiki/Functional_programming)

- What is a pure function and how do we know if something is a pure function?
  - A **pure function** does not cause any observable side effect and returns the same result when given the same arguements.
    -[Concepts of Functional Programming in Javascript](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)
- What are the benefits of a pure function?
  - They are easier to read and predict making them easier to test.
- What is immutability?
  - This means the state of the data cannot be changed once it is created.
- What is Referential transparency?
  - It means that the function displays the same results on the same inputs.

## Modules and require()

- What is a module?
  - Sort of like a component, it holds similar code in a different file
- What does the word ‘require’ do?
  - grabs the data from a different file
- How do we bring another module into the file the we are working in?
  - Pass the file in my using `require()` and enter the file path ending with a *.js*.
- What do we have to do to make a module available?
  - You need to place module.exports into the module.
- [Reference](https://www.youtube.com/watch?v=xHLd36QoS4k)

## Things I want to know more about

- More in general about require().
