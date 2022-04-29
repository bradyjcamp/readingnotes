# Hashtables

- A Data Structure that uses key value pairs.
  - Every **Node** or **Bucket** has a key and a value.

## Hashtable Terminology

- **Hash**
  - a hash is an algorithm that takes a string and converts it into a more secure input.
  - used to determine index in array for *hashtable*
- **Buckets**
  - a bucket is at each index and contains a key value pair or multiple key value pairs.
- **Collision**
  - this occurs when more than one key gets hashed into the same location.

## What does it do?

- It hashes a key and stores it so we can easily access the value by searching the key.
- Let's take a look at an example.
  - This example is from [CodeFellows](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)

```js
["Greenwood:98103", "Downtown:98101", "Alki Beach:98116", "Bainbridge Island:98110"]
```

- This is a set of key value pairs and different indexes.
- **Collisions** can occur when more than one key value pair share the same index.
- Typically search an array happens in O(n) because we have to search through each index using a loop until we find the value we want.
- A **hash function** makes it possible to find a value in the hashtable in O(1) time.
- Let's take a look at an example:

```js
let key = 'Brady';
let value = 26;

let bradySum = 410;
let primeNumer = 599;

let product = bradySum * primeNumer;

function hash(key){
  let characters = key.split('');
  let asciiSum = characters.reduce((sum, char) => {
    return sum + char.charCodeAt(0);
  }, 0);
  let initialHash = asciiSum * 599;

  return initialHash % 1024;
}
```

- This is a simple hash function that takes in a key and splits each letter of a string.
- We then use the reduce method to sum up the characters and multiply it my a prime number then take the remainder after dividing by **1024**.
- The key then gets placed at that index.

## Collisions

- Like I mentioned earlier when two key value pairs get resolved to the same index it is called a collision.
- This can cause issues because if we want to access that index there would be 2 different keys living there.
- A solution to this would be to instead of starting indexes or *buckets* at `null`, we can initialize a `LinkedList` at each one.
- That way if two or more keys live at a same index, then can be put into a linked list as Nodes to be individually accessable.
