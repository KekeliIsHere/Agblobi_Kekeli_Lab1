# Drone Pathfinding & Terrain Navigation using Search Algorithms

## Course: Introduction to Artificial Intelligence (Lab 1)
**Student Name:** Kekeli Yao Agblobi  
**Student ID:** 45862028  
**Submission Date:** June 2026  

---

## Project Overview
This repository contains an object-oriented Python framework for pathfinding logic deployed on an autonomous environmental-monitoring drone. The system simulates navigating a 2D grid world from a designated start position (`S`) to a destination goal (`G`). 

The project is split into two foundational paradigms, tracking how an agent transitions from blind exploration to intelligent, domain-aware navigation:

1. **Part A: Uninformed Search (Blind Exploration)**
   * The drone navigates uniform-cost grids with no spatial context or understanding of whether a move approaches or recedes from the goal.
2. **Part B: Informed Search (Heuristic-Driven Navigation)**
   * The drone utilizes GPS coordinates to calculate heuristic distances ($h(n)$) and adapts to non-uniform terrain costs (e.g., routing safely around high-battery-drain turbulence zones or wind corridors rather than just taking the shortest path).

---

## Algorithms Implemented & Profiled

### Uninformed Strategies (Part A)
* **Breadth-First Search (BFS):** Guarantees optimal path depth on uniform grids using a FIFO queue.
* **Depth-First Search (DFS):** Explores deeply using a LIFO stack; space-efficient but non-optimal.
* **Depth-Limited Search (DLS):** Restricts DFS traversal depth to mitigate infinite paths.
* **Iterative Deepening Search (IDS):** Combines the optimal depth guarantees of BFS with the linear memory space of DFS.

### Informed Strategies (Part B)
* **Uniform-Cost Search (UCS):** Finds the cost-optimal path by sorting the frontier strictly by accumulated step cost ($f(n) = g(n)$).
* **Greedy Best-First Search:** Prioritizes speed by expanding nodes estimated closest to the goal ($f(n) = h(n)$), ignoring historical costs.
* **A\* Search:** Achieves absolute cost-optimality by balancing cost-paid and estimated remaining path cost ($f(n) = g(n) + h(n)$).
* **Weighted A\*:** Accelerates search speeds by introducing a bounded suboptimality multiplier ($f(n) = g(n) + W \cdot h(n)$).
* **Iterative-Deepening A\* (IDA\* - Bonus):** A memory-optimized variation that bounds search paths using $f$-cost thresholds instead of depth levels.

---

## Repository Structure
* `Kekeli_Agblobi_Lab_1A.ipynb` — Core implementation notebook for uninformed search frameworks.
* `Kekeli_Agblobi_Lab_1B.ipynb` — Completed informed search notebook, including terrain weight overrides, heuristic functions (Manhattan & Euclidean), suboptimality experiments, and comparison plots.
* `AI Use Declaration Form.doc` — Transparency report documenting generative tool use for scaffolding search engines, code refactoring, and stack tracing.
* `AI_Prompt_History_Lab1A.txt` — Shows the prompt and their summary response given by the main AI used(Gemini) for Lab A
* `AI_Prompt_History_Lab1B.txt` — Just like the first one it shows my prompts and their summary response given by the main AI used(Gemini) for Lab B
* `README.md` — Project documentation and performance summary (this file).

---

## Core Performance Metrics Tracked
Every search execution evaluates algorithmic efficiency and trade-offs using these standardized benchmarks:
* **Solution Depth:** The step count of the path from start to goal.
* **Solution Cost:** The cumulative mathematical cost of terrain crossed (where obstacles are unpassable, calm spaces cost $1.0$, and severe turbulence costs $\ge 3.0$).
* **Nodes Expanded:** Total states popped from the frontier queue to execute neighbor generation.
* **Max Frontier Size:** The peak size of the frontier queue, indicating the maximum memory footprint.
* **Reached States:** Total unique grid coordinates logged in the spatial lookup table.

---
