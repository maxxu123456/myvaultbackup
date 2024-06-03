
Adding to front and back is O(1)

Removing from front is O(1)

Removing from back is O(n)

Add front:
front = (front-1)%arr.len
arr\[front\] = data
size++

