# Graphplan Algorithm Visualizer

Interactive visualization of the **Graphplan AI planning algorithm** — built for CS 3511 Honors Algorithms at Georgia Tech.

🔗 **[Live Demo](https://sarvesh-tiku.github.io/Graph-Plan-Algorithm/)**

![Graphplan Demo](https://your-gif-url-here.gif)

---

## What it does

Graphplan builds a layered graph of propositions and actions, uses **mutex constraints** to prune impossible combinations, then runs **backward search** to extract a valid parallel plan.

Default scenario: you're *asleep, hungry, at home* — goal is to be *awake, fed, dressed, at class*.

---

## Usage

| Button | Action |
|---|---|
| **▶ Step** | Expand graph one stage |
| **Auto** | Step + search automatically |
| **Search** | Extract plan from current graph |
| **✎ Edit Domain** | Define your own scenario |

Hover any node for details. Toggle **no-ops** and **mutex arcs** with the checkboxes.

---

## How it works

1. **Expand** — alternates Proposition Levels and Action Levels; no-ops carry facts forward
2. **Mutex** — marks action/proposition pairs that can't coexist at the same level
3. **Search** — backward goal-regression once goals are reachable and non-mutex

---

## Stack

Pure HTML/CSS/JS — no dependencies, no build step.

---

## Reference

Blum & Furst, *Fast Planning Through Planning Graph Analysis* (1997) · CS 3511 Honors Algorithms, Georgia Tech · **Sarvesh Tiku**
