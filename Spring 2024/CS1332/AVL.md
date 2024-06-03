An AVL is a BST that is never degenerate, by forcing bst to always be balanced, it can never be degenerate.

Balance factor of a node: node.left.height-node.right.height

0: perfectly balanced
1: leaning left, but ok
-1: leaning right, but ok
$\geq 2$: unbalnced to the left
$\leq-2$ unbalnaced, to the right

![[Pasted image 20240221143613.png]]


```
add():
	if curr.data = data:
	...
	if curr.data <  data:
	...
	if curr.data > data:
	...

	update(curr)
	if curr.bf is bad:
		fix tree
```