# Problem Architecture Checklist

> "Don't search for algorithms. Discover the architecture."

This checklist is the first thing to mentally execute whenever solving a new problem.

---

# Phase 1 — Understand the Problem (Week 1)

## □ 1. What is the output asking for?

Classify the problem before thinking about algorithms.

Examples

- Minimum
- Maximum
- Count
- Boolean (Exists?)
- Enumeration
- Construction

This determines the type of search.

---

## □ 2. Why does brute force fail?

Identify why exploring all possibilities explodes.

Common reasons

- Exponential branching
- Repeated computation
- Revisiting identical situations
- Large search space

---

# Phase 2 — Information Flow (Weeks 1 & 2)

## □ 3. What information controls future decisions?

Ask yourself:

> "If I remove this information, will the future become different?"

If YES

↓

It belongs in the state.

---

## □ 4. Separate State from Search Value

Never mix these.

### State

Information that determines future possibilities.

Examples

- Position
- Speed
- Keys
- Remaining fuel
- Stops used

### Search Value

The quantity being optimized.

Examples

- Steps
- Cost
- Time
- Probability

---

## □ 5. Is there a capability/resource?

Does something change what actions are legal?

Examples

- Remaining obstacle eliminations
- Fuel
- Keys
- Permissions
- Energy

If YES

↓

It belongs in the state.

---

# Phase 3 — State Engineering (Weeks 2 & 5)

## □ 6. Propose the candidate state

Ask

> "What is the minimum information needed to uniquely determine every future decision?"

Remember

State should be

- Complete
- Minimal

Never larger than necessary.

---

## □ 7. State Audit

Imagine two executions reaching the same candidate state.

Ask

> "Can they have different futures?"

YES

↓

State is incomplete.

NO

↓

State is complete.

---

## □ 8. Identity vs Quantity

Ask

> "Does the future depend on how many resources exist, or exactly which ones?"

Example

❌ Number of keys

✅ Set of keys

---

# Phase 4 — Dominance (Weeks 2 & 5)

## □ 9. Can one state safely replace another?

Possible outcomes

### Total Dominance

One state is always better.

Example

More remaining obstacle eliminations.

---

### Partial Dominance

Depends on another dimension.

Example

Cheapest Flights

(city, stops)

---

### Set Dominance

One resource set completely contains another.

Example

Keys

{a,b,c}

dominates

{a,b}

---

### No Dominance

Both executions must continue.

---

Never prune until dominance is proven.

---

# Phase 5 — Architecture Discovery (Weeks 3 & 4)

## □ 10. How many responsibilities exist?

Look for cooperating subsystems.

Examples

Generate neighbors

↓

Traversal

---

Pattern construction

↓

Search

---

State Machine

↓

BFS

---

## □ 11. Can the graph be generated instead of built?

Look for

- Implicit Graph
- Generated Graph
- State Machine
- Index Mapping

Avoid building huge graphs if neighbors can be generated.

---

# Phase 6 — Control Engine (Weeks 4 & 5)

## □ 12. What traversal naturally emerges?

Don't ask

> "Which algorithm is this?"

Instead ask

> "What traversal best satisfies the optimization objective?"

Examples

- BFS
- 0-1 BFS
- Priority Queue
- DFS
- DP
- Topological Traversal

Derive.

Don't recognize.

---

# Phase 7 — Storage Strategy (Week 5)

## □ 13. Does the traversal guarantee optimality?

If YES

↓

visited[state]

Examples

- BFS
- Multi-source BFS

---

If NO

↓

bestValue[state]

Examples

- Dijkstra
- Dynamic Programming
- Bellman-Ford

---

# Phase 8 — State Finalization (Week 5)

## □ 14. When does a state become mathematically final?

Examples

### BFS

Finalized when discovered (push).

---

### Dijkstra

Finalized when popped.

---

Storage strategy follows from this.

---

# Phase 9 — Complexity

## □ 15. Derive complexity from architecture

Don't count loops.

Instead derive

Complexity =

State Space

×

Transition Function

Examples

State

(row,col,keyMask)

×

4 directions

↓

O(n × m × 2^k)

---

# Common Failure Modes

Before coding, check:

□ Mixed State with Search Value

□ Forgot Capability

□ Added unnecessary state

□ Candidate state fails State Audit

□ Assumed dominance without proof

□ Used visited instead of bestValue

□ Used bestValue when visited was enough

□ Built an explicit graph unnecessarily

□ Started coding before discovering architecture

---

# Mental Model

Optimization

↓

Information that survives

↓

State

↓

State Audit

↓

Dominance

↓

Architecture

↓

Traversal

↓

Storage

↓

Implementation

---

# Golden Rules

1. State is information that changes future decisions.

2. Search Value is what is being optimized.

3. Capability changes what actions are legal.

4. Dominance must be proven before pruning.

5. Build the minimum complete state.

6. Derive traversal from the optimization objective.

7. Storage follows from traversal guarantees.

8. Algorithms are discovered through invariants, not recognized by name.
