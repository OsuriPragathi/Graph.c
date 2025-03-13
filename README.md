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

#include <stdio.h>
#include <stdlib.h>
#include <stdbool.h>

#define MAX_VERTICES 10

// Function prototypes
void printAdjacencyMatrix(int graph[MAX_VERTICES][MAX_VERTICES], int vertices);
void searchEdge(int graph[MAX_VERTICES][MAX_VERTICES], int u, int v);
void updateEdge(int graph[MAX_VERTICES][MAX_VERTICES], int u, int v, int weight);
void deleteEdge(int graph[MAX_VERTICES][MAX_VERTICES], int u, int v);
void deleteNode(int graph[MAX_VERTICES][MAX_VERTICES], int* vertices, int vertex);
void takeInput(int* vertices, int graph[MAX_VERTICES][MAX_VERTICES]);
void bfs(int graph[MAX_VERTICES][MAX_VERTICES], int vertices, int start);
void dfs(int graph[MAX_VERTICES][MAX_VERTICES], int vertices, int start, bool visited[MAX_VERTICES]);
bool isCyclic(int graph[MAX_VERTICES][MAX_VERTICES], int vertices);

int main() {
    int graph[MAX_VERTICES][MAX_VERTICES] = {0};
    int vertices = 0, choice, u, v, weight;

    takeInput(&vertices, graph);

    while (1) {
        printf("\nMenu:\n");
        printf("1. Print adjacency matrix\n");
        printf("2. Search for an edge\n");
        printf("3. Update an edge\n");
        printf("4. Delete an edge\n");
        printf("5. Delete a node\n");
        printf("6. Perform BFS\n");
        printf("7. Perform DFS\n");
        printf("8. Check if graph is cyclic\n");
        printf("9. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                printAdjacencyMatrix(graph, vertices);
                break;
            case 2:
                printf("Enter two vertices to search for an edge (u, v): ");
                scanf("%d %d", &u, &v);
                searchEdge(graph, u, v);
                break;
            case 3:
                printf("Enter two vertices to update edge (u, v) and weight: ");
                scanf("%d %d %d", &u, &v, &weight);
                updateEdge(graph, u, v, weight);
                break;
            case 4:
                printf("Enter two vertices to delete edge (u, v): ");
                scanf("%d %d", &u, &v);
                deleteEdge(graph, u, v);
                break;
            case 5:
                printf("Enter vertex to delete: ");
                scanf("%d", &u);
                deleteNode(graph, &vertices, u);
                break;
            case 6:
                printf("Enter starting vertex for BFS: ");
                scanf("%d", &u);
                bfs(graph, vertices, u);
                break;
            case 7:
                printf("Enter starting vertex for DFS: ");
                scanf("%d", &u);
                bool visited[MAX_VERTICES] = {false};
                dfs(graph, vertices, u, visited);
                printf("\n");
                break;
            case 8:
                printf(isCyclic(graph, vertices) ? "Graph is cyclic.\n" : "Graph is acyclic.\n");
                break;
            case 9:
                printf("Exiting...\n");
                exit(0);
            default:
                printf("Invalid choice! Please try again.\n");
        }
    }
    return 0;
}

    }
    return false;
}
