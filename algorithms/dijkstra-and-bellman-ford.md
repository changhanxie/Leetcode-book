---
description: Single Source Shortest Paths
---

# Dijkstra And Bellman Ford

{% hint style="info" %}
**Initialize Single Source** is the initial step that preprocess the graph.

**Relaxation** is a technique that being used in below algorithms algorithms.
{% endhint %}

![Initialization Single Source](../.gitbook/assets/image%20%283%29.png)

![Relax](../.gitbook/assets/image%20%284%29.png)

{% hint style="info" %}
One way to find single source shortest path is to use topological sort to sort the vertices and then initialize the single source.
{% endhint %}

![Single Source Shortest Paths in Directed Acyclic graphs](../.gitbook/assets/image%20%287%29.png)

## Dijkstra's Algorithm

We can break down this algorithm into 3 steps:

1. Build the graph with the sources\(v, u, w\)
2. Create a _**Priority Queue**_ based on the weight w and create a _**Set**_ to find the lightest given vertex
3. insert the start source into the queue and loop over it. Update the Set of constrains and relax the current vertex u with all its adjacent vertex v.

![Dijkstra&apos;s Algorithm Template](../.gitbook/assets/image%20%286%29.png)

{% hint style="info" %}
The run time of Dijkstra Algorithm is **O\(\(V + E\) log V\)** in general. The heap-extract-min takes time O\(log V\). For V such operations, the total time is O\(V log V\). To build the priority queue with decrease-key operations that takes time O\(log V\) for E edges, the time complexity is O\(E log V\). 

If the graph is sufficiently sparse, E = O\( V^2 / log V\).
{% endhint %}

{% page-ref page="dijkstra-and-bellman-ford.md" %}

## Bellman-Ford Algorithm

![Bellman Ford Algorithm Template](../.gitbook/assets/image%20%285%29.png)

