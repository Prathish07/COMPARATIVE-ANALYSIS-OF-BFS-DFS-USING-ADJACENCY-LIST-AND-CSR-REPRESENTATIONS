# COMPARATIVE-ANALYSIS-OF-BFS-AND-DFS-USING-ADJACENCY-LIST-AND-CSR
Comparative performance analysis of BFS and DFS using Adjacency List and CSR representations for scalable graph traversal.

## Overview
Graph traversal algorithms are fundamental to many applications such as network analysis, recommendation systems, and web crawling.  

This project presents a comparative study of **Breadth First Search (BFS)** and **Depth First Search (DFS)** using two graph representations:

- Adjacency List
- Compressed Sparse Row (CSR)

The goal is to analyze how graph storage structures influence traversal performance, memory usage, and scalability for large graphs.

---

## Objectives
- Implement BFS and DFS traversal algorithms
- Represent graphs using **Adjacency List** and **CSR**
- Compare traversal performance across different graph sizes
- Evaluate execution time and scalability
- Visualize performance trends

---

## Technologies Used
- **C++** – Graph algorithms and performance measurement
- **Python (Matplotlib)** – Performance visualization
- **STL Data Structures** – Queue, vector, recursion
- **Random Graph Generation**

---

## Repository Structure
- Graph-BFS-DFS-CSR
- |code
- │ bfs_dfs_comparison.cpp
- |plots
- │ bfs_comparison.png
- │ dfs_comparison.png
- |documentation
- │ Doc.pdf
- |README.md


---

## Algorithms Implemented

### Breadth First Search (BFS)
- Uses a **FIFO queue**
- Explores graph **level by level**
- Time Complexity: **O(V + E)**

### Depth First Search (DFS)
- Uses **recursion or stack**
- Explores graph **depth first**
- Time Complexity: **O(V + E)**

---

## Graph Representations

### Adjacency List
- Stores neighbors for each vertex
- Flexible for dynamic graphs
- Requires pointer-based memory access

### Compressed Sparse Row (CSR)
- Stores graph in compact arrays
- Improves memory locality
- Suitable for large static graphs

---

## Experimental Setup
- Graph sizes: **1000, 5000, 10000 vertices**
- Random undirected graphs
- Approximately **3 × V edges**
- Execution time measured using C++ `chrono`

---

## Results

| Vertices | BFS (Adjacency List) | DFS (Adjacency List) | BFS (CSR) | DFS (CSR) |
| -------- | -------------------- | -------------------- | --------- | --------- |
| 1000     | 0.3962 ms            | 0.5592 ms            | 0.2891 ms | 0.2791 ms |
| 5000     | 1.7368 ms            | 1.5117 ms            | 1.0482 ms | 0.7782 ms |
| 10000    | 3.8149 ms            | 5.3644 ms            | 2.4037 ms | 1.9884 ms |


### Key Observations
- CSR consistently outperforms adjacency list.
- Performance gap increases with graph size.
- CSR benefits from better **cache locality and memory layout**.

---

## Performance Visualization

Graphs were generated using Python's **Matplotlib** to visualize runtime trends for BFS and DFS across different graph sizes.

---

## Conclusion

Although both representations have the same theoretical complexity **O(V + E)**, CSR demonstrates better real-world performance for large graphs due to improved memory locality and reduced traversal overhead.

Adjacency lists remain useful for **dynamic graphs**, while CSR is ideal for **large-scale graph analytics and high-performance computing environments**.

---

## Author
**Prathish A**  
M.Tech CSE (AI/ML)  

---
