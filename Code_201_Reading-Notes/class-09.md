# Forms and JS Events

## Form Controls

- There are several types of form controls.
  - **Adding Text**
    - _Text Input_
      - single line for short text like emails
    - _Password Input_
    - _Text Area_
      - multiple lines for longer text
  - **Making Choices**
    - _Buttons_
    - _Checkboxes_
    - _Drop-down Boxes_
  - **Submitting Forms**
    - _Submit Buttons_
    - _Image Buttons_
    - _File Upload_
- A form used **name/value pairs**

```js
username = Ivy;
vote = Herbie;
```

- Form uses the `<form>` element.

```html

<form action = "http://www.example.com" method = "get">
  <p>Form controls will appear here</p>
</form>
```

- The `<input>` element is used to create several different form controls.

```html
<input type="text" name="username" size="15" maxlength ="30">
```

- Text Area

```html

<textarea name="comments" cols="20" rows="4">Enter your comments </textarea>
```

Duckett, John. _HTML & CSS: Design and Build Websites._ John Wiley and Sons, 2014.

## JS Events

- addEventListener Function
  - the `e` is the **Event Object**
  - 2 *parameters* in the event function
    - first parameter is the type of even you want to listen for.
    - second is a callback, it is a function that runs every time we do what the event is.

```js
let clickHere = document.getElementById('box'); 

clickHere.addEventListener('click', function(e){ //e could also be ev or event
  alert('Hello!');
});

```

- You can also repeat the event function but change the callback function and JS will run both in the order they appear.

- Bubbling
  - **Bubbling** is when you click on the child element, it will also click on its parent, then grandparent, all the way up to the document.

- Capturing
  - **Capturing** starts from the document, then works its way down to the parent, then child elements.
- After a capture event, it will then *bubble* out.

- Example of how to Capture

```js
let old = document.querrySelector('.grandbox')
let parent = document.querrySelector('.parentbox')
let child = document.querrySelector('.childbox')

old.addEventListener('click', function(e){ // function(e) could also be shorthanded down to e =>
  alert('Grand')
}, {capture:true})

parent.addEventListen('click', e => {
  alert('Parent')
})

child.addEventListener('click', e => {
  alert('Child')
})

document.addEventListener('click', e => {
  alert('Document')
})
```

- In this example, the alerts would be in this order:
  - *Grand* (because capture was set to true)
    - The event would work downward because the capture function but would not capture any other elements on the way down because their capture default is false.
    - Once down to child, it would bubble out.
  - *Child*
  - *Parent*
  - *Grand*
  - *Document*

- You can also use the `e.stopPropagation()` method to stop the event from propagating upward or downward.
  - If you place this in a parent or child, then the event will stop there.

```js
old.addEventListener('click', function(e){
  alert('Grand')
})

parent.addEventListen('click', e => {
  e.stopPropagation() alert('Parent')
})

child.addEventListener('click', e => {
  alert('Child')
})

document.addEventListener('click', e => {
  alert('Document')
})
```

- Running an event once

```js
old.addEventListener('click', function(e){
  alert('Grand')
})

parent.addEventListen('click', e => {
  alert('Parent')
}, {once: true})

child.addEventListener('click', e => {
  alert('Child')
})

document.addEventListener('click', e => {
  alert('Document')
})
```

