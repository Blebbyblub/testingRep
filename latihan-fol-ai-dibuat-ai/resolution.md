---
description: >-
  After changing the english language to CNF, we can make a resolution using all
  the statements based on what needs understanding/resolving
---

# Resolution

### Question:

Use resolution to prove or disprove the statement:\
_"If it is raining, then the ground is wet."_\
Assume the following facts are given:

1. "It is raining."
2. "If it is raining, then the ground is wet."

<details>

<summary>Click to reveal the answer</summary>

#### Answer:

1. **Convert each statement into First-Order Logic (FOL)**:
   * Fact 1: Raining
   * Fact 2: Raining → Wet(Ground)
2. **Convert Fact 2 into CNF**:
   * Raining → Wet(Ground) becomes ¬Raining ∨ Wet(Ground)
3. **Set up the resolution**:
   * We have:
     * Clause 1: Raining
     * Clause 2: ¬Raining ∨ Wet(Ground)
4. **Apply resolution**:
   * Since we have Raining and ¬Raining ∨ Wet(Ground), we can resolve these clauses by removing Raining:
     * This gives us Wet(Ground).
5. **Conclusion**:
   * The resolution result is Wet(Ground), meaning we have proven that if it is raining, then the ground is indeed wet based on the given facts.

</details>
