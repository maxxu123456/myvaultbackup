Tree
* Non Linear
* Data is in nodes
* Nodes are either parent or child
* A node may have any number of children
* A node may have at most 1 parent
	* Root has 0 parent
* There is only 1 root

Def: a leaf is a node with no kids
Def: an internal node is a node that is not a leaf
Def; The ancestors of a node are the nodes parents, and the parent's parents, and so on
Def: THe descendents of a node are the kids, and teh kid's kids, and so on
Def: siblings are nodes with the same parent


Depth: Distance from the root
The depth of the root is 0
depth of a node: depth of a parent + 1

Height:
Height of leaf: 0
Heighte of a node: max(height of the kids) +1


Rules:
* Trees have no cycles
* A cycle is a walk where you can go back to where to started

A binary Tree is a tree where you can have at most two children.
We call the children the left child and the right child.

3 Possible Properties of binary tree

Def: a full binary tree is one where each node has exactly 0 or 2 kis. No nodes have just 1.

Def: a binary tree is complete if
1. Each level except the last has teh maximum number of nodes
2. the last level must be filled left to right

Def: a node is balanced if its children heights differ by 0 or 1 (height of a missing child is -1)
Def: a tree is balanced if all of its nodes are balanced
Note: A leaf is always balanced


