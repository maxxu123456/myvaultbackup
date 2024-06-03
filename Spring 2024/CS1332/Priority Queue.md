It serves items based on priority.

It consists of two method

Enqueue()
Dequeue() -> Removes highest priority item

# Applications
- Organ Donor List
- Airplane boarding
- Amusement Parks with VIP Pass

# Implementation

Methodology 1: Store sorted data
Enqueue(): O(n) since you have to shift items even with binary search.
Dequeue(): O(1) highest priority data is simply at the end.

Methodology 2: Stored unsorted Data
Enqueue(): O(1)
Dequeue(): O(n)


Best Methodology: Use a Heap
Enqueue: O(logn)
Dequeue: O(logn)

