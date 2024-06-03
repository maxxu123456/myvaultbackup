## Complexities
Add and Remove $O(\log n)$


A heap is a binary tree, but not necessarily a binary search tree.

It has two fundamental properties: shape and order

Shape Property: Heaps are always complete.
- All non last layers are filled
- Last layer is filled left to right

Order property: parent always higher priority than kids

Two common heaps are maxHeaps and minHeaps:

Maxheap: parent > kids
Minheap: parent < kids

Example of a Max Heap
![[Pasted image 20240205142027.png]]

Example of a Min Heap:
![[Pasted image 20240205142055.png]]

Because there are no gaps in a complete tree, we will store heaps as arrays.

When creating the array, index 0 is empty. Heap starts at index 1. Then store the level order traversal.

![[Pasted image 20240205142615.png]]

Parent of index $i=\lfloor \frac{i}{2}\rfloor$
Children of $i=2i,2i+1$

## Heap Operations

Why do we care? Use to implement a priority queue: enqueu, dequeue only the highest priority elemtn

Since no gaps, store heaps in arrays.

## Add

1. Preserve Shape
2. Fix Parent/Child relationships
	1. Upheap/heapify/bubble-up. While new data has bad relationship with parent: swap parent and kid

Efficiency?

Average case $O(\log n)$ amortized
Worst case $O(\log n)$ amortized

Both the cases are amortized since heaps are stored in arrays.

## Remove

only allowed to remove root because it is the largest/smallest thing

1. Remove Root
2. Downhead/Heapify/bubble-down
	1. while new data has bad relationship with its kids, swap parent and kids


3 Scenarios
2 good kids -  No swap. Done

1 good, 1 bad: swap with bad children.

2 bad:
	for max heap: swap with larger child
	for min heap: swap with smaller child

Efficiency:

O(log(n)) for average and worst

How to find last leaf?

arr\[size\]

How do you know if you are at a leaf position in an array (for downheap?)

Children of i are 2i and 2i+1. SO if 2i>size we have no kids and are a leaf

How ot convert a list to a heap?
for i in range(0,size-1):
	hea.add(list\[i\])
This is O(n* logn)

We can use build heap which is O(n)

Build Heap - Convert a random array of data into a heap.

for each internal node in reverse level order:
	down heap that node

Runtime: how many internal nodes: (n/2)*downheap
O(n) * O(logn)
=O(n)

## Build Heap

Downheap every internal node from right to left bottom to top.
