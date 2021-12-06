---
description: Single Source Shortest Paths
---

# Dijkstra And Bellman Ford

{% hint style="info" %}
**Initialize Single Source** is the initial step that preprocess the graph.

**Relaxation** is a technique that being used in below algorithms algorithms.
{% endhint %}

![Initialization Single Source](<../.gitbook/assets/image (3).png>)

![Relax](<../.gitbook/assets/image (4).png>)

{% hint style="info" %}
One way to find single source shortest path is to use topological sort to sort the vertices and then initialize the single source.
{% endhint %}

![Single Source Shortest Paths in Directed Acyclic graphs](<../.gitbook/assets/image (7).png>)

## Dijkstra's Algorithm

We can break down this algorithm into 3 steps:

1. Build the graph with the sources(u, v, w)
2. Create a _**Priority Queue Q**_ based on the weight w and create a _**Set**_  **S** to find the lightest given vertex
3. insert the start source into the queue and loop over all sources. Update the Set of vertices and relax the current vertex u with all its adjacent vertex v.

![Dijkstra's Algorithm Template](<../.gitbook/assets/image (6).png>)

{% hint style="info" %}
The run time of Dijkstra Algorithm is **O((V + E) log V)** in general. The heap-extract-min takes time O(log V). For V such operations, the total time is O(V log V). To build the priority queue with decrease-key operations that takes time O(log V) for E edges, the time complexity is O(E log V).&#x20;

If the graph is sufficiently sparse, E = O( V^2 / log V).
{% endhint %}

{% content-ref url="../depth-first-search-dfs/787.-cheapest-flights-within-k-stops.md" %}
[787.-cheapest-flights-within-k-stops.md](../depth-first-search-dfs/787.-cheapest-flights-within-k-stops.md)
{% endcontent-ref %}

{% content-ref url="../depth-first-search-dfs/1631.-path-with-minimum-effort.md" %}
[1631.-path-with-minimum-effort.md](../depth-first-search-dfs/1631.-path-with-minimum-effort.md)
{% endcontent-ref %}



## Bellman-Ford Algorithm

![Bellman Ford Algorithm Template](<../.gitbook/assets/image (5).png>)
