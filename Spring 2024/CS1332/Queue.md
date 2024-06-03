
First In, First Out

Add to Back, Remove from Front

Add = enqueue
Remove = dequeue

Examples
* Office Hour queue
* Vending Machine Items
* Waiting List

Two Implementations

Array Queue 

Last alement in ciruclar Array QUeue = 
(fonr+size-1)% length

Linked Queue

Enqueue = Add to back of linked list
Dequeue: Remove from the front of the linked list

Array Queue
We cant use an arraylist since at least remove from front or add to front will be O(n)

The Solution is a CircularArray since it doesnt shift data arround when adding or removing from front

CircularArrayADT:
* ordered, contiguous, not need 0 aligned
* The next index after size-1 is 0

If there is no more space to enqueue data, resize the array so the the front pointer data is at index 0.