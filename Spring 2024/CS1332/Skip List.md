
## Complexities
![[Pasted image 20240304202808.png]]


If goal is to run binary serach on a link list, just add all the links: to the middle, to one quarter, to three quarters and so on.

The solution is to use a "stacked" linked list

```
Node<T> {
	T Data
	Node next
	Node prev
	Node up
	Node down
}
```

![[Pasted image 20240219143215.png]]



Rules
1. All data must be in bottom layer
2. no floating nodes: if on level i, must be on i-1,i-2,...
![[Pasted image 20240219143505.png]]


How to add to a skip list?

Calculate the number of levels of a node:

Option 1: recalculate the height of every node in the list. O(n)

Option 2: use randomness.
1. Step 1: flip a fair coin until we get tails
2. Step 2: for each heads, "promote" one level.


When you add to a skipList, if the data is already there, still flip coins. If larger than previous height, update.

Best Case Time Complexity
$O(\log n)$
Worst Case Time Complexity
$O(n)$


Average Case Memory Usage
$O(n)$
Worst Case  Memory Usage
$O(n\log n)$


Important difference between Skip List and Binary Search Tree

In a bst, the worst case depends on the data
In a skip list, worst case is user independent, depends on coin