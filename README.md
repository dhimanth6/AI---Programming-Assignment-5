# AI-Programming-Assignment-5
# AI Algorithms Assignment

This repo has my implementations for the AI programming assignment. Four parts — search algorithms, a travel planner, a knowledge graph, and a Bayesian network.

---

## What's inside
├── min-max.py            # Minimax, Alpha-Beta, Heuristic AB, MCTS
├── travel_planner.py     # AI travel planner with recommendations
├── knowledge_graph.py    # Movie knowledge graph with NetworkX
├── bayesian_network.py   # Students's performance model with pgmpy

---

## Dependencies

```bash
pip install networkx matplotlib pgmpy
```

Everything else is standard Python 3.

---

## 1. Search Algorithms — `min-max.py`

Implemented all four algorithms on Tic-Tac-Toe so there's a clear way to test correctness.

- **Minimax** — explores the full game tree, no shortcuts
- **Alpha-Beta Pruning** — same result as Minimax but skips branches that won't matter. Cuts node count by ~96% on an empty board
- **Heuristic Alpha-Beta** — adds a depth limit so it doesn't search forever. Uses a simple board evaluation function when it hits the cutoff
- **MCTS** — runs random playouts instead of evaluating every state. The more iterations you give it, the better it plays

```bash
python min-max.py
```

---

## 2. AI Travel Planner — `travel_planner.py`

Recommends destinations based on what you're into, what you want to eat, when you're travelling, and how much you want to spend per day. Uses a local knowledge base for cities, food types, and activities — no API needed.

Gives you a day-by-day itinerary with cost estimates, hotel suggestions, and food picks once it narrows down a destination.

```bash
python travel_planner.py
```

---

## 3. Knowledge Graph — `knowledge_graph.py`

Built a movie knowledge graph with NetworkX. Nodes are movies, actors, directors, and genres. Edges are relationships between them (acted_in, directed_by, belongs_to, etc.).

You can query things like "which actors worked with this director" or "what films share a genre" directly from the graph. Also renders a visual using matplotlib.

```bash
python knowledge_graph.py
```

---

## 4. Bayesian Network — `bayesian_network.py`

Models student exam performance using pgmpy. The variables are Study, Difficulty, Grade, and Pass — with Grade depending on both Study and Difficulty, and Pass depending on Grade.

Uses exact inference to answer queries like "what's the probability of passing if the student studied but the exam was hard." The numbers come out sensible which is a good sign the CPTs are wired up correctly.

```bash
python bayesian_network.py
```# AI---Programming-Assignment-5
