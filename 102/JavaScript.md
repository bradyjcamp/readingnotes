# JavaScript

## What is it?

- It is most popular and best known as the scripting language for web pages.
- Classified as a just-in-time scripting or programming language. Meaning it is not compiled before execution but during execution. 
- Unless you are staring at a static web browser page, then JS is working in the background to provide content updates, interactive maps etc.
- Creates dynamically updating content, contols multimedia, and animates images.
- If you think of HTML as content, CSS as the look, then JS would be the behavior.
- It is a programming or scripting language. 
  - Programming language is language that we use to tell the computer what to do using data and features available.
  - Syntax is more straight forward.
- Data types
  - String
    - Group of text character, used to represent natural language (like this sentance).
  - Number
    - Quantitative value that represents all fractions, decimals, intigers.
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
- Variables are much like baisc algebra.

## Identifiers

- All JS **variables** must be **identified** with **unique names**.
- These unique names are called **Identifiers**.
- Identifiers are what you lable the vaiable or `const`.
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
- Be sure to always add `" "` for implemnting a space in your `document.getElementByID("demo").innterHTML =` OtherwiseTheOutcomeWillHaveNoSpaces
- Use parentheses for strings but not for numbers! If you put parentheses around numbers they will be display side by side, not added.

## How Computer Work!
- What makes a computer a computer?
  - It is a tool!
  - Designed to help with thinking work like equations /
- It takes **Input** -> **Stores Data** -> **Processes** -> **Output**
  - Itput is what we type in or what we want it to do
  - The input is then stored in memory
  - The processor then munipulates the stored date to change to output
- It is designed to display image, text, photos, videos, games, or signals.
- Binary and Data
  - Binary
    - Circuit wires in the hardware chips are used to either select 1 or 0 in the computers native binary language. 1 means they are on, 0 means they are off.
    - The more info that is needed, more bits are used.
    - In binary there are only 2 numbers used but each position as it progresses is multuplied by x 2.
    - To get the numnber 9 in binary, you put in 1001. (1x8)(0x4)(0x2)(1x1) = 9.
   - Letters are assigned numbers.
    - Pixels
    - Displays images.
    - Millions of pixels in an image.
  - Sound
    - Soundwaves can also be nailed down into sound.
    - Think of 8 bit as lower quality. 32 bit is better quality.
- Curcuits
  - The smaller the circuit is, the faster the info can get to where it needs to be.
  
  