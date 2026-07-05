# week 2
Initial Thinking

State = Current Position

↓

Counterexample

Different futures

↓

Discovery

State must include every piece of information that affects the future.

# week 3

Initial Thinking

Problems are single algorithms.

↓

Discovery

Many problems are cooperating architectures.

↓

General Principle

Decompose before solving.

# Week 4


## Race Car

Initial Thought

State = Position

↓

Counterexample

Different speeds

↓

Discovery

State = (Position, Speed)

↓

General Principle

If futures differ,
the proposed state is incomplete.

---

## Sliding Puzzle

Initial Thought

State = Zero Position

↓

Counterexample

Different boards.

Same blank position.

↓

Discovery

Entire board is the state.

---

## Genetic Mutation

Initial Thought

Reuse Word Ladder.

↓

Discovery

Same abstraction.

Different constraints.

↓

Engineering Decision

Generate neighbors instead of wildcard preprocessing

# Week 5

## Biggest Evolution

Before

I viewed state as simply extra information.

After

I distinguish between

- State
- Search Value
- Capability
- Constraint

and understand that each serves a different purpose.

---

## Biggest Discovery

Future equivalence determines state.

Not implementation.

---

## Biggest Mistake Fixed

Not every optimization value belongs in the state.

---

## Engineering Principle Learned

Traversal guarantees determine storage.

visited[state]

vs

bestValue[state]

is derived mathematically rather than memorized.

---

## Personal Milestone

For the first time I independently derived Prim's Algorithm
without recognizing it by name.
