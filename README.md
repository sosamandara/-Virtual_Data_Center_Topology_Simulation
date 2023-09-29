# Virtual Data Center Topology Simulation Readme

## Overview

This readme provides a summary of a simulation study that evaluates the performance and connectivity of different virtual data center topologies: Fat-Tree and Jellyfish. We analyze computational complexities, connectivity probabilities, and the impact of node count on connectivity.

## Connectivity and Computational Complexity

We first explored the connectivity of random graphs, focusing on p-ER and r-regular graphs. The computational complexities of various methods were compared:

- **Matrix Exponential Method (p-ER)**: $O(K^3)$, where $K$ is the number of nodes.
- **Eigenvalue Analysis (p-ER)**: $O(K^3)$, optimized for larger graphs with parallelization.
- **Breadth-First Search (BFS) Algorithm**: $O(K + E)$, where $E$ is the number of edges.

## Connectivity in p-ER Graphs

We estimated the probability of a p-ER graph being connected. For $K = 100$ nodes, we observed:

- Low probability of connectivity for small $p (≤ 0.03)$.
- Rapid increase in connectivity probability as p rises from 0.03 to 0.12.

## Connectivity in r-Regular Graphs

In r-regular graphs ($r = 2$ and $r = 8$), we analyzed connectivity probability with respect to the number of nodes (K):

- For $r = 2$, as K increased, connectivity probability decreased due to limited connections.
- For $r = 8$, the graph remained connected as each node had more connections.

## Fat-Tree and Jellyfish Analysis

*Fat-Tree Topology*

- Determines switch and server requirements.
- Constructs a structured graph following the Fat-Tree pattern.

*Jellyfish Topology*

- Creates a topology with the same switches as Fat-Tree.
- Uses the r-regular graph for specific switch connections.

*Performance Simulation*

- Randomly selects a server (A).
- Identifies N nearest servers using Dijkstra's algorithm.
- Simulates task completion time and output size.
- Calculates Round Trip Time (RTT) and average throughput.
- Measures input/output transfer time.

*Metrics*

- Computes response time (R) and job running cost (S).

*Repeated Simulation*

- Repeats the simulation 100 times for N values from 1 to 10,000.
- Calculates mean response time (E[R]) and job running cost (S).
- Normalizes results using single-server performance (Rbase and Sbase).

*Results*

- Figures illustrate expected response time and job running cost.
- Key insights highlight optimal server numbers and the impact of adding more servers.

---

