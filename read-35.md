# Graphs

Graph - A non-linear data structure that can be looked at as a collection of vertices (nodes) potentially connected by line segments named edges.
- Vertex - A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.
- Edge - An edge is a connection between two nodes.
- Neighbor - The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.
- Degree - The degree of a vertex is the number of edges connected to that vertex.
- Cycle - A culmination of directions which cause the user to end up back at the starting node ('a -> b -> c -> a' or 'a a.next=> b b.next=> a' NOT 'a -> b -> c -> b -> a' or 'a a.next=> b b.previous=> a)

Undirected Graph - Edges can be traversed in either direction

Directed Graph (Digraph) - Edges can only be traversed from one node to another not in reverse. I'm assuming this is similar to the way a node may have a .next but doesn't have a .previous vs having both.

Complete Graph - Every node in the graph is connected to each and every other node.

Connected Graph - Each node has at least one connection, but may optionally have more.

Disconnected - At least one node in the graph does not have any connections to any other nodes.

Acyclic Graph - A directed graph without cycles.

Cyclic graph - A graph with at least one cycle.

Graphs can be represented by:

- Matrices - By adding a 1 to every connection in a given graph.
```
# Graph:
# A---B---C
# |   |   | 
# D---E---F

# Matrix
  A B C D E F
A 0 1 0 1 0 0
B 1 0 1 0 1 0
C 0 1 0 0 0 1
D 1 0 0 0 1 0
E 0 1 0 0 0 1
F 0 0 1 0 1 0
```

- Adjacency Lists - By adding every connected node to the linked list at an lists index representing the initial node.
```
# Graph:
# A---B---C
# |   |   | 
# D---E---F

# Adjacency List
[
    A -> B -> D,
    B -> A -> C -> E,
    C -> B -> F,
    D -> A -> E,
    E -> B -> D - > F,
    F -> C -> E,
]
# (those would be actual linked lists not just their print statements)
```

Weighted Graph - A graph with numbers assigned to each edge. In a matrix the 1s would be replaced with the number of the edge connecting the nodes. In a linked list the node.value would be atuple containing (the connection, and the edge).