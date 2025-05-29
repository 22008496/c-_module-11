
# EX.NO : 11(C)  SHORTEST PATH - DIJKSTRA'S ALGORITHM 
 
# PROGRAM STATEMENT: 
 
There is a directed weighted connected graph. You are given a positive integer n which denotes that the graph has n nodes labeled from 1 to n, and an array edges where each edges[i] = [ui, vi, weighti] 
denotes that there is an edge between nodes ui and vi with weight equal to weighti. 
 
Correct the given C++ function to find the dijkstra'a shortest path from every node to all other nodes in the given graph. 
 
# ALGORITHM:   
 
1. Start the program. 
2. Initialize the distance for the source vertex to 0 and all other vertices to infinity. 
3. Insert the source vertex into a set with its distance as the key. 
4. While the set is not empty: 
a. Extract the vertex with the minimum distance from the set. 
b. For each neighboring vertex, check if the current path offers a shorter distance than previously known. If so, update the distance and insert it back into the set. 
5. After processing all vertices, print the shortest distance from the source to each vertex. 
6. End the program.

# Program:
```
// Driver program to test methods of graph class
int main()
{
	int n, m;
	 cin >> n >> m;

	 Graph g(n);
	for (int i = 0; i < m; i++)
	{
		 int x, y, w;
		 cin >> x >> y >> w;
		 g.addEdge(x, y, w);
	 }
	g.shortestPath(0);
	return 0;
}

```

# output:

![image](https://github.com/user-attachments/assets/faea5a38-b8b9-48d2-9fee-513836619119)

# RESULT: 
 
Thus, the C++ program to find the dijkstra'a shortest path from every node to all other nodes in the given graph is created successfully.
