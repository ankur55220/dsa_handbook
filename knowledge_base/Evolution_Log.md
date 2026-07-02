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

Generate neighbors instead of wildcard preprocessing.