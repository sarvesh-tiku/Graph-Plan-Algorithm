# Graphplan Algorithm Visualizer

An interactive visualization of the Graphplan AI planning algorithm, built for CS 3511 Honors Algorithms at Georgia Tech — taught by **Merrick Furst**, one of the algorithm's original authors.

🔗 **[Live Demo](https://sarvesh-tiku.github.io/Graph-Plan-Algorithm/)**

<img width="1313" height="484" alt="Graphplan Visualizer" src="https://github.com/user-attachments/assets/55cc28e6-2eba-4178-bbab-86ab9f6bfb9a" />

---

Graphplan builds a layered graph alternating proposition and action levels, propagates mutex constraints to prune impossible combinations, then runs backward goal-regression to extract a valid parallel plan — all without ever searching the full state space.

The default scenario is minimal on purpose: start *asleep, hungry, at home*, reach *awake, fed, dressed, at class*. Simple enough to trace by hand, complex enough to show where the algorithm earns its keep.

---

## Usage

| Control | |
|---|---|
| **▶ Step** | Expand the graph one stage |
| **Auto** | Run expansion and search to completion |
| **Search** | Extract a plan from the current graph |
| **✎ Edit Domain** | Swap in your own propositions, operators, and goals |

Hover any node or arc for inline detail. Mutex arcs and no-op actions are toggleable.

---

## How it works

1. **Expand** — alternate Proposition and Action levels; no-ops carry facts forward unchanged
2. **Mutex propagation** — flag action/proposition pairs that cannot coexist at the same level, pruning the search space before extraction begins
3. **Backward search** — once all goals appear non-mutex in a proposition level, regress through the graph toward the initial state

---

<sub>**Sarvesh Tiku** · CS 3511 Honors Algorithms · Georgia Institute of Technology</sub>

<sub>Blum, A., & Furst, M. L. (1997). Fast planning through planning graph analysis. *Artificial Intelligence, 90*(1–2), 281–300. https://doi.org/10.1016/S0004-3702(96)00047-1</sub>
