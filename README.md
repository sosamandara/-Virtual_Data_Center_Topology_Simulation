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

We implemented Fat-Tree and Jellyfish topologies with n = 64 ports. Key insights from our study include:

- **Fat-Tree**: Deterministic structure, unaffected by server choice.
- **Jellyfish**: Random interconnect scheme, requiring randomized server selection.

## Conclusion

This readme summarizes our findings regarding the connectivity and performance of virtual data center topologies. These insights are crucial for optimizing network configurations and avoiding overload, especially when dealing with large-scale data center setups.

---

This consolidated readme provides an overview of your simulation study, including insights on connectivity and computational complexities for different graph types and the analysis of Fat-Tree and Jellyfish topologies.
