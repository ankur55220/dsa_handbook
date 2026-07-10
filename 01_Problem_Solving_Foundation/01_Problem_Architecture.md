# Problem Architecture

> "Before choosing an algorithm, understand the architecture of the problem."

---

# Why this chapter exists

One of the biggest mistakes engineers make while preparing for coding interviews is attempting to recognize patterns immediately.

Questions like

- "Is this BFS?"
- "Is this Dynamic Programming?"
- "Is this Sliding Window?"

are asked too early.

These questions focus on implementation before understanding the problem itself.

As a result, even engineers who have solved hundreds of problems often struggle when interview questions combine multiple patterns together.

This chapter introduces a different way of thinking.

Instead of recognizing algorithms, we first discover the architecture of the problem.

Algorithms become a consequence of understanding rather than memorization.

---

# The Philosophy

Every problem is an engineering system.

Just as large software systems are built from interacting components, algorithmic problems are composed of reusable architectural pieces.

Instead of asking

> "Which algorithm should I use?"

we ask

> "How is this problem constructed?"

Once the architecture becomes clear, the algorithm usually follows naturally.

---

# The Universal Problem Solving Pipeline

Every problem in this handbook is analyzed using the same pipeline.

```
Problem

↓

Objective

↓

Future Determining Information

↓

Invariant

↓

Representation

↓

Maintenance Engine

↓

Repair Strategy

↓

Consumer
```

Every future chapter expands one part of this pipeline.

---

# Step 1 — Discover the Objective

Before thinking about data structures or algorithms, classify the output.

Every problem belongs to one of a small number of categories.

Examples include

- Optimization
- Decision
- Counting
- Construction
- Enumeration

The objective determines how the final answer is consumed.

---

# Step 2 — Discover What Controls the Future

Ask

> "What information changes future decisions?"

This information becomes the algorithm's state.

Examples

- Position
- Remaining fuel
- Keys collected
- Transactions completed
- Current speed

Future chapters will call this **State Engineering**.

---

# Step 3 — Discover the Invariant

Many problems process information continuously.

Ask

> "What condition must remain true?"

Examples

- Window contains unique characters.
- Window satisfies all requirements.
- Difference between maximum and minimum remains within a limit.

Future chapters will call this **Invariant Engineering**.

---

# Step 4 — Choose a Representation

Once the state or invariant is known, determine how it can be maintained efficiently.

Examples

- Frequency Map
- Bitmask
- Priority Queue
- Monotonic Deque
- Prefix Sum
- Trie

Representations exist to support efficient maintenance.

They are not the algorithm itself.

---

# Step 5 — Build the Maintenance Engine

Algorithms are continuous processes.

Every iteration performs three responsibilities.

```
Update

↓

Validate

↓

Repair
```

Different problems implement these responsibilities differently, but the architecture remains the same.

---

# Step 6 — Consume the Answer

Once the architecture guarantees correctness, decide how the result should be used.

Examples

- Return immediately.
- Maximize.
- Minimize.
- Count.
- Collect.

Changing only the consumer often transforms one problem into another.

---

# Architecture Before Algorithms

Notice that none of the previous steps required knowing

- BFS
- DFS
- DP
- Sliding Window
- Binary Search

These techniques are implementation choices.

Architecture comes first.

Implementation comes second.

---

# Common Mistakes

## Mistake 1

Trying to recognize the algorithm before understanding the problem.

---

## Mistake 2

Thinking about code before identifying the objective.

---

## Mistake 3

Treating every LeetCode problem as an independent trick.

---

## Mistake 4

Memorizing templates instead of understanding the engineering process.

---

# Key Takeaways

Before solving any problem, ask:

1. What is the objective?
2. What information controls future decisions?
3. What invariant defines correctness?
4. What representation maintains that information?
5. How is correctness maintained?
6. How is the answer consumed?

These six questions form the foundation of the DSA Engineering Handbook.

Every future chapter builds on them.
