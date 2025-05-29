
# EX.NO : 11(A)  PRIM'S MINIMUM SPANNING TREE 
 
# PROGRAM STATEMENT: 
 
Given a weighted, undirected and connected graph of V vertices and E edges. The task is to find the sum of weights of the edges of the Minimum Spanning Tree.


![image](https://github.com/user-attachments/assets/fa595923-0b2e-45eb-97d1-18b71ac3f0e7)

 
# ALGORITHM:   
 
1. Start the program. 
2. Initialize a priority queue to store edges, each represented by (weight, vertex). 
3. Choose an arbitrary starting vertex and mark it as visited. 
4. Add all edges connected to the starting vertex into the priority queue. 
5. While the priority queue is not empty, pop the edge with the minimum weight and if the destination vertex is not in the MST, add it and update the priority queue with edges from the newly visited vertex. 
6. End the program by calculating the sum of the edge weights in the MST. 
 
# PROGRAM: 
```
void Graph::addEdge(int u, int v, int w)
{
	adj[u].push_back(make_pair(v, w));
	adj[v].push_back(make_pair(u, w));
}
```

# output:

![image](https://github.com/user-attachments/assets/da5e6819-9ac2-43d6-8f8b-b317fb81d600)

# RESULT: 
 
Thus, the C++ program to find the sum of weights of the edges of the Minimum Spanning Tree is created successfully. 


