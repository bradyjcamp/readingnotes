# Debugging

- There is a large list of *Error Types* you can get when trying to debug your JavaScript.
  - **Range Errors**
  - **Reference Errors**
  - **Syntax Errors**
  - **Type Errors**
  - **URI Error**
  - **Eval Error**
  - **Warning**

- A common place to check these errors would be your console on your browser.
- To filter through your code to check if something is working right you can use a `console.log`
- **Console logs**
  - variables
  - make sure things are running how they should
  - console logging is used to one by one go through variables or functions in your code to see if they are working properly.
- **Break points** in Google Chrome dev tools
- Google it
- Linter
- Hover over duplicate variable names and function names to ensure they are all spelt the same.

- **Error Messages**
  - In Google Chrome Console, if there is an error it will tell you what line it is on and what the error is.
  - Reference Error
    - Undefined
    - Variable is assigned but never used.
    - Unreachable code
  - Type Error 
    - NaN!
      - passing a string to a value that should be an integer
  - Syntax Error 
    - Unexpected token

- It is important to understand the **Stack** of your code and make sure things are not nested into a function or loop that shouldn't be.
  - JavaScript reads through your code one line at a time.