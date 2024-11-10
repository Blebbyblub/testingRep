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

### Question:

Use resolution to prove or disprove the statement:\
_"If John is hungry and there is food, then John will eat."_

Assume the following facts are given:

1. "If John is hungry, then he will look for food."
2. "If John looks for food and there is food, then he will eat."
3. "John is hungry."
4. "There is food."

<details>

<summary>Click to reveal the answer</summary>

#### Answer:

1. **Convert each statement into First-Order Logic (FOL)**:
   * Fact 1: Hungry(John) → LookForFood(John)
   * Fact 2: LookForFood(John) ∧ Food → Eat(John)
   * Fact 3: Hungry(John)
   * Fact 4: Food
2. **Convert each statement into CNF**:
   * Fact 1 (Hungry(John) → LookForFood(John)): ¬Hungry(John) ∨ LookForFood(John)
   * Fact 2 (LookForFood(John) ∧ Food → Eat(John)): ¬LookForFood(John) ∨ ¬Food ∨ Eat(John)
   * Fact 3 (John is hungry): Hungry(John)
   * Fact 4 (There is food): Food
3. **Set up the resolution process**:
   * We have the following clauses:
     * Clause 1: ¬Hungry(John) ∨ LookForFood(John)
     * Clause 2: ¬LookForFood(John) ∨ ¬Food ∨ Eat(John)
     * Clause 3: Hungry(John)
     * Clause 4: Food
4. **Apply resolution steps**:
   * Step 1: Resolve Clause 1 (¬Hungry(John) ∨ LookForFood(John)) with Clause 3 (Hungry(John)):
     * This gives LookForFood(John).
   * Step 2: Resolve the result (LookForFood(John)) with Clause 2 (¬LookForFood(John) ∨ ¬Food ∨ Eat(John)):
     * This gives ¬Food ∨ Eat(John).
   * Step 3: Resolve the result (¬Food ∨ Eat(John)) with Clause 4 (Food):
     * This gives Eat(John).
5. **Conclusion**:
   * The resolution process yields Eat(John), meaning we have proven that if John is hungry and there is food, then John will eat.

</details>

### Question:

Use resolution to prove or disprove the statement:\
_"If there is a fire and John has water, he will put out the fire."_

Assume the following facts are given:

1. "If John sees smoke, he believes there is a fire."
2. "If John believes there is a fire and he has water, then he will put out the fire."
3. "If John sees smoke, he has water."
4. "John sees smoke."
5. "If there is a fire, there is smoke."

<details>

<summary>Click to reveal the answer</summary>

#### Answer:

1. **Convert each statement into First-Order Logic (FOL)**:
   * Fact 1: SeesSmoke(John) → BelievesFire(John)
   * Fact 2: BelievesFire(John) ∧ HasWater(John) → PutOutFire(John)
   * Fact 3: SeesSmoke(John) → HasWater(John)
   * Fact 4: SeesSmoke(John)
   * Fact 5: Fire → Smoke
2. **Convert each statement into CNF**:
   * Fact 1 (SeesSmoke(John) → BelievesFire(John)): ¬SeesSmoke(John) ∨ BelievesFire(John)
   * Fact 2 (BelievesFire(John) ∧ HasWater(John) → PutOutFire(John)): ¬BelievesFire(John) ∨ ¬HasWater(John) ∨ PutOutFire(John)
   * Fact 3 (SeesSmoke(John) → HasWater(John)): ¬SeesSmoke(John) ∨ HasWater(John)
   * Fact 4 (John sees smoke): SeesSmoke(John)
   * Fact 5 (Fire → Smoke): ¬Fire ∨ Smoke
3. **Set up the resolution process**:
   * We have the following clauses:
     * Clause 1: ¬SeesSmoke(John) ∨ BelievesFire(John)
     * Clause 2: ¬BelievesFire(John) ∨ ¬HasWater(John) ∨ PutOutFire(John)
     * Clause 3: ¬SeesSmoke(John) ∨ HasWater(John)
     * Clause 4: SeesSmoke(John)
     * Clause 5: ¬Fire ∨ Smoke
4. **Apply resolution steps**:
   * Step 1: Resolve Clause 1 (¬SeesSmoke(John) ∨ BelievesFire(John)) with Clause 4 (SeesSmoke(John)):
     * This gives BelievesFire(John).
   * Step 2: Resolve Clause 3 (¬SeesSmoke(John) ∨ HasWater(John)) with Clause 4 (SeesSmoke(John)):
     * This gives HasWater(John).
   * Step 3: Now that we have BelievesFire(John) and HasWater(John), we can resolve with Clause 2 (¬BelievesFire(John) ∨ ¬HasWater(John) ∨ PutOutFire(John)):
     * This gives PutOutFire(John).
5. **Conclusion**:
   * The resolution process yields PutOutFire(John), meaning we have proven that if John sees smoke and has water, he will put out the fire.

</details>
