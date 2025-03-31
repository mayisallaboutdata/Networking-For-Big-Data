# Networking for Big Data: Data Centers – Topology Design Challenge

This repository contains the work for the Topology Design challenge from the 2023/2024 "Networking for Big Data: Data Centers" course. Our project explores the design and analysis of data center topologies using both Erdős-Rényi (ER) graphs and r-Regular graphs. We evaluate graph connectivity and response time metrics to assess the performance of different network designs.

## Team Quimby

- **Simay Çalışkan** – 2105260  
- **Dila Aslan** – 2113310  
- **Umut Altun** – 2101934  
- **Mayis Atayev** – 2104359

## Project Overview

The project is divided into two main parts:

### 1. Graph Connectivity Analysis
- **Graph Types:**  
  - **ER Graphs:** Random graphs where each edge is included with probability _p_.  
  - **r-Regular Graphs:** Graphs where each node has exactly _r_ neighbors.
- **Connectivity Methods:**  
  We implement three algorithms to check graph connectivity:
  - **Irreducibility method:** Exhibits cubic complexity.
  - **Laplacian Eigenvalue method:** Also cubic in complexity, but more efficient than irreducibility.
  - **Breadth-First Search (BFS):** Quadratic complexity, proving more scalable for larger graphs.
- **Key Findings:**
  - For ER graphs, as _p_ increases, connectivity probability sharply rises, with a critical threshold around _p = 0.08_.
  - For r-Regular graphs, connectivity trends vary: 2-regular graphs become less connected as the number of nodes increases, whereas 8-regular graphs maintain a high probability of connectivity.

### 2. Local versus Distributed Run Analysis
- **Mean Response Time Algorithm:**  
  We design an algorithm to measure the mean response time as a function of the number of servers.
- **Performance Evaluation:**
  - **Normalized Mean Response Time:**  
    Both Fat-Tree and Jellyfish topologies show an initial steep decrease in response time with more servers.
  - **Job Running Cost:**  
    - **Fat-Tree Topology:** Optimal at 32 servers; cost increases sharply beyond this point.
    - **Jellyfish Topology:** Optimal at 242 servers; remains more stable and cost-effective even as the number of servers grows.
- **Observations:**  
  The Jellyfish topology outperforms Fat-Tree in distributed settings due to its flexible routing, which reduces congestion and balances network traffic more evenly. Monte Carlo simulations further highlight the robustness and variability of the Jellyfish design.

## Repository Contents

- **Source Code & Scripts:**  
  Scripts for generating ER and r-Regular graphs, implementing connectivity checks, and evaluating mean response times.
- **Report:**  
  A comprehensive PDF report documenting our methodology, experimental results, and analysis.


## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
