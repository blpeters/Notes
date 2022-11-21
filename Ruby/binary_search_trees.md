# Binary Search Trees

## Traversal

Tree traversal is the process of visiting each node in the tree exactly once in some order. Visiting would be considered reading/processing data in the node.

### Breadth-First Traversal or Search (BFS)

This is visiting all nodes on the same depth or level before continuing deeper to the next level. Top root node is considered depth d = 0. Also known as L-0.

Walking through left-to-right in each level is called _Level Order Traversal_

### Depth-First Traversal or Search (DFS)

Depth-first is when you visit all children and grandchildren of a node before visiting the next child or node.

This allows for different orders of operations, which creates three types of depth-first traversals - Preorder, Inorder, Postorder

Traditionally, the left subtree is always visited before the right subtree, but the root can be visited before, between or after the left and right - This gives us three types.

#### Preorder Traversal

root = D, so shorthand is DLR

<ROOT><left><right>

#### Inorder Traversal

Shorthand is LDR. Inorder Traversal will return a SORTED LIST in a binary search tree.

<left><ROOT><right>

#### Postorder Traversal

Shorthand is LRD.

<left><right><ROOT>
