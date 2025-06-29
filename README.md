# 🧠 QUBO Formulation for Weekend Event Assignment

This project demonstrates the use of a **Quadratic Unconstrained Binary Optimization (QUBO)** model to solve a constrained event assignment problem using quantum-inspired methods.

---

## 🧩 Problem Overview

We are given:

- **5 events** scheduled across a weekend (Saturday and Sunday).
- **5 persons** are available to attend these events.
- **Each person must attend exactly two different events.**

### 🎯 Objective

- **Maximize the total edge weight** in a graph, where:
  - **Nodes** represent the events (E1 to E5).
  - **Edges** represent a pair of events attended by the same person.
- Each person contributes one edge between their two chosen events.
- The goal is to assign events to each person such that the resulting graph has the highest total weight (maximum number of high-value connections).

---

## 🖼️ Graph Representation

- **Nodes:**  
  - `E1`, `E2`, `E3`, `E4`, `E5` — representing 5 unique events.
  
- **Edges:**  
  - A person attending `E2` and `E4` contributes an edge `(E2, E4)`.
  - The final graph is formed by all such edges created by all 5 persons.

- The edge weight increases with every valid person-to-event assignment.

### 📘 Example Edge Set

```text
Person 1 → E1 & E2 → Edge: (E1, E2)  
Person 2 → E2 & E4 → Edge: (E2, E4)  
Person 3 → E3 & E4 → Edge: (E3, E4)  
Person 4 → E3 & E5 → Edge: (E3, E5)  
Person 5 → E1 & E5 → Edge: (E1, E5)
