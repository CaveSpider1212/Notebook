---
tags: CMSC_132
created: 2025-11-17
description: 11/14, 11/17 notes (Lectures 31 and 32)
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