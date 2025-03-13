Title:Graph and operations
Project Description:
This project provides an implementation of a graph using an adjacency matrix in C. It includes various operations such as creating a graph, updating edges, searching for edges, deleting edges, and performing traversal algorithms like BFS and DFS. Additionally, the program can detect cycles in the graph.

Features:
✅ Graph Representation: Uses an adjacency matrix for storing edges.
✅ Graph Operations:

Create a graph with user input
Print the adjacency matrix
Search for an edge between two vertices
Update the weight of an edge
Delete an edge between two vertices
Delete a vertex and its associated edges
✅ Graph Traversals:
Breadth-First Search (BFS)
Depth-First Search (DFS)
✅ Cycle Detection: Checks if the graph contains a cycle.

Installation Instructions
Follow these steps to install and run the Graph Operations program in C:

1. Prerequisites
Ensure you have the following installed on your system:
✅ GCC Compiler (for compiling C programs)
✅ A Terminal or Command Prompt (for running commands)
/*
 * Graph Implementation in C with various operations
 * Features:
 * 1. Create a graph (Adjacency Matrix representation)
 * 2. Print adjacency matrix
 * 3. Search for an edge
 * 4. Update an edge
 * 5. Delete an edge
 * 6. Delete a vertex
 * 7. Perform BFS (Breadth-First Search)
 * 8. Perform DFS (Depth-First Search)
 * 9. Check if the graph is cyclic
 */

Usage Examples
Once the program is compiled and running, you will see a menu with various options. Below are some example interactions to help you understand how to use the program.

1. Creating a Graph:
2. input:
Enter number of vertices: 4  
Enter number of edges: 4  
Enter edge 1 (u v weight): 0 1 5  
Enter edge 2 (u v weight): 1 2 3  
Enter edge 3 (u v weight): 2 3 7  
Enter edge 4 (u v weight): 3 0 2  
Graph Representation:
Adjacency List:
Vertex 0 -> [1 (5), 3 (2)]
Vertex 1 -> [0 (5), 2 (3)]
Vertex 2 -> [1 (3), 3 (7)]
Vertex 3 -> [2 (7), 0 (2)]
Searching for an Edge:
input:
Enter two vertices to search for an edge (u, v): 1 2  
Output:
Edge exists between 1 and 2 with weight 3
Updating an Edge:
input:
Enter two vertices to update edge (u, v) and weight: 1 2 6  
output:
Edge updated between 1 and 2 with new weight 6  
Deleting an Edge:
input:
Enter two vertices to delete edge (u, v): 3 0  
output:
Edge deleted between 3 and 0  
Performing Breadth-First Search (BFS):
input:
Enter starting vertex for BFS: 0  
output:
BFS starting from vertex 0: 0 1 3 2
Performing Depth-First Search (DFS):
input:
Enter starting vertex for DFS: 0
output:  
DFS starting from vertex 0: 0 1 2 3  

