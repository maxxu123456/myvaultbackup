- Only one data item allowed per index. How to handle collisions? If index you want is full, try the right neighbor. If that is full, try its right neighbor and so on. Add to the first empty index you find.

Pseudocode Version 1:
```
put(key,value):
	index = abs(key.hash())%arr.length
	while arr[index] != null and arr[index].key != key:
		index = index+1 % arr.length
	if arr[index] == null:
		add key value pair
	else if arr[index].key = key:
		update value
```

If data has been removed form hashmap, then you must serach every possible spot to get the key value pair, since the kv pair could be anywhere


Must replace removed data with something (DEL marker)

![[Pasted image 20240216142653.png]]

![[Pasted image 20240216142901.png]]


Example:
![[Pasted image 20240216143803.png]]
![[Pasted image 20240216143813.png]]


## Pros and Cons

![[Pasted image 20240216143949.png]]

## How to deal with runs?

Idea: leave gaps between collided items rather than storing everything next to each other.

Quadratic Probing

| linear probing | quadratic probing |
| ---- | ---- |
| i | i |
| i+1 | i+1 |
| i+2 | i+4 |
| i+3 | i+9 |
| i+4 | i+16 |

