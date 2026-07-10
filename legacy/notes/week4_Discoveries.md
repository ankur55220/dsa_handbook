# Week 4 Discoveries

## Discovery 1 - Every Search Problem is a State Machine

State
↓

Transition Function
↓

Search

Problems:
- Open Lock
- Race Car
- Sliding Puzzle
- Genetic Mutation

---

## Discovery 2 - State Representation Engineering

Logical State != Implementation Representation

Examples:
Race Car
Sliding Puzzle
Bus Routes

---

## Discovery 3 - Data Reorganization Before Search

Instead of optimizing search,
reorganize the data.

Examples:
Bus Routes
Word Ladder

---

## Discovery 4 - Multiple Valid Architectures

One abstraction

↓

Multiple correct implementations

Trade-offs depend on constraints.

---

## Discovery 5 - Constraint Driven Design

Word Ladder

26 letters

↓

Wildcard preprocessing

Genetic Mutation

4 letters

↓

Generate neighbors

---

## Discovery 6 - Transition Functions

Don't search for graphs.

Ask:

Given a state,
what legal moves exist?

---

## Discovery 7 - State Completeness Test

Counterexample

↓

Refine state

↓

Repeat
