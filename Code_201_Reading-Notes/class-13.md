# Local Storage

- **Cookies** are there to hold a very small amount of data on web applications.
  - They can slow down your applications and even send unencrypted data over the internet.
- Local storage is there to improve the users experience and make web apps and web browsing for customizable to the user.

## HTML5 Storage

- Also known as *Local Storage* or *DOM Storage*
- It is a way to store named *key/value* pairs locally.
- The difference between this and cookies is that local storage data is never automatically sent out to remote web servers.
- The data can be any JavaScript type but is stored as a *string*.
  - If you are storing anything other than a sting you will need to use functions to revert that type to string (`parseInt()`).
- This is created and used as an *Object*.

```js
interface Storage{
  this.getItem();
  this.setItem();
}
```

- 2 common *methods* used in Storage object in JS are `getItem('string')` and `setItem('string')`.
  - Or, you can use *square brackets* `[]` to replace the words getItem and setItem.
- You can also use methods for removing a value.
  - `removeItem()`
  - Then use `clear()` to delete all the keys and values at once.
- To get the total number of values being stored use:
  - `key()` with the index.

[Info Referenced Above Found at This Site](http://diveinto.html5doctor.com/storage.html)
