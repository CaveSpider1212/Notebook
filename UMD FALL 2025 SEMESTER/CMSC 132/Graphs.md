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

##### Adjacency list, set, or map

For each vertex, store either a list, set, or map of its neighbors (i.e. successors). In addition, for a weighted graph, also store the weight of each edge.

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

### Shortest path in a graph

**Dijkstra's algorithm** finds the paths with the lowest sum of edge weights from a starting from a starting vertex $X$ to *all* the other vertices in a graph.

It uses several data structures:
- A set of vertices `processed` with known shortest paths from the starting vertex (the vertices that have been processed so far)
- An array of costs `D` storing the cost of the shortest path from the starting vertex to each vertex `V` currently in `processed`, in `D[V]`
- An array `predecessors` storing the predecessor on the shortest path from the starting vertex to each vertex `V` in `processed`, in `predecessors[V]`
	- This is updated whenever a new (lower) cost path is discovered
	- It remembers the actual path with lowest cost