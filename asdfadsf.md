
# Sorting Searching


### Resversort

Algorithm:
```sh
Reversort(L):
  for i := 1 to length(L) - 1
    j := position with the minimum value in L between i and length(L), inclusive
    Reverse(L[i..j])

```


Code:
```cpp
int reversort(vector<int>& v) {
    int cost = 0;  
    
    for(int i=0; i<v.size()-1; ++i){
        int m = *min_element(v.begin() + i, v.end());
        auto p = find(v.begin(), v.end(), m);
        reverse(v.begin() + i,  p);
        cost += distance(v.begin(), p) - i + 1;
    }
    return cost;

}
```


### Engineering Reversort





### Number Game




https://onlinecourses.nptel.ac.in/noc22_cs59/preview






# Greedy Algorithms

https://www.youtube.com/watch?v=cklYqfIRDao&list=PLyqSpQzTE6M9p9pKxFGpskf4voY45T2DZ&index=11


## Pancake Flipping




## Islands War



## Stable Marriage




















# Graphs Trees




## Disjoint Set Union









---


<h1 align="center">Assignments</h1>

## Graph


1. Dijkstra Algorithm

- Given a graph where all edges have positive weights, the shortest path produced by Dijkstra's and Bellman Ford algorithm may be different but path weight would be same.
- The shortest path between two vertices and in a graph always remains unaltered when all the edges of are multiplied by a positive integer.


2. BFS

- If all edges have the same weight in an undirected graph, **BFS** algorithm will find the shortest path between two nodes more efficiently.
- 


3. Floyd Warshall Algorithm

- It can detect negative weight cycles in the graph
- It works correctly if the graph has negative edge weights but does not have negative weight cycles
- The time complexity of Floyd-Warshall is O(V^3), where V is the number of vertices in the graph.


4. Spanning tree of connected graph

- A spanning tree is a connected acyclic graph
- In a spanning tree, every pair of nodes is connected by a unique path



5. Maximum flow
- Ford-Fulkerson algorithm uses the idea of BFS
- T.C. of Ford-Fulkerson = O(maxflow * |E|)
- T.C. of finding an augmented path = O(|E|)
- The minimum cut = the maximum flow





## DP

1. LIS
- TC = O(N^2)


Dice Combination:
```cpp
#include <iostream>
#include <vector>
#include <algorithm>

int minCostFrog(std::vector<int>& heights) {
    int n = heights.size();
    std::vector<int> dp(n, 0);
    dp[1] = abs(heights[1] - heights[0]);

    for (int i = 2; i < n; ++i) {
        dp[i] = std::min(dp[i-1] + abs(heights[i] - heights[i-1]), dp[i-2] + abs(heights[i] - heights[i-2]));
    }

    return dp[n-1];
}

int main() {
    std::vector<int> heights = {10, 15, 14, 19, 20, 16, 19, 27, 15, 16, 10, 23};
    std::cout << minCostFrog(heights) << std::endl;
    return 0;
}

```



Grid unique path:
```cpp
#include <iostream>
#include <vector>

int uniquePaths(int rows, int cols) {
    std::vector<std::vector<int>> dp(rows, std::vector<int>(cols, 0));

    // Initialize the first row and first column to 1
    for (int i = 0; i < rows; ++i) {
        dp[i][0] = 1;
    }
    for (int j = 0; j < cols; ++j) {
        dp[0][j] = 1;
    }

    // Calculate the number of paths for each cell
    for (int i = 1; i < rows; ++i) {
        for (int j = 1; j < cols; ++j) {
            dp[i][j] = dp[i-1][j] + dp[i][j-1];
        }
    }

    return dp[rows-1][cols-1];
}

int main() {
    int rows = 6, cols = 11;
    std::cout << uniquePaths(rows, cols) << std::endl;
    return 0;
}

```


Grid unique path with block:
```cpp
#include <iostream>
#include <vector>

int uniquePaths(int rows, int cols) {
    // Initialize the grid with zeros
    std::vector<std::vector<int>> grid(rows, std::vector<int>(cols, 0));

    // Mark the blockage at (3, 2)
    grid[3][2] = -1;

    // Initialize the first row and first column to 1
    for (int i = 0; i < rows; ++i) {
        if (grid[i][0] != -1) {
            grid[i][0] = 1;
        } else {
            break; // Stop initializing if there's a blockage
        }
    }
    for (int j = 0; j < cols; ++j) {
        if (grid[0][j] != -1) {
            grid[0][j] = 1;
        } else {
            break; // Stop initializing if there's a blockage
        }
    }

    // Calculate the number of paths for each cell
    for (int i = 1; i < rows; ++i) {
        for (int j = 1; j < cols; ++j) {
            if (grid[i][j] == -1) {
                continue; // Skip blocked cells
            }
            if (grid[i-1][j] != -1) {
                grid[i][j] += grid[i-1][j];
            }
            if (grid[i][j-1] != -1) {
                grid[i][j] += grid[i][j-1];
            }
        }
    }

    return grid[rows-1][cols-1];
}

int main() {
    int rows = 6, cols = 5; // 6 rows, 5 columns
    std::cout << uniquePaths(rows, cols) << std::endl;
    return 0;
}

```
