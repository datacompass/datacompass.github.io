---
layout: post
use_math: true
title: Graphs and Trees
---

Many methods of data analysis "branch out" (choose one possibility over another) and link pairs of objects based on similarity in some features (e.g., pairs of cities with a direct flight connection).  The concept of a **graph** was invented to keep track of these processes and information structures.  This concept is convenient for both analysis and programming.

##  Graphs

A **graph** is defined as two lists: 
1) a list of objects--called **nodes** or **vertices**--and 
2) a list of pairs of nodes--these pairs are called **edges** or **arcs** or **links**.  

So, we can specify a graph by writing down these two lists--for example, nodes: *A*, *B*, *C*, *D*, *E*, *F*, *G*, links: \{*A*, *C*}, {*A*, *D*}, {*E*, *G*}--but sometimes it is helpful to sketch the graph:

![linear fit]({{ site.url }}/images/graph-example-1.jpg){:height="300px" width = "400px"}

Another way to list the same links is: {*C*, *A*}, {*A*, *D*}, {*G*, *E*}.  Can you find another?

A pair of nodes paired up by a link is said to be "linked".

###  Walks, paths, and connectivity

Sometimes the links model transporting of objects or transmission of signals from node to node, and the transportation/transmission is possible only if the two nodes are linked.

If an object is transported through two or more nodes, then the nodes it traverses can be written down, in that order.  A sequence of nodes in graph with every consecutive pair linked is called a **walk** (in that graph).  A walk can have repeated nodes: after all, some itineraries go through the same location more than once.

A graph is **connected** if every two nodes are connected by a walk.  

(A list of cities is connected if one can get from any city to any other in the list without visiting any city off the list.  The "getting" from one city to another does not have to be direct: we can go through other, intermediate, cities, as long as they are on our list.)

The graph illustrated above is not connected, but the following one is:

![linear fit]({{ site.url }}/images/connected-graph-example.jpg){:height="300px" width = "400px"}


###  Two special types of paths

**Paths:**  A walk with each node appearing exactly once is called a **path**.

**Cycles:**  A walk with the first and last node being the same one is called a **cycle**.

One exercise in algorithms is to write a program that determines whether a given graph contains a cycle.

###  Trees

A connected graph with no cycles is called a **tree**.  If one of the nodes in a tree is chosen and marked as "root" (it becomes clearer what actually to do with roots once one uses a tree in an algrithm), the resulting tree is a **rooted tree**.


## Directed graphs

Sometimes graphs are needed to model links that can be traversed in one direction, but not in the other (like one-way streets).  Such links are specified a little differently from the above; namely, one now writes a links as an *ordered* pair of nodes.

A graph where the links are ordered pairs of nodes is called a **directed graph**.
