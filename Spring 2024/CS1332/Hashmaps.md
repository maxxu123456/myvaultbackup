Motivating Case

At GT Parking, we need to know who to let into each parking deck
Given an id, we need to retrieve that user information.

We want to store \<ID, UserInfo\> pairs like (2234,Bob)

2 actions:
1. Add new id-user pairs (put)
2. given an id, get the user's information (get)

We could store pairs in a linked list or a sorted array list or a binary search tree, but these are inefficient

Hash-map ADIt
- Collection of key-value pairs
- Keys are unique and immutable, values are not necessarily unique.

How to access data in O(1) time?
- Use Array
- Array has O(1) access if you know the index

A naive idea would be where the index and id are the same
- Store each key at the index matching the value of the key. So (371,Lucian) goes in index 371, etc.

There are two problems
1. The only type of key allowed is positive integers
2. Too much memory required

Fix Problem 1: Keys need to be positive integers
- Get Hash code of object
- Note: hashcode() default is BAD. You must make your own good hashcode function()
- A good hascode funtion has some properties
	- MANDATORY: two objects that are .equals() must have the same hascode
	- Preferred: different objects have different hashcodes

Fix Problem 2: Huge Amount of Memory
key.hashcode is 888888
Where do I put it if my array is not that large? Mod by length of the array.

Index = abs(key.hashcode() % arr.length)




Collisions are when two keys try to go to the same spot. This is bad! The more collisions you have, the slower you run.

How do you avoid collsions

Collision avoidance technique  #1, careful size of backing array. For hashmaps, filling the entire backing array is bad. The more ful the backing array is, the higher probaibly of a collision. Resize while still space in array.

load Factor of an array = size/capacity

Set a maximum allowed threshold.

Most common are between .6 and .8

Collision occurs when two items try to go to the same spot. Collision decrease speed.

Resize the array. Use load factor to decide resize.

Reclaculate where you put everythign.

Prime length arrays lead to fewer collisions.

Resize to 2\*oldLength+1. Its not prime, but at least its not even.

How do we deal with collisions?

Closed Addressing: All collided things get to be at the same index.

- use external chaining

Open Addressing: Only one thing allowed per spot. New things that collide must go somewhere else.
- linear probing
- quadratic probing
- modulus, double hashing

## External Chaining

at each index, there is a linked-list that stores all of the key-value pairs associated with that index
Our backing array is therefore an array of linked lists

![[Pasted image 20240214142625.png]]
![[Pasted image 20240214143148.png]]

