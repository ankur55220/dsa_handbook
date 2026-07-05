11. Representation Engineering

Can the logical state be represented better?

---

12. Transition Function

Given the current state,
what legal moves exist?

---

13. Multiple Architectures

Is there more than one valid representation?

---

14. Constraint Analysis

Do the constraints change the best architecture?

# Week 5 Additions

After identifying the candidate state, always ask

□ Is this State or Search Value?

□ Is this Capability?

□ Is this Constraint?

□ Does it change future decisions?

□ Does dominance exist?

□ Can the state be compressed?

□ Does the traversal guarantee optimality?

If yes

↓

visited

If no

↓

bestValue
