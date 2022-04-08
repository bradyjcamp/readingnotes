# Trees

- Some different types of trees include **Binary Trees**, **Binary Search Trees**, and **K-ary Trees**.

## Common Terminology

- **Node**
  - Has been covered previously.
- **Root**
  - Refers to the Node at the beginning of the tree.
- **K**
  - Refers to the max amount of children a Node can have in a k-ary tree. In a binary tree, k = 2.
- **Left**
  - Refers to one child node in a binary tree.
- **Right**
  - Refers to the other child node in a binary tree.
- **Edge**
  - This refers to the link between a parent node and a child node.
- **Leaf**
  - Refers to a Node that does not have any children.
- **Height**
  - This refers to how many *Edges* there are from the *Root* to the furthest *Leaf*

## Binary Trees

- Diagram from [Code Fellows Article](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html):

![Binary Tree](/img/BinaryTree.png)

### Traversals

- Traversing is how we search for a specific Node, view the contents of a tree and much more.
- There are two ways to Traverse, Depth First and Breadth First

### Depth First

- This method goes through the tree through the height of it first.
- Uses a **Stack**
- There are 3 methods in depth first traversal:
  - Pre-order `root >> left >> right`
  - In-order `left >> root >> right`
  - Post-order `left >> right >> root`

- Diagram from [Code Fellows Article](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html):

![Tree Traversal](/img/tree-example.png)

- Based on the Diagram above
  - Pre-order: `A, B, D, E, C, F`
  - In-order: `D, B, E, A, F, C`
  - Post-order: `D, E, B, F, C, A`

- The most common way to traverse through a tree is to use **recursion**
  - We will look at the Algorithm for each:
- Pre-Order:

```js
ALGORITHM preOrder(root)

  OUTPUT <-- root.value

  if root.left is not NULL
      preOrder(root.left)

  if root.right is not NULL
      preOrder(root.right)
```

- Pre-order means that the *root* has to be looked at first

![Tree Depth Traversal](/img/TreeDepthTraversal.png)

`OUTPUT <-- root.value`

> This means that we will output the root.value out to the console. Then, our next block of code instructs us to check if our root has a left node set. If the root does, we will then send the left node to our preOrder method recursively. This means that we make another function call, where B is our new root:

- [Source](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)

- Here is the Pseudocode for the other **depth first** traversal methods:

```js
ALGORITHM inOrder(root)
// INPUT <-- root node
// OUTPUT <-- in-order output of tree node's values

    if root.left is not NULL
        inOrder(root.left)

    OUTPUT <-- root.value

    if root.right is not NULL
        inOrder(root.right)
```

```js
ALGORITHM postOrder(root)
// INPUT <-- root node
// OUTPUT <-- post-order output of tree node's values

    if root.left is not NULL
        postOrder(root.left)

    if root.right is not NULL
        postOrder(root.right)

    OUTPUT <-- root.value
```

### Breadth First

- This Traversal method goes through the tree by going through each level of the tree node-by-node.
- Diagram from [Code Fellows Article](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)
- The output would be `A, B, C, D, E, F`.
- Breadth first uses a **Queue**
- See the Code Fellows Article to look through the diamgram for this [traversal method](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)

- PseudoCode utilizing built-in queue to implement a breadth first traversal

```js
ALGORITHM breadthFirst(root)
// INPUT  <-- root node
// OUTPUT <-- front node of queue to console

  Queue breadth <-- new Queue()
  breadth.enqueue(root)

  while ! breadth.is_empty()
    node front = breadth.dequeue()
    OUTPUT <-- front.value

    if front.left is not NULL
      breadth.enqueue(front.left)

    if front.right is not NULL
      breadth.enqueue(front.right)
```

## K-ary Trees

- When nodes can have more than two child nodes, it is considered a **k-ary tree**

>Traversing a K-ary tree requires a similar approach to the breadth first traversal. We are still pushing nodes into a queue, but we are now moving down a list of children of length k, instead of checking for the presence of a left and a right child.

- [Source](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)

![k-ary tree](/img/KaryTree.png)

