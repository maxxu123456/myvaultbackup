A graph is a set of vertices and a set of edges.

G = (V,E)

An edge connects two vertices, called its endpoints.

Two graphs are equal if they have the same vertices and the same edges

A simple graph has no self loops, and only one edge connecting any pair of vertices

Two vertices are adjacent if they are connected by an edge?

An edge is incident to a vertex if that vertex is one of its endpoints.

Degree of a vertex is the number of edges incident to that vertex

![[Pasted image 20240405143405.png]]

![[Pasted image 20240405144555.png]]

## Graph Traversals

Option 1: At each step, travel along a random edge. If get to a new vertex, add it to list.

Issue: Inefficient, lots of repeats, don't know when to stop

Option 2: Whenever move to a vertex, makr it as "visited". Never go to a repeated vertex.

Issue: You can get stuck

Option 3: When visit a vertex, remember all of the neighbors in a sort of a TODO List.


When should you explore brand new vertices that you've just seen? Before or after the other vertices you already know about?

## Depth First Search

- Always explore the NEWEST thing that you've just seen.
- Go back to old things when you run out of new things
```
DFS(G,S):
	mark s as visited
	for w adjacent to s:
		if w is not visited:
			DFS(G,w)
```


## Breadth First Search
- Explore the Oldest thing first, do the newest things last.
- Consequence:
	- Explore the adjacent vertices first
	- then the vertices that are two away
	- then the vertices that are three steps away


![[Pasted image 20240412141806.png]]


![[Pasted image 20240412141810.png]]



