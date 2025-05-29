
# EX.NO : 11(D)  APPLICATION OF GRAPH 
 
# PROGRAM STATEMENT: 
 
A traveller needs to visit all cities from a list, where distances between all cities are known and visited once. What is the shortest possible routes that he visits each city exactly once and returns to 
the origin city?. Find the TSP solution using CPP function. 

![image](https://github.com/user-attachments/assets/80780670-4fe9-4ed4-9ff3-5b3e7ee001e3)

 
# ALGORITHM:   
 
1. Start the program. 
2. Initialize a list ver containing all vertices except the starting vertex p. 
3. Set m_p to infinity to store the minimum path weight. 
4. Generate all permutations of the vertices in ver: 
a. For each permutation, calculate the total path weight by traversing through the vertices in the order of the permutation. 
b. Add the weight to complete the cycle by returning to the starting vertex p. 
5. Update m_p with the minimum path weight found. 
6. After checking all permutations, return the minimum path weight.

# Program:
```
 int TSP(int p) // implement traveling Salesman Problem. 
    {
   vector<int> ver; //
   for(int i = 0; i <V; i++)
   {
      if(i!=p)
         ver.push_back(i);
   }
         int m_p = INT_MAX; // store minimum weight of a graph
   do {
      int cur_pth = 0;
      int k = p;
      for(int i=0;i<(int)ver.size();i++)
      {
         cur_pth += adjMatrix[k][ver[i]];
         k = ver[i];
      }
      cur_pth += adjMatrix[k][p];
      m_p = min(m_p, cur_pth); // to update the value of minimum weight
   }
   while (next_permutation(ver.begin(), ver.end()));
   return m_p;
}
```

# output:

![image](https://github.com/user-attachments/assets/1446f9e2-dce1-4489-a088-b696901e5cf6)

# RESULT: 
 
Thus, the C++ program to find the TSP solution using CPP function is created successfully.
