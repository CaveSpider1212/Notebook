---
tags: CMSC_132
created: 2025-11-17
description: 11/14, 11/17, 11/19 notes (Lectures 31, 32, 33)
---

A **graph** consists of a set of **vertices** (or nodes) with a set of **edges** that connect them.

A graph has a many-to-many relationship between elements (meaning each element may have multiple predecessors or multiple successors).

### Definitions

A **vertex** is just a node in the graph.

An **edge** is what connects two vertices.

An **undirected graph** is where the edges don't necessarily point from one vertex to another, while a **directed graph** is where edges point from one vertex to another.

The **neighbors** of a vertex are all the vertices you can reach from that vertex by following a single edge.

A **path** is a sequence of vertices in a graph such that the graph has an edge between each pair of vertices in the sequence.

A **cycle** is a path that ends back where it started (at the initial vertex).

An **acyclic graph** is one that doesn't have any cycles.

A **connected** undirected graph is one that has a path from every vertex to every other vertex, while an **unconnected** graph does not have this property.

In a **strongly connected** directed graph, for every pair of vertices `u` and `v` there is a path from both `u` to `v` and `v` to `u`.

A **weighted** graph is one where the edges have numeric "weights".

### Operations

- Structural
	- Adding or removing vertices or edges
	- Changing edge weights (for a weighted graph)
- Informational
	- Looking up (checking for) vertices or edges, or (for a weighted graph) getting the weight of an edge
	- Traversing (visiting each vertex in a graph)
		- Some type of processing is typically performed at each vertex
		- Could do a breadth-first search (BFS) or depth-first search (DFS)

### Representation

- Edges can be represented in different ways:
	- An **adjacency matrix** is a two-dimensional array of neighbors of vertices (the matrix rows and columns correspond to vertices)
	- In an **adjacency list**, **adjacency set**, or **adjacency map**, each vertex stores (respectively) a list, set, or map of its neighbors

##### Adjacency matrix

If there's an edge between vertices $v_i$ and $v_j$, its data is stored in element `[i][j]` of the array.

For an unweighted graph, the array elements can just be booleans. For a weighted graph, they would be the edge weights.

A directed graph's adjacency matrix is a $k \times k$ matrix, where $k$ is the number of vertices, while an undirected graph's adjacency matrix is a staircase.

The rows and columns are labeled with the vertices of the graph. In a directed graph, if there is a value in a row, then there is an edge going out of the corresponding vertex. If there is a value in a column, then there is an edge going into the corresponding vertex.

##### Adjacency list, set, or map

For each vertex, store either a list, set, or map of its neighbors (i.e. successors). In addition, for a weighted graph, also store the weight of each edge.

For a weighted graph, use an adjacency map over an adjacency set. For an unweighted graph, an adjacency set is fine.

For an undirected graph with edge ($a \leftrightarrow b$), vertices $a$ and $b$ need to store each other as neighbors. For a directed graph with edge ($a \rightarrow b$), vertex $a$ needs to store vertex $b$ as a neighbor.

### Graph Traversal

Breadth-first search visits all vertices at distance (number of edges) $k$ from the starting point before visiting any vertices at (minimum) distance $k + 1$ from the starting point.

Depth-first search visits vertices as far ahead as possible in one direction before backing up, then backs up the minimum distance possible.

Issues to be addressed:
- Avoid revisiting vertices
- Avoid an infinite loop if the graph contains cycles

Two approaches to address the above issues:
- Maintain a set of the vertices that have been visited or processed
	- Initialize `visited` to be an empty set
	- Add each vertex to `visited` as it's processed
	- When traversing, skip vertices that are already in `visited`
- Mark the vertices as they're visited
	- Initialize the tag on all vertices to false
	- Set the tag on a vertex to true as it's processed
	- When traversing, skip vertices with tag = true

For a breadth-first search, add a vertex into a *queue*, remove the first element from the queue, then process it (how it's processed depends on whether we are using a set or tags), and then add all of its neighbors to the queue and repeat.

For an iterative depth-first search, do the same thing but with a *stack* instead.

For a recursive depth-first search, call the recursive method for each neighbor of a vertex. A good way to approach this is to add the vertex to the processed set (or set its tag to "true"), then go to the next neighbor, and keep going until it has no unprocessed/untagged neighbors, then go back starting from the end of the processed vertices until we reach a vertex that does have an unprocessed/untagged neighbor, and keep going from there until all vertices have been processed/tagged.

### Shortest path in a graph

**Dijkstra's algorithm** finds the paths with the lowest sum of edge weights from a starting from a starting vertex $X$ to *all* the other vertices in a graph.

It uses several data structures:
- A set of vertices `processed` with known shortest paths from the starting vertex (the vertices that have been processed so far)
- An array of costs `D` storing the cost of the shortest path from the starting vertex to each vertex `V` currently in `processed`, in `D[V]`
- An array `predecessors` storing the predecessor on the shortest path from the starting vertex to each vertex `V` in `processed`, in `predecessors[V]`
	- This is updated whenever a new (lower) cost path is discovered
	- It remembers the actual path with lowest cost

Algorithm:
- Have an empty set `processed`, plus an empty array `predecessors` and array `D` to begin with
- While there are some vertices in the graph that are not in `processed`, find the vertex `u` that isn't in `processed` that has the smallest value of `D[u]`, then add `u` to `processed`
- For each neighbor `n` of `u` that is not in `processed`, if `D[n]` is greater than `D[u]` plus the cost to get from `u` to `n`, then set `D[n]` to `D[u]` plus the cost of the edge from `u` to `n`, then set the predecessor of `n` to `u`

### Factors affecting graph algorithm efficiency

- The efficiency of graph algorithms can depend on what graph representation is used, or what graphs it is run on (what the graphs look like)
- Graphs are more complex than other data structures because they have two components: vertices and edges
- A graph could be large or small
- A graph could have many edges relative to the number of vertices (*dense*) or have few edges relative to the number of vertices (*sparse*), meaning we need to consider the number of vertices and edges separately
- `n` will be used to represent the number of vertices, while `m` will be used to represent the number of edges

### Graph Representations - Memory Usage

> Graph type|Adjacency matrix|Adjacency list|Adjacency set or map
> -|-|-|-|
> Undirected|$\frac{1}{2}(n^2 + n) = O(n^2)$|$2 \times m = O(m)$|$2 \times m = O(m)$
> Directed|$n^2 = O(n^2)$|$m = O(m)$|$m = O(m)$

If there are a lot more vertices compared to edges, then an adjacency matrix is a bad choice since there is a lot of unused space. An adjacency list/set/map is a better choice for memory.

### Graph Operations - Running Time

Assuming edges can be found in adjacency matrices quickly, lists are in increasing order by vertex name, hashing is used for sets/maps, and the edges of graphs are distributed as evenly as possible throughout graphs, then the average complexity of operations for a directed graph with `n` vertices and `m` edges is:

> Operation|Adjacency matrix|Adjacency list|Adjacency set or map
> -|-|-|-|
> Inserting an edge|$O(1)$|$O(\frac{m}{n})$|$O(1)$
> Deleting an edge|$O(1)$|$O(\frac{m}{n})$|$O(1)$
> Finding an edge|$O(1)$|$O(\frac{m}{n})$|$O(1)$
> Iterating through the neighbors of a vertex|$O(n)$|$O(\frac{m}{n})$|$O(\frac{m}{n})$

### Types of Graph Algorithms

Algorithms can be neighbor-based (meaning iterating through the vertices, then iterating through the neighbors for each vertex and doing something with the neighbor) or connection-based (iterating through the vertices, then for each vertex iterating through the vertices again and seeing if there is an edge between the inner loop vertex and outer loop vertex).

For neighbor-based algorithms, using an adjacency matrix is slower since we have to iterate through each element in a row to see the neighbors of a vertex, even if there is no edge between some of the vertices. Adjacency lists/sets/maps are faster since we only iterate through the vertices there are edges with.

For connection-based algorithms, using an adjacency matrix is faster since we can instantly look up in the array to see if two vertices have an edge.

### Efficiency of Graph Algorithms

DFS and BFS can be implemented so they're efficient
- For the iterative versions, each (reachable) vertex will be processed, and a loop iterates over the neighbors of each vertex being processed (this would be $O(n + m)$, or linear in the size of the graph)

The efficiency of Dijkstra's algorithm depends on what is used to store vertices
- If it's coded inefficiently, Dijkstra's algorithm would take $O(n^2)$
- If things are done efficiently, it can be coded to run in $O((n + m) \log(n))$
- Using a heap to store the vertices (where the smallest vertex can be removed each time) can make this algorithm efficient