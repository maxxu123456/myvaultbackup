They have an average time complexity of $O(\log n )$


Use a heap to store data. Repeatedly remove the largest thing to sort data.

## Heap Sort
1. Add data to a heap $O(n)$
2. Remove each item one at a time $O(n\log n)$
So the total result is $O(n\log n)$

Time complexity:
Best, Average, and Worst: $O(n\log n)$


Is it adaptive? No
Is it stable? No
It is in-place? No


How to know if an algorithm is stable?
- If swaps are only made between adjacent elements, then the sort is probably stable.
- If you regularly make "large" swaps, i.e. swaps between non-adjacent elements, then the sort is probably not stable.

In the case of HeapSort, you are swapping data throughout the tree, so probably not stable.


## Divide and Conquer Algorithms
- break problem into subproblems, solve the subproblems, then combine solutions into a solution for original problem

## Merge Sort

Break list into two halves, sort each half. Now you have two sorted sublists. Combine them into a single sorted list.

```
mergesort(arr):
	if len(arr) == 1
		return arr
	else
		left = left half
		right = right half
		mergesort(left)
		mergesort(right)
		merge(left,right)
```


When merging two sorted arrays, 
continually take the smaller element of the two arrays, and add that to the new array. Once one half is empty, the remaining elements of the other half can be directly copied over.

Note: For stability, when comparing equal values, take the one from the left half.

What is Big O of merging? O(n) to merge two half arrays of size n/2

Adaptive? NO
Stable? YES
In-Place? NO

