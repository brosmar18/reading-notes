# Binary Trees

## Overview: 

A binary tree is a fundamental data structure in computer science, used to store data in a hierarchical manner. It consists of nodes, where each node has at most two children, typically referred to as the left child and the right child. 

## In Simple Terms: 

Imageine a family tree, but every person (node) can only have up to two children. This structure helps in orgamizing data in a way that allows for efficient operations like searching, inserting, and deleting. 

## Key Terms: 

1. **Node: ** An element in the tree containing data and links to child nodes. 
2. **Root: ** The topmost node of the tree, without a parent. 
3. **Leaf: ** A node without any children. 
4. **Depth: ** The number of edges from the root to a node. 
5. **Height: ** The number of edges on the longest path from a node to a leaf. 

## Syntax: 

In JS, a binary tree can be implemented using classes and objects. Here's a basic structure: 
```js
class TreeNode {
  constructor(data) {
    this.data = data;
    this.left = null;
    this.right = null;
  }
}

class BinaryTree {
  constructor() {
    this.root = null;
  }
  
  // Methods like insert, delete, search will be added here. 
}
```

## Example: 

Creating a simple binary tree with three nodes: 
```js
let tree = new BinaryTree();
tree.root = new TreeNode(1);
tree.root.left = new TreeNode(2);
tree.root.right = new TreeNode(3);
```

This code sets up a tree like this: 
```
    1
   / \
  2   3
```

### Breakdown: 

- **TreeNode Chass: ** Defines the structure of each node (data, left child, right child). 
- **BinaryTree Class: ** Represents the entire tree, starting from the root. 
- **Creating Nodes: ** `new TreeNode(data)` creates a new node with the given data. 
- **Setting up the tree: ** Assigning left and right children to nodes constructs the tree. 

## Related Topics: 

1. **Binary Search Trees (BSTs): ** A type of binary tree with ordered elements. 
2. **Tree Transfersal: ** The process of visiting all nodes in a tree (e.g., in-order, pre-order, post,order). 
3. **Balanced Trees: ** Binary trees where the left and right subtrees of any node differ in height by no more than one. 
4. **Tree Rotations: ** Operations in balanced trees to maintain their properties. 

## Summary: 

Binary trees are versitile data structures and enable efficient data management and operations. They form the basis for more complex tree types like BSTs and AVL trees. Understanidng binary trees is crucial for grasping more advanced data structure concepts in software development. 







