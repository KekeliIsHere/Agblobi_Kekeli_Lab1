# Drone Pathfinding using Uninformed Search Algorithms

## Course: Introduction to Artificial Intelligence
### Lab 1 Part A — Uninformed Search Algorithms
**Student Name:** Kekeli Yao Agblobi  
**Student ID:** 45862028  
**Submission Date:** 5th June 2026  

---

## Project Overview
This repository contains the object-oriented Python implementation of pathfinding logic for an autonomous environmental monitoring drone. The drone's objective is to safely navigate a 2D grid world from a designated start position (`S`) to a destination goal (`G`) while successfully maneuvering around obstacles such as dense forests, restricted zones, and dangerous terrain.

The project evaluates, profiles, and compares four classic uninformed search algorithms:
1. **Breadth-First Search (BFS)**
2. **Depth-First Search (DFS)**
3. **Depth-Limited Search (DLS)**
4. **Iterative Deepening Search (IDS)**

---

##  Repository Structure
* `Kekeli_Agblobi_Lab_1A.ipynb` — The Jupyter Notebook containing all formal mathematical definitions, class overrides (`GridProblem`, `Node`, `SearchAlgorithm`), test grids, and profiling performance tables.
* 
* `AI_Prompt_History_Lab1A.txt` — Plain-text evidence showing the raw prompt exchanges and diagnostic iterations used in Lab1A.
* `README.md` — Project roadmap and setup instructions (this file).

---

## Core Performance Metrics Tracked
Every search execution evaluates behavioral differences using specific parameters:
* **Solution Depth**: The path length (number of transitions) from start to goal.
* **Path Cost**: The accumulated path cost calculated via the problem's step transitions.
* **Nodes Expanded**: Total number of states removed from the frontier and expanded.
* **Max Frontier/Stack Size**: The peak memory footprint observed during the search space traversal.

---

