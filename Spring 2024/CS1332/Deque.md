
Linked Deque

For remove back these are O(n)
* SLL
* SLL with tail
* CSLL


Addfront, add back, remove front, and remove back is O(1)
* DLL

linked Deque is literally a doublely linked list.


Array Deque
* Use circular Array
	* Add front
	* add back - same as array queue
	* rem front - same as array queue
	* rem back

Add front:
```
front = front-1 mod array.len
arr[front] = data
size++
```



![[Pasted image 20240124145106.png]]

