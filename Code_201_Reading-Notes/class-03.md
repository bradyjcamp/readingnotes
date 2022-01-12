# HTML Lists, Control Flow with JS, and the CSS Box Model

## HTML Lists

- There are three types of lists with HTML:
  - Ordered lists
    - Each part of this list is numbered and is used for content like recipes or step by step instructions.
    - Uses the element `<ol>`.
  - Unordered lists
    - This list is what is used when listing bullet points with little to no order required.
    - Uses the element `<ul>`.
  - Definition lists
    - This list includes a list of terms and their definitions
    - Uses the element `<dl>`.
- Once the type of list is defined by an opening element tag, to actually create the content in the list you use the `<li>` and `</li>` tags.
- Place each line of the list within their own `<li>` tags.
  - `<li>` tags do not apply for definition lists.
    - Use `<dt>` and insert the word that will be defined within it.
    - Then use `<dd>` to explain the definition of that word.
- You can add a **nested list** within a list as well to create a sub-level of lists.

## CSS Boxes

- Whenever CSS is styling HTML elements, it will display and think of each element as its own box. Therefore, it is important to always set some dimensions of that box and ensure everything is sized correctly.
- This can be done by adding `height` and `width` features to the HTML element you are styling.
  - For example:
```
div{
  height: 300px;
  width: 400px;
  background color: green;
}
p{
  height: 75%;
  width: 75%;
  background color: grey;
}
```
Duckett, John. _HTML & CSS: Design and Build Websites._ John Wiley and Sons, 2014.

- This is setting the *height* and *width* of the box behind the paragraph element, and also setting the *height* and *width* of the paragraph box.
- You can also use `min-width` and `max-width`, or `min-height` and `max-height` to set a maximum and minimum width and height for the browser. This is helpful if a user is using the browser on a smaller screen or changing the size of it.
- If the box is too small for the contents of the paragraph, then you can use the `overflow: hidden;` or `overflow: scroll;` elements on CSS to either hide the content when it runs out of room in the box, or the user can scroll down to see more.

### Border, Margin, and Padding

- The **padding** is the box around the **context box**, it is the closest layer.
  - Change the padding dimensions and size to create space from the text to the border.
- The **border** then goes around the **padding** and most time is not visible unless specified otherwise.
  - Borders can have any width and you can also assign different styles and colors.
- The **margin** is the outer most box that creates space around the *padding* and *border*.
  - Margin can create space from outside the border.
- Border Images
  - When yoou add a border image, it is usually sliced into 9 individual pieces.
  - This property requires three pieces of info:
```
p.one {
  -moz-border-image: url("images/dots.gif") 11 11 11 11 stretch;
  -webkit-border-image: url("images/dots.gif") 11 11 11 11 stretch;
  border-image: url("images/dots.gif") 11 11 11 11 stretch
}
```
Duckett, John. _HTML & CSS: Design and Build Websites._ John Wiley and Sons, 2014.


- You can change the value from **stretch** to **repeat**, or **round** as well.
- Box Shadows follows a similar layout:
```
-moz-box-shadow: px, px, px, px, color;
-webkit-box-shadow: px, px, px, px, color;
box-shadow:px, px, px, px, color;
```
Duckett, John. _HTML & CSS: Design and Build Websites._ John Wiley and Sons, 2014.

## Arrays

- Arrays store a list of elements not just one.
  - Contains strings, numbers, booleans, arrays, objects
  - They can be given a name as well to go with the values.
- They do not have predetermined size of arrays.
- Data type or data structure **special type of ebject**
- Every element in the array has an index(location reference)
- Array values can be referenced using numbers.
  - If an array had a list of 5 values and you wanted to reference the first value, you would enter `name[0]`.
  - The index value starts at 0 so your first item would be `[0]`.
    - Zero based index system
- Build in Methods!
  - `.push()`, `.pop()`, `.includes()`.
-Properties
  - `length`

## Switch Statements

- Switch statements are useful when you have multiple possible values for a variable and they run quicker than if than statements by using the keyword **break**.
- In the example below, based on what level the user is on, they will get a different message:

```
var msg;        // Message
var level = 2;  // Level

// Determine message based on level
switch (level) {
case 1:
    msg = 'Good luck on the first test';
    break;

case 2:
    msg = 'Second of three - keep going!';
    break;

case 3:
    msg = 'Final round, almost there!';
    break;

default:
    msg = 'Good luck!';
    break;
}

var el = document.getElementById('answer');
el.textContent = msg;
```
Duckett, John. JAVASCRIPT &amp; JQUERY: interactive front-end web development. John Wiley and Sons, 2014.