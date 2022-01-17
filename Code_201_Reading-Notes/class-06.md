# Problem Domain, Objects, and the DOM

## Object Literals

> Objects group together a set of variables and functions to create a model of something you would recognize from the real world.

Duckett, John. JAVASCRIPT &amp; JQUERY: interactive front-end web development. John Wiley and Sons, 2014.

- _Variables_ become **properties** inside an object.
- _Functions_ become **methods**.

```js
let hotel = {
  name: "Quay",
  rooms: 40,
  booked: 25,
  gym: true,
  RoomTypes: ["twim", "double", "suite"],
  //These are the properties above
  checkAvailability: function () {
    return this.rooms - this.booked;
  },
  //This is the method and also a function.
};
```

Duckett, John. JAVASCRIPT &amp; JQUERY: interactive front-end web development. John Wiley and Sons, 2014.

- Properties: **Key** ---- **Value**
  - `name` ---- `string`
  - `rooms` --- `number`
  - `booked` -- `number`
  - `gym` ----- `boolean`
  - `roomTypes` - `array`
- Methods:
  - `checkAvailability` - `function`

## Document Object Model - DOM

- DOM Tree
  - Made of 4 main node types
    - Document Node
      - Represents the entire page.
    - Element Nodes
      - These are the elements within HTML
    - Attribute Nodes
      - Attribute that can change an element Node, CSS or JS
    - Text Nodes
      - The text within the Element Node
      - Only value is `nodeValue`
  - Using the DOM tree you can select any element, attribute, or text.
    - You can also use methods like `getElementById()`
