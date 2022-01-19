# CSS Layout

## Understanding Display

- Display in CSS can be used to determine if the code will be inline or a block.
- Block content will start up top and end down low.
- Inline will start from the left and end on the right.
- Display can also determind how children elements will behave.

```css
.my-element {
  display: flex;
}
```

> https://web.dev/learn/css/layout/

## Flexbox

- Flexbox layout is one-dimensional.
  - it is laid out on a single axis.
  - the element's children will be placed next to each other.
- Using `align-items`, `justify-content`, and `flex-wrap` properties, you can control how flew children elements behave.
  > https://web.dev/learn/css/layout/

## Review on Layout

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
