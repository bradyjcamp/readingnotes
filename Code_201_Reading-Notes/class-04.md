# HTML Links, JS Functions, and Intro to CSS Layout

## Links

- When using links on HTML it is important to use `<a>` or anchor tags.
  - This element is what you put your link inside.
    `<a href="linkToWebsite.com">Link</a>`
- You can put links in an `<ul>` or `<ol>` or use them on your `<nav>` bar to put in links to other pages on your site.
- If you are using a **relative** link that is inside another folder, make sure to first enter that folder name followed by a `/` then the url in that folder.
- To open a new window use `target="_blank"` after entering the href url.
- You can also enter a link to jump to a spot in your web page by giving that heading or paragraph an `id` then using that `id` name after the `href`.

## Layout

- **Block-Level Elements** Start on a new line.
- **Inline Elements** flow within the same line.
- Positioning elements.
  - Normal Flow
    - Each block level element sits on top of the next
  - Relative Positioning
    - This is used to move it from its normal flow position.
    - change _property_ and _value_ to `position: relative` then add offset properties to move left, right, top, or bottom.
  - Absolute Positioning
    - When you add the _property_ and _value_ `position: absolute`, the element will ignore all other element positions regardless of where it is put.
  - Fixed Positioning
    - This is used to keep an element in the same place on the web page even as the user scrolls through.
  - Floating Positioning
    - This is used to _float_ an element to the right or left so other text and elements can go directly beside it.
- **Screen Size** and **resolution** is always something to consider when building a web page.
  - Think to yourself what the user will be using to search your website. Phone, tablet, laptop, or monitor and computer?
- Consider the page size and where things are laid out.
  - **Fixed Width Layouts**
    - These layouts tend to not change size as the user increases or decreases the size of their browser window.
    - Typically measured in pixels
  - **Liquid Layouts**
    - Designed to stretch and contract as the user changes the size of their browser.
- Layout Grids
  - 960 Pixel Wide 12 Column Grid

## JS Functions

> Functions let you group a series of statements together to perform a specific task.

Duckett, John. JAVASCRIPT &amp; JQUERY: interactive front-end web development. John Wiley and Sons, 2014.

- You start by _declaring_ the function. `function`
- Then you add a _name_ to the function. `sayGoodbye()`
- Then you create and fill in a _code block_. `{document.write('Goodbye!');}`
- Next you can **call on the function**
  - This is done by enter the function _name_ follow by parentheses.
- Sometimes, once you _declare_ the function, you will need to give it **parameters** in the parentheses.
  ```js
  // Parameters
  ```

funciton getArea(width, height){
return width \* height;
}

````
Duckett, John. JAVASCRIPT &amp; JQUERY: interactive front-end web development. John Wiley and Sons, 2014.

- Once parameters have been determined, when you call on that funciton, you will need to specify those _values_
  - These values are called **arguments**, and they provide the values on the _variables_ in the parentheses.

```js
// Arguments as Values

getArea(3, 5);

//Arguments as Variables

wallWidth = 3;
wallHeight = 5;
getArea(wallWidth, wallHeight);
````

Duckett, John. JAVASCRIPT &amp; JQUERY: interactive front-end web development. John Wiley and Sons, 2014.

- Getting single value out of a _function_

```js
function calculateArea(width, height) {
  let area = width * height;
  return area;
}
let surfaceOne = calculateArea(5, 8);
let surfaceTwo = calculateArea(10, 10);
```

Duckett, John. JAVASCRIPT &amp; JQUERY: interactive front-end web development. John Wiley and Sons, 2014.

- Getting multiple values out of a function using an array.

```js
function getSize(width, height, depth) {
  let area = width * height;
  let volume = width * height * depth;
  let sizes = [area, volume];
  return sizes;
}

let areaOne = getSize(5, 2, 8)[0];
let volumeOne = getSize(5, 2, 8)[1];
```

Duckett, John. JAVASCRIPT &amp; JQUERY: interactive front-end web development. John Wiley and Sons, 2014.
