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