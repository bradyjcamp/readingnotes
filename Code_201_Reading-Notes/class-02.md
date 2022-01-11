# Basics of HTML, CSS & JS

## HTML Text

- HTML contains all the content for you web page.
- To make the web page more structured for the user, you need to use multiple elements.
- There is a very large list of elements used in HTML but there are a few key elements to use everytime.
  - `<h1>`,`<h2>`,`<h3>`,`<h4>`,`<h5>`,`<h6>`
    - These element tags create different level headings, with one being the main, most prominent.
  - `<p>`
    - This is where you would place text to appear in paragraph form on the webpage.
  - There is also a large list of elements to apply to specific words and phrases. This list can be found in our book, "HTML & CSS: design and build websites"

## Introducing CSS

- CSS gives you the flexibility to style any element in HTML
- You can change background color, text color, text size, and so much more.
- Examples:
```
p {
  color: blue
}
h1{
  background-color: pink
}
```
- The CSS code above changes the color of all paragraph text to blue, and changes `h1` background color to be pink!


- If you want to put your CSS directly in your HTML you would simply put the above elements inside of an opening `<style>` bracket and closing `</style>` bracket.
- You can also source your CSS from another file on your code editor and it would look like this:
`<link href="css/styles.css" type="text/css">`

## Basic JavaScript Instructions

- Similar to HTML and CSS, JS code is read by statements.
  - The script is read one statement at a time and moves down the list.
- Comments, like mentioned before, are important to organize and add notes to help understand the functions in script.
  - Syntax for JS comments are `//` for single line, and `/* */` for chunks including multiple lines.


## Variables


- Throughout the script there will be multiple variables to help identify what we want the functions to reference.
- All variables will have a **name** and a **value** associated with them. See example:


```
let variableName;
variableName = 'variableValue';
```


- You can also shorten the amount of lines needed when defining a variable by using the following steps,


```
let variableName = 'variableValue'
```


- Rules for naming variables are as follow:
  - Must begin with letter, underscore (_), or Dollar sign ($) and can only contain these characters.
  - Cannot use **keywords** or **reserved** words.
  - They are case sensitive.
  - Should be a descriptive name.
  - Must use camel case if name is more than one word.


### Data Types


- JS has three different data types
  - Numeric Data `0.75`
  - String Data `'Hello World'`
  - Boolean Data `true`


### Arrays


- Arrays store a list of values not just one.
- They can be given a name as well to go with the values.
- Array values can be referenced using numbers.
  - If an array had a list of 5 values and you wanted to reference the first value, you would enter `name[0]`.
  - The index value starts at 0 so your first item would be `[0]`.


### Operators


- Operators create a single value from multiple values.
- Types include:
  - Assignment Operators
  - assigns a value to variable
  - Arithmetic Operators
    - performs math to get value
  - String Operators
    - combines two or more strings
  - Comparison Operators
    - compares two values and returns `true` or `false`
  - Logical Operators
    - combine expressions that return `true` or `false`


Duckett, John. JAVASCRIPT &amp; JQUERY: interactive front-end web development. John Wiley and Sons, 2014.


## Decisions and Loops


- To understand **decision** and **loops** we must first think of the flow of the script we are trying to run.
- Within that flow there will be multiple **evaluations**, **decisions**, and **loops**
- When the script comes to a decision, it first evaluates.
  - Was this task done?
  - If answer is yes, it moves on to the next decision.
  - If answer is no, then it may loop you back to the prior instructions.
  - Use the `document.write('string')` function to display on the web page what you are wanting to communicate based on the input.
- Loops will often times use `if` `else` statements
- To set a **condition** you must know which **comparison operator** you are needing to use. These include:
  - `==` (is equal to)
  - `!=` (is not equal to)
  - `===` (strictly equal to) - both the data type and value must match.
  - `!==` (strictly not equal to)
  - `>` (greater than)
  - `<` (less than)
  - `>=` (greater than or equal to)
  - `<=` (less than or equal to)
- Logical operators refer to `true` or `false` values
  - `&&` (logical and)
    - `true && true` returns `true`.
    - `true && false` returns `false`
    - whenever a logical and contains a `false` it is always `false`.
  - `||` (logical or)
    - `true || false` returns `true`
    - `false || true` returns `true`
    - `false || false` returns `false`
  - `!` (logical not)
    -`!true` returns `false`


Duckett, John. JAVASCRIPT &amp; JQUERY: interactive front-end web development. John Wiley and Sons, 2014.