
It is a binary tree.
Data must be comparable
every node  must have
	all left decendants are smaller
	all right decendatns are larger



PreOrder Traversal:
- Always have a node before all of its decendants.
- Pre order is unique for BST's?
	- Two different trees definitely have two  different pre order traversals
	- given a traversal, can reconstruct the original tree
- BST.add() in preorder produces the original tree

Implementation of PreOrderPrint():
```java
void printPreorder(Node node)
	{
        if (node == null)
            return;
 
        // First print data of node
        System.out.print(node.key + " ");
 
        // Then recur on left subtree
        printPreorder(node.left);
 
        // Now recur on right subtree
        printPreorder(node.right);
    }
```
Implementation of PostOrderPrint():
```java
    void printPostorder(Node node)
    {
        if (node == null)
            return;
 
        // First recur on left subtree
        printPostorder(node.left);
 
        // Then recur on right subtree
        printPostorder(node.right);
 
        // Now deal with the node
        System.out.print(node.key + " ");
    }
```

Implementation of In Order Traversal:

```java
    void printInorder(Node node)
    {
        if (node == null)
            return;
 
        // First recur on left child
        printInorder(node.left);
 
        // Then print the data of node
        System.out.print(node.key + " ");
 
        // Now recur on right child
        printInorder(node.right);
    }
```


Level Order Traversal

Print Out everything based on depth

depth 0 gets printed first
depth 1 gets printed second etc.

This cant be recursive. Instead we ill do this iteratively.

Plan:

1. Add root ot the queue
2. while the queue is not empty
	1. dequee and print
	2. enque the children of the deque's node

<iframe width="560" height="315" src="https://www.youtube.com/embed/IozGo2kwRYE?si=IN4TXK5N1FMY3whd" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Is level order traversal unique for binary search tree: Yes


Searching a binary search tree:

![[Pasted image 20240131142453.png]]

Numbet of steps in contains in the worse case is the height of the tree.

Why: each step goes down one level, so number of steps is bounded by the number of levels.

Best case height?

A complete tree is the best height. For n nodes in a complete tree, you will have $\log(n)$ height.

So search on a complete tree is $O(\log n)$

The worst case height is where its one long strand

![[Pasted image 20240131143059.png]]

The height is n.

On average, a tree will be $\log n$ height. so the average time complexty is $O(\log n)$
Worse case is $O(n)$

## Add

Search until you get to a leaf node. Then create a new leaf on the left or right.

def Add(data)
	root = addHelper(root, data)

def addHelper(curr, data)
	if curr == null:
		curr = new Node(data)
	if curr.data < data:
		go left
		curr.left = addHelper(curr.left,data)
	if(curr.data > data):
		go right
		curr.right = addHelper(curr.right,data)
	if(curr.data == ndata):
		dont add duplicates


## Remove

BST remove() is on the exam

1. Use the search logic from contains() to find the data to remove

With add, we always add at a leaf node to save effort. Unfortunately, we cannot always remove at a leaf node.

Case 1:
 Node has 0 kids. Just remove the node. The tree leftover is still a binary search tree.

Cas2:
Node has 1 kid. You need to connect child node to the parent node.

![[Pasted image 20240202145032.png]]