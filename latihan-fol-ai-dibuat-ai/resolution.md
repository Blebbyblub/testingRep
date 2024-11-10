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



### Question:

Use resolution to prove or disprove the statement: \
_"Bob is successful"_\
\
Assume the following facts are given:

1. All students who study hard pass their exams.
2. Every student who passes their exams is happy.
3. Everyone who is happy has a good life.
4. Alice is a student.
5. Bob is a student and he studies hard.
6. If a person has a good life, they are successful.
7. Alice does not study hard.

<details>

<summary>Click to reveal the answer</summary>

### Answers:

#### 1. Translate each statement to First-Order Logic (FOL)

1. All students who study hard pass their exams.\
   $$\forall x (Student(x) \land StudyHard(x) \rightarrow PassExam(x))$$
2. Every student who passes their exams is happy.\
   $$\forall x (Student(x) \land PassExam(x) \rightarrow Happy(x))$$
3. Everyone who is happy has a good life.\
   $$\forall x (Happy(x) \rightarrow GoodLife(x))$$
4. Alice is a student.\
   $$Student(Alice)$$
5. Bob is a student and he studies hard.\
   $$Student(Bob) \land StudyHard(Bob)$$
6. If a person has a good life, they are successful.\
   $$\forall x (GoodLife(x) \rightarrow Successful(x))$$
7. Alice does not study hard.\
   $$eg StudyHard(Alice)$$

#### 2. Convert the FOL statements to Conjunctive Normal Form (CNF)

1. $$\forall x (Student(x) \land StudyHard(x) \rightarrow PassExam(x))$$\
   **CNF:**\
   $$eg Student(x) \lor \neg StudyHard(x) \lor PassExam(x)$$
2. $$\forall x (Student(x) \land PassExam(x) \rightarrow Happy(x))$$\
   **CNF:**\
   $$eg Student(x) \lor \neg PassExam(x) \lor Happy(x)$$
3. $$\forall x (Happy(x) \rightarrow GoodLife(x))$$\
   **CNF:**\
   $$eg Happy(x) \lor GoodLife(x)$$
4. $$Student(Alice)$$\
   **CNF:**\
   $$Student(Alice)$$
5. $$Student(Bob) \land StudyHard(Bob)$$\
   **CNF:**\
   $$Student(Bob), \quad StudyHard(Bob)$$
6. $$\forall x (GoodLife(x) \rightarrow Successful(x))$$\
   **CNF:**\
   $$eg GoodLife(x) \lor Successful(x)$$
7. $$eg StudyHard(Alice)$$\
   **CNF:**\
   $$eg StudyHard(Alice)$$

#### 3. Prove using Resolution that Bob is successful

To prove $$Successful(Bob)$$ using resolution, we use the derived CNF statements.

1. **Given Clauses**:
   * $$eg Student(x) \lor \neg StudyHard(x) \lor PassExam(x)$$ — Clause 1
   * $$eg Student(x) \lor \neg PassExam(x) \lor Happy(x)$$ — Clause 2
   * $$eg Happy(x) \lor GoodLife(x)$$ — Clause 3
   * $$Student(Alice)$$ — Clause 4
   * $$Student(Bob)$$ — Clause 5a
   * $$StudyHard(Bob)$$ — Clause 5b
   * $$eg GoodLife(x) \lor Successful(x)$$ — Clause 6
   * $$eg StudyHard(Alice)$$ — Clause 7
2. **Resolution Proof**:
   * From Clause 5a ($$Student(Bob)$$) and Clause 5b ($$StudyHard(Bob)$$), we know $$Student(Bob) \land StudyHard(Bob)$$.
   * Substitute $$x = Bob$$ in Clause 1: $$eg Student(Bob) \lor \neg StudyHard(Bob) \lor PassExam(Bob)$$, and with $$Student(Bob)$$ and $$StudyHard(Bob)$$, we resolve to $$PassExam(Bob)$$.
   * Substitute $$x = Bob$$ in Clause 2: $$eg Student(Bob) \lor \neg PassExam(Bob) \lor Happy(Bob)$$, and with $$Student(Bob)$$ and $$PassExam(Bob)$$, we resolve to $$Happy(Bob)$$.
   * Substitute $$x = Bob$$ in Clause 3: $$eg Happy(Bob) \lor GoodLife(Bob)$$, and with $$Happy(Bob)$$, we resolve to $$GoodLife(Bob)$$.
   * Substitute $$x = Bob$$ in Clause 6: $$eg GoodLife(Bob) \lor Successful(Bob)$$, and with $$GoodLife(Bob)$$, we resolve to $$Successful(Bob)$$.
3. **Conclusion**:
   * We have proven that $$Successful(Bob)$$ holds true using resolution.

</details>
