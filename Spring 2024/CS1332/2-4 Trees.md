## Complexities

$O(\log n)$ for all operations since shape is contrained. (leaves are on same level)

- Last Data Structure of the course.
- This is a b-tree but smaller and simplified
- Each node has 1,2, or 3 data items
- Each node has 2,3,or 4 children
- Rule: \#kids = \#data +1
- All leaves must be at the same depth
![[Pasted image 20240226144025.png]]

## Adding
Instead of creating a leaf, add to the node list.

If node is already full, promote second or third data item to the parent and split the rest of the leaf in two.

If the root overflows, promote one thing into a new root. Split the old root into two.

Runtime $O(\log n)$

## Removing
![[Pasted image 20240304223100.png]]




