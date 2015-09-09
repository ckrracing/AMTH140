# Week 8 Lecture 2

### Chapter 10 Graphs and Trees

Graphs: Definitions

#### Trails, Paths and Circuits

##### 7 Bridges Problem (euler)
Is it possible for a person to take a wlak around town , starting and ending at the same location and crossing each of the 7 brdiges exactly once.

Euler translated this proble into a graph theory. In terms of the graph , the question becomes the following.

> Is it possible to trace this graph , starting and ending at the same point , without ever lifting your pencil from the paper? Or more formally is it possible to find a route through the graph that starts and ends at some vertex, one of A,B,C,D and traverse each edge exactly once.

Vertices(Plural) vertex (Singular),**edges** connect vertices.

> Graphs have pictorial representations in which the vertices are represented by dots and the edges by the line segments. A give pictorial representation uniquely determines a graph.

###### Formal Definition of a Graph
* Parallell Edges
  * Two vertexes connected by two edges
* Loop
  * Connects a vertex to itslef
* Edge Endpoint function


// note look up incident


##### Main thing is need set of Edges , set of vertices and an Edge Endpoint Function

##### Example
1. Write the vertex set , edge set and give a table showing the edge Endpoint function

{ v1, v2 , v3 } //set of vertices
{ e1,e2,e3 ,e4 } //set of edges

Edge endpoint function ( done as a table )

Edge e1 , Endpoints {v1,v2}
Edge e2 , Endpoints { v1 , v3 } // parallell
Edge e3 , Endpoints { v1, v3 } //parallell
Edge e6 , Endpoint { v6 } //loop
...

##### Directed Graphs

Endpoints are an ordered pair , ie the graph goes in a certain direction.
so { v1 , v3 } e1 so edge goes from v1 to v3 , draw edges with arrow heads to show directed graph.

### Examples of Graphs.

Using a Graph to represent networks such as internet , plane routes .
Questions arise in the design of such systems which involve choosing connecting edges to minimize cost , or optimize paths in order to optimise services through the network.

**Simple Graphs**
* No loops
* No parallel edges
* Specifiying two endpoints is sufficient to determine an edge

**Complete Graph**
* All pairs of vertices connected by edges  denoted Ksub n
* its simple graph with n vertices and exactly one edge per pair
* Every vertices is connected to all vertices .


**SubGraph**
* Where one graph is a sub graph of another graph eg H sub G
* Iff ever vertex in graph H is also a vertex in G
* Iff every edge in H is also edge in G
* Every edge in H has the same endpoints as G

### The concept of degree. deg(v)
* number of edges eminating from / to a vertex -*-
* total degree of G = sum of edges on vertexex in graph
* Loops are counted twice

total degree of G = deg(v1) + deg(v) ...

##### Handshake Theorem

total degree of G = 2 X edges
total degree of a graph is even

##### Trails , Paths and Circuits

##### Travel in a graph (defn)
> Accomplished by moving from one vertex to another along a sequence of adjacent edges.
defined by writing v1,e1,v2,e2,v3,e3 (Walk on the Graph)

> Certain types of sequences (Walks) of adjacent vertices and edges are of special importance in graph theory. Those that do not have a repeared edge , those that do not have a repeated vertex , and those that start and end at the same vertex.

* Those that do not have a repeated edge ( do not travel same edge twice )
* those that do not have a repeated vertex ( do not pass over the same vertex twice )
* those start and end at the same vertex

> Let G be a graph and let v and w be vertices in G .
> A Walk from v to w is a finite alternating seq of *adjacent* v and e's ie cant leap to a vertex without going over e's
* Trail from v to w , walk with no repeated edge
* Path from v to w , no repeated v
* closed walk is walk starts and ends at the same vertex
* circuit closed walk that contains at least one e and does not contain a reated e
* Simple circuit, does not have any other repeated vertex except the first and last .