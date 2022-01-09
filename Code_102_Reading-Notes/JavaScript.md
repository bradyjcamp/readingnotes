# JavaScript

## What is it?

- It is most popular and best known as the scripting language for web pages.
- Classified as a just-in-time scripting or programming language. Meaning it is not compiled before execution but during execution. 
- Unless you are staring at a static web browser page, then JS is working in the background to provide content updates, interactive maps etc.
- Creates dynamically updating content, controls multimedia, and animates images.
- If you think of HTML as content, CSS as the look, then JS would be the behavior.
- It is a programming or scripting language. 
  - Programming language is language that we use to tell the computer what to do using data and features available.
  - Syntax is more straight forward.
- Data types
  - String
    - Group of text character, used to represent natural language (like this sentence).
  - Number
    - Quantitative value that represents all fractions, decimals, integers.
  - Boolean
   - A set of two value: **True and False**
  - lack of date = null and undefined
- Browser behavior
  - JS can prompt User with an input box.
  - It can also print text to the console
  - It makes http requests.
  - semicolons are optional but should stay consistent.

## What are Variables, Const, and Let?

- Containers for storing values
```
 var x = 11;
 var y = 6;
 var z = x + y;
 ```
- Then `z` = 17
- In this instance, if you were to replace `var` with `let` or simply leave them undeclared, you would get the same outcome.

- Wherever you place `**<p id="demo"></p>**` is where your outcome will be on your html page. 

### When to use Variables?

- Always declare JavaScript variables with `var`, `let`, or `const`.
- `var` is used in JS up to 2015, `let` and `const` were added after. Running JS in an old browser must use `var`
- Keep in mind, if you think the value of the variable can change, use `let`.

### When to use Const?

- If you want a general rule: always declare variables with `const`.
- If you think the value of the variable can change, use `let`.
``` 
const price = 10;
const price2 = 20;
let total = price + price2;
```
- Variables are much like basic algebra.

## Identifiers

- All JS **variables** must be **identified** with **unique names**.
- These unique names are called **Identifiers**.
- Identifiers are what you label the variable or `const`.
  - Names can contain letters, digits, underscores, and dollar signs.
  - Names must begin with a letter, $, or _, just keep in mind they that even $ and _ is treated like a letter.
  - Names are case sensitive (y and Y are different variables).
  - Reserved words (like JavaScript keywords) cannot be used as names.
- In JavaScript, the equal sign (=) is an "assignment" operator, not an "equal to" operator.
- The "equal to" operator is (==) in JS.

## JS date types

- **Strings are written inside double or single quotes. Numbers are written without quotes.**
- Below is the code of how you can use variables, `const` and `let` using JS. 
```
<!DOCTYPE html>
<html>
<body>

<h1>JavaScript Variables</h1>

<p>Strings are written with quotes.</p>
<p>Numbers are written without quotes.</p>

<p id="demo"></p>

<script>
const pi = 3.14;
let person = "John Doe";
let answer = 'Yes I am!';

document.getElementById("demo").innerHTML =
pi + "<br>" + person + "<br>" + answer;
</script>

</body>
</html>
```
- `"<br>"` is a line break.
- Be sure to always add `" "` for implementing a space in your `document.getElementByID("demo").innterHTML =` OtherwiseTheOutcomeWillHaveNoSpaces
- Use parentheses for strings but not for numbers! If you put parentheses around numbers they will be display side by side, not added.

## How Computer Work!
- What makes a computer a computer?
  - It is a tool!
  - Designed to help with thinking work like equations /
- It takes **Input** -> **Stores Data** -> **Processes** -> **Output**
  - Input is what we type in or what we want it to do
  - The input is then stored in memory
  - The processor then manipulates the stored date to change to output
- It is designed to display image, text, photos, videos, games, or signals.
- Binary and Data
  - Binary
    - Circuit wires in the hardware chips are used to either select 1 or 0 in the computers native binary language. 1 means they are on, 0 means they are off.
    - The more info that is needed, more bits are used.
    - In binary there are only 2 numbers used but each position as it progresses is multiplied by x 2.
    - To get the number 9 in binary, you put in 1001. (1x8)(0x4)(0x2)(1x1) = 9.
   - Letters are assigned numbers.
    - Pixels
    - Displays images.
    - Millions of pixels in an image.
  - Sound
    - Soundwaves can also be nailed down into sound.
    - Think of 8 bit as lower quality. 32 bit is better quality.
- Circuits
  - The smaller the circuit is, the faster the info can get to where it needs to be.


# More on JavaScript


## Control Flow


- Typically computers will read a line of code from top to bottom, unless there are **conditionals** or **loops** added
  - A **condition** is a set of rules that can interrupt normal code execution or change it, depending on whether the condition is completed or not. (think of instructions, if done correctly you will go to instruction A, if wrong, go to instruction B)
- JS uses `if`... then `else`
```js
if (field==empty) {
    prompt();
} else {
   submitForm();
}
```
## Functions


- Any JS operation or set of operations that should be repeated. Provides a syntax for turning operations into a repeatable "thing"
- JS Function signature
```js
// "function" keyword, followed by a name for the function, followed by parentheses, followed by a pair of curly brackets.


let words = 'is it morning yet';


// function defined with the words parameter/


function functionName(words){
//the things the function needs to do go here.
}


//invoke functionName


functionName('Is it morning yet'); // our argument


//argument is created on invoke of function




function calculateTime(time) {
  if (time < 12) {
    return 'it is morning';}
  else {
  return 'it is evening';}
}
```
- arguments / parameters
  - Arguments are the values that are passed into the function on 'invocation'
  - Parameter is a variable we define in the parentheses of our function signature.
  - the argument is the value that is assigned to the parameter
  - Return values
    - Stops your function from running
- A JavaScript function is a block of code designed to perform a particular task.
- Function is executed when something invokes it


## JS Topics


- Expressions
  - line of code or JS operations that evaluates to some value.
```js
let words = 'name';
if (words > 10) {
console.log('works');
} else {
console.log('doesn't work);
}


//inverse example


let itAwesome = false;


if (!itAwesome) {
console.log('You are awesome');
}


OUTCOME You are awesome
```
-Operators
  - <: less than
  - >: greater that
  - +: increment one (plus)
  - -: decrement one
  - &&: logical AND
  - ||: logical OR
  - !: logical NEGATION / INVERSE
  - ==: equal to
  - ===: strictly equal to


```js


let number = 10;


if (number < 10 && number > 5) {
  console.log('your number is between 5 and 10');
} else {
    console.log('your number is not between 5 and 10');
}


//when you add function and input you do not have to put in data every time 


function compareNumber(number) {
if (number < 10 && number > 5) {
  console.log('your number is between 5 and 10');
} else {
    console.log('your number is not between 5 and 10');
}


}
```
```js


function makeASandwich(){


let bread = prompt('what bread do you like?');
let meat = prompt('what meat do you like?');
let cheese = prompt('what cheese do you like?');


return 'Here is a sandwich with ' + bread + ',' + meat + ',' + cheese + ',';
}


```
  