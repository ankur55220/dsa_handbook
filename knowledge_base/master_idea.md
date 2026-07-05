# Master Ideas

---

# Idea 001

## Name
Problem Architecture Framework

## Status
⭐ Fundamental

## Introduced
Week 1

## Expanded
Week 2
Week 3
Week 4

## Description

A structured framework for deriving algorithms from first principles instead of recognizing patterns. Every problem is analyzed through a sequence of architectural questions before implementation begins.

## Referenced By

### Problems
All problems solved throughout the handbook.

### Patterns

- State Thinking
- Control Engines
- State Machines
- Pipeline Architecture

### Future Chapters

Chapter 1 – The Problem Architecture Framework

## Related Ideas

→ Output Classification

→ State Thinking

→ Control Engines

→ State Machines

## Last Updated

Week 4

---

# Idea 002

## Name

Output Classification

## Status

⭐ Fundamental

## Introduced

Week 1

## Expanded

Week 2

## Description

Every problem should first be classified by the type of output it asks for (minimize, maximize, count, enumerate, decide). The optimization objective determines the search strategy.

## Referenced By

### Problems

All optimization problems.

### Patterns

- BFS
- Dijkstra
- Dynamic Programming
- Greedy

### Future Chapters

Chapter 1

## Related Ideas

→ Control Engines

→ Problem Architecture Framework

## Last Updated

Week 2

---

# Idea 003

## Name

Control Engines

## Status

🟢 Mature

## Introduced

Week 1

## Expanded

Week 3

## Description

Algorithms are consequences of optimization objectives. Instead of memorizing algorithms, derive the correct traversal from the properties of the objective function.

## Referenced By

### Problems

- Path With Minimum Effort
- Minimum Cost Grid
- Bus Routes
- Open Lock

### Future Chapters

Chapter 3 – Control Engines

## Related Ideas

→ Output Classification

→ Dominance

## Last Updated

Week 4

---

# Idea 004

## Name

State Thinking

## Status

⭐ Fundamental

## Introduced

Week 2

## Expanded

Week 3
Week 4

## Description

The state contains only the information required to uniquely determine all future decisions. Path quality belongs to the search, not the state.

## Referenced By

### Problems

- Cherry Pickup
- Shortest Path Visiting All Nodes
- Race Car
- Sliding Puzzle

### Future Chapters

Chapter 2 – State Thinking

## Related Ideas

→ State Completeness

→ State Representation

→ Dominance

→ Information Flow

## Last Updated

Week 4

---

# Idea 005

## Name

State vs Value

## Status

🟢 Mature

## Introduced

Week 2

## Expanded

Week 4

## Description

Separate the logical state from the value accumulated along the path. Future decisions depend on the state, while optimization values (distance, cost, effort, moves) belong to the traversal.

## Referenced By

### Problems

- Race Car
- Sliding Puzzle
- Genetic Mutation

### Future Chapters

Chapter 2

## Related Ideas

→ State Thinking

→ Dominance

## Last Updated

Week 4

---

# Idea 006

## Name

Information Flow

## Status

🟢 Mature

## Introduced

Week 2

## Expanded

Week 4

## Description

Before defining a state, ask:

"What information must survive between decisions?"

Whatever survives becomes a candidate state variable.

## Referenced By

### Problems

- Cherry Pickup
- Race Car
- Sliding Puzzle

### Future Chapters

Chapter 2

## Related Ideas

→ State Thinking

→ State Completeness

## Last Updated

Week 4

---

# Idea 007

## Name

Dominance

## Status

⭐ Fundamental

## Introduced

Week 2

## Expanded

Week 4

## Description

If two executions reach identical states, and one execution is guaranteed to produce an equal or better future for every continuation, the worse execution can be safely discarded.

## Referenced By

### Problems

Almost every optimization problem.

### Future Chapters

Chapter 2

## Related Ideas

→ State Thinking

→ State Completeness

## Last Updated

Week 4

---

# Idea 008

## Name

Pipeline Architecture

## Status

🟢 Mature

## Introduced

Week 3

## Description

Many problems consist of multiple cooperating subsystems. Solve each subsystem independently and define the information exchanged between them.

## Referenced By

### Problems

- Shortest Bridge

### Future Chapters

Chapter 4

## Related Ideas

→ Graph Transformation

→ State Machines

## Last Updated

Week 3

---

# Idea 009

## Name

Graph Transformation

## Status

🟢 Mature

## Introduced

Week 3

## Description

The graph provided by the problem is not always the graph that should be searched. Transform the representation before applying graph algorithms.

## Referenced By

### Problems

- Minimum Cost Grid
- Bus Routes

### Future Chapters

Chapter 4

## Related Ideas

→ Implicit Graphs

→ Data Reorganization

## Last Updated

Week 4

---

# Idea 010

## Name

Implicit Graphs

## Status

🟢 Mature

## Introduced

Week 3

## Description

Nodes and edges may not be explicitly given. They can be derived from the problem representation.

## Referenced By

### Problems

- Bus Routes

### Future Chapters

Chapter 4

## Related Ideas

→ Generated Graphs

→ Graph Transformation

## Last Updated

Week 4

---

# Idea 011

## Name

Generated Graphs

## Status

⭐ Fundamental

## Introduced

Week 3

## Expanded

Week 4

## Description

The graph does not exist beforehand. Neighbors are generated dynamically from the current state using transition rules.

## Referenced By

### Problems

- Open Lock
- Race Car
- Sliding Puzzle
- Genetic Mutation

### Future Chapters

Chapter 4

## Related Ideas

→ State Machines

→ Transition Functions

## Last Updated

Week 4

---

# Idea 012

## Name

State Machines

## Status

🟡 Growing

## Introduced

Week 4

## Description

Every search problem can be viewed as a state machine:

State

↓

Transition Function

↓

Neighbor Generation

↓

Search

## Referenced By

### Problems

- Open Lock
- Race Car
- Sliding Puzzle
- Genetic Mutation

### Future Chapters

Chapter 5

## Related Ideas

→ Generated Graphs

→ Transition Functions

→ State Representation

## Last Updated

Week 4

---

# Idea 013

## Name

Transition Function Engineering

## Status

🟡 Growing

## Introduced

Week 4

## Description

Instead of searching for a graph, define the legal transitions from the current state. The transition function implicitly defines the graph.

## Referenced By

### Problems

- Race Car
- Sliding Puzzle
- Genetic Mutation

### Future Chapters

Chapter 5

## Related Ideas

→ State Machines

→ Generated Graphs

## Last Updated

Week 4

---

# Idea 014

## Name

State Representation Engineering

## Status

🟡 Growing

## Introduced

Week 4

## Description

Logical state and implementation representation are separate engineering decisions. Choose a representation that simplifies comparison, hashing, and transition generation.

## Referenced By

### Problems

- Sliding Puzzle
- Race Car

### Future Chapters

Chapter 6

## Related Ideas

→ State Thinking

→ Transition Functions

## Last Updated

Week 4

---

# Idea 015

## Name

Data Reorganization Before Search

## Status

🟡 Growing

## Introduced

Week 4

## Description

Before optimizing the search algorithm, ask whether the input data can be reorganized into a representation that makes searching trivial.

## Referenced By

### Problems

- Bus Routes
- Word Ladder

### Future Chapters

Chapter 7

## Related Ideas

→ Index-Based Thinking

→ Graph Transformation

## Last Updated

Week 4

---

# Idea 016

## Name

Index-Based Thinking

## Status

🟡 Growing

## Introduced

Week 4

## Description

Repeated expensive searches often indicate that an intermediate index should be built. Replace repeated computation with efficient lookup.

## Referenced By

### Problems

- Word Ladder
- Bus Routes

### Future Chapters

Chapter 8

## Related Ideas

→ Data Reorganization

→ Constraint Driven Design

## Last Updated

Week 4

---

# Idea 017

## Name

Multiple Valid Architectures

## Status

🟡 Growing

## Introduced

Week 4

## Description

Many problems admit multiple correct architectures. Engineering involves selecting the implementation that best matches the constraints rather than searching for a single correct solution.

## Referenced By

### Problems

- Word Ladder

### Future Chapters

Chapter 9

## Related Ideas

→ Constraint Driven Design

→ Data Reorganization

## Last Updated

Week 4

---

# Idea 018

## Name

Constraint-Driven Architecture

## Status

🟡 Growing

## Introduced

Week 4

## Description

The preferred architecture depends on the problem constraints. The same abstraction may require different implementations when input size, alphabet size, or graph structure changes.

## Referenced By

### Problems

- Word Ladder
- Minimum Genetic Mutation

### Future Chapters

Chapter 10

## Related Ideas

→ Multiple Valid Architectures

→ Index-Based Thinking

## Last Updated

Week 4

---

# Idea 019

## Name

State Completeness Test

## Status

🟡 Growing

## Introduced

Week 4

## Description

To validate a proposed state, construct two executions that reach the same state. If their future legal moves or outcomes differ, the state is incomplete and must be expanded.

## Referenced By

### Problems

- Race Car
- Sliding Puzzle

### Future Chapters

Chapter 2

## Related Ideas

→ State Thinking

→ Dominance

## Last Updated

Week 4

Idea 030

Capability vs Search Value

Status

Growing

Introduced

Week 5

Summary

Capability determines future legal actions.
Search Value measures how good a path currently is.

Idea 021

Resource-Augmented State

Status

Growing

Introduced

Obstacle Elimination

Summary

If acquiring or consuming a resource changes future decisions,
that resource belongs in the state.

Idea 022

Objective vs Constraint

Status

Growing

Introduced

Cheapest Flights

Summary

Never confuse what is being optimized with what limits feasible solutions.

Idea 023

Identity vs Quantity

Status

Growing

Introduced

Shortest Path to Get All Keys

Summary

Sometimes knowing "how many" resources exist is insufficient.
Future behavior depends on "which" resources exist.

Idea 023

Set Dominance

Status

Growing

Introduced

Shortest Path to Get All Keys

Summary

For set-valued state,
dominance only exists when one state's set is a superset of another.

Idea 024

Minimal Complete State

Status

Growing

Introduced

Shortest Path in Binary Matrix

Summary

A state should contain exactly the information required to determine every future decision.
Nothing more.
Nothing less.

Idea 025

Path Value Propagation

Status

Growing

Introduced

Swim in Rising Water

Summary

Every optimization problem propagates its search value differently.

Examples:

+

max()

min()

bitwise OR

union

Idea 026

State Finalization

Status

Growing

Introduced

Week 5

Summary

Every traversal has a point where a state becomes mathematically final.

BFS

↓

Discovery

Dijkstra

↓

Pop

Idea 027

Algorithm Discovery vs Recognition

Status

Growing

Introduced

Week 5

Summary

Algorithms should emerge from invariants rather than be recognized by pattern matching.
