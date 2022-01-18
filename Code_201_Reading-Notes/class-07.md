# Tables and Object-Oriented Programming

## Tables

- Tables are a great way to present date or a list of items to the user.
- The main _elements_ used include:

```html
<table>
  <thead>
    <tr>
      <th>This is a table head.</th>
      <th>This is another table head in the same row</th>
      </tr>
  </thead>
  <tbody>
    <tr>
      <th></th>
      <td>100 pounds</td>
      <td>this is the table data</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td></td>
      <td>This is footer data, like a total of above.</td>
    </tr>
  </tfoot>
</table>
```

## Functions, Methods, and Objects

- There are two ways to create objects
  - Literal Notation

```js
let hotel = {
  name: "Quay",
  rooms: 40,
  booked: 25,
};
```

- Constructor Notation

```js
function Hotel (name, rooms, booked){
  this.name = name;
  this.rooms = rooms;
  this.booked - booked;
}
let quayHotel = new Hotel('Quay', 40. 25);
let parkHotel = new Hotel('Park', 120, 77);
```

Duckett, John. JAVASCRIPT &amp; JQUERY: interactive front-end web development. John Wiley and Sons, 2014.

- Use the keyword **this** followed by **.** then the key or property you are wanting to access.

- Browsers come with **built in objects**
  - Browser Object Model
    - Includes a Window: current browser or tab
    - Document: current web page
    - History
    - Location: URL of the current webpage
    - Navigator: info about browser
    - Screen
  - Document Object Model
    - This has all your elements of the page
  - Global JavaScript Objects
    - Groups of individual objects that relate to different parts of the JavaScript language

Duckett, John. JAVASCRIPT &amp; JQUERY: interactive front-end web development. John Wiley and Sons, 2014.

- Creating a date object

```js
let today = new Date();


let dob= new Date(1995, 08, 28);


// once a date object is created, there is a list of methods to set and retrieve time and date.


getDate()
setDate()
getFullYear()
setFullYear()
```

- The syntax for month, hour, minutes, seconds, and miliseconds all start at 0.
  - month: 0-11
  - hour: 0-23
  - minutes: 0-59