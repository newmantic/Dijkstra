# Dijkstra


Dijkstra's algorithm is an efficient method for finding the shortest path from a single source node to all other nodes in a graph with non-negative edge weights. It is a greedy algorithm that explores nodes based on their current shortest known distance from the source, ensuring that each node is processed in order of increasing distance.


The graph is represented by a set of vertices V and a set of edges E.
Each edge (u, v) has a non-negative weight w(u, v) representing the cost to move from vertex u to vertex v.

Initialization:
Create a distance table dist[] where each entry dist[v] represents the shortest known distance from the source node s to vertex v.
Initialize dist[s] = 0 for the source node, and dist[v] = inf (infinity) for all other vertices v.
Use a priority queue (min-heap) to manage and explore vertices based on their current shortest distance.


Step 1:
Set the distance to the source node s as 0:
dist[s] = 0
Initialize all other distances to infinity:
dist[v] = inf  for all v in V, v != s

Step 2:
Insert the source node s into the priority queue with distance 0.

Step 3:
While the priority queue is not empty:
Extract the node u with the smallest distance from the priority queue.
For each neighbor v of u, calculate the tentative distance dist[u] + w(u, v):
new_dist = dist[u] + w(u, v)
If new_dist is less than dist[v], update dist[v]:
if new_dist < dist[v]:
    dist[v] = new_dist
Insert or update v in the priority queue with the updated distance dist[v].

Step 4:
Repeat until all vertices are processed or the priority queue is empty.

Final Output:
The dist[] array now contains the shortest path distances from the source node s to every other node in the graph.
