---
description: Convert First Order Logic to Conjuctive Normal Form
---

# FOL to CNF

### Question 1:

Convert the following sentence into First-Order Logic and then into CNF: _"John is a person."_

<details>

<summary>Click to reveal the answer</summary>

**FOL**: Person(John)

**CNF**: Person(John) (Already in CNF as a single literal)

</details>

***

### Question 2:

Convert the following sentence into First-Order Logic and then into CNF: _"Sally is a student."_

<details>

<summary>Click to reveal the answer</summary>

**FOL**: Student(Sally)

**CNF**: Student(Sally) (Already in CNF as a single literal)

</details>

***

### Question 3:

Convert the following sentence into First-Order Logic and then into CNF: _"Tom likes ice cream."_

<details>

<summary>Click to reveal the answer</summary>

**FOL**: Likes(Tom, IceCream)

**CNF**: Likes(Tom, IceCream) (Already in CNF as a single literal)

</details>

***

### Question 4:

Convert the following sentence into First-Order Logic and then into CNF: _"Every cat is an animal."_

<details>

<summary>Click to reveal the answer</summary>

**FOL**: ∀x (Cat(x) → Animal(x))

**CNF**: ∀x (¬Cat(x) ∨ Animal(x)) (Apply the implication elimination rule: A → B = ¬A ∨ B)

</details>

***

### Question 5:

Convert the following sentence into First-Order Logic and then into CNF: _"There is a dog."_

<details>

<summary>Click to reveal the answer</summary>

**FOL**: ∃x (Dog(x))

**CNF**: ∃x (Dog(x)) (Already in CNF as a single existential quantifier with a literal)

</details>

***

### Question 6:

Convert the following sentence into First-Order Logic and then into CNF: _"Alice knows Bob."_

<details>

<summary>Click to reveal the answer</summary>

**FOL**: Knows(Alice, Bob)

**CNF**: Knows(Alice, Bob) (Already in CNF as a single literal)

</details>

***

### Question 7:

Convert the following sentence into First-Order Logic and then into CNF: _"All students attend school."_

<details>

<summary>Click to reveal the answer</summary>

**FOL**: ∀x (Student(x) → AttendsSchool(x))

**CNF**: ∀x (¬Student(x) ∨ AttendsSchool(x)) (Apply the implication elimination rule: A → B = ¬A ∨ B)

</details>

***

### Question 8:

Convert the following sentence into First-Order Logic and then into CNF: _"There is a book on the table."_

<details>

<summary>Click to reveal the answer</summary>

**FOL**: ∃x (Book(x) ∧ OnTable(x))

**CNF**: ∃x (Book(x) ∧ OnTable(x)) (Already in CNF as a conjunction of literals)

</details>

***

### Question 9:

Convert the following sentence into First-Order Logic and then into CNF: _"Bob is older than Alice."_

<details>

<summary>Click to reveal the answer</summary>

**FOL**: OlderThan(Bob, Alice)

**CNF**: OlderThan(Bob, Alice) (Already in CNF as a single literal)

</details>

***

### Question 10:

Convert the following sentence into First-Order Logic and then into CNF: _"Some birds can sing."_

<details>

<summary>Click to reveal the answer</summary>

**FOL**: ∃x (Bird(x) ∧ CanSing(x))

**CNF**: ∃x (Bird(x) ∧ CanSing(x)) (Already in CNF as a conjunction of literals)

</details>

### Question 11:

Convert the following sentence into First-Order Logic and then into CNF: _"All dogs are mammals."_

<details>

<summary>Click to reveal the answer</summary>

**FOL**: ∀x (Dog(x) → Mammal(x))

**CNF**: ∀x (¬Dog(x) ∨ Mammal(x)) (Apply the implication elimination rule: A → B = ¬A ∨ B)

</details>

***

### Question 12:

Convert the following sentence into First-Order Logic and then into CNF: _"There exists a student who has a pet dog."_

<details>

<summary>Click to reveal the answer</summary>

**FOL**: ∃x (Student(x) ∧ ∃y (Dog(y) ∧ Pet(x, y)))

**CNF**: ∃x (Student(x) ∧ ∃y (Dog(y) ∧ Pet(x, y))) (Already in CNF as a conjunction of literals)

</details>

***

### Question 13:

Convert the following sentence into First-Order Logic and then into CNF: _"No cats are dogs."_

<details>

<summary>Click to reveal the answer</summary>

**FOL**: ∀x (Cat(x) → ¬∃y (Dog(y) ∧ Same(x, y)))

**CNF**: ∀x (¬Cat(x) ∨ ¬∃y (Dog(y) ∧ Same(x, y)))\
∀x (¬Cat(x) ∨ ¬Dog(x)) (Remove the existential quantifier by standard CNF transformation)

</details>

***

### Question 14:

Convert the following sentence into First-Order Logic and then into CNF: _"Every human has a mother."_

<details>

<summary>Click to reveal the answer</summary>

**FOL**: ∀x (Human(x) → ∃y (Mother(y) ∧ Parent(y, x)))

**CNF**: ∀x (¬Human(x) ∨ ∃y (Mother(y) ∧ Parent(y, x)))\
∀x ∀y (¬Human(x) ∨ Mother(y) ∨ Parent(y, x)) (Skolemization and CNF conversion)

</details>

***

### Question 15:

Convert the following sentence into First-Order Logic and then into CNF: _"If it is raining, then the ground is wet."_

<details>

<summary>Click to reveal the answer</summary>

**FOL**: ∀x (Raining(x) → Wet(Ground))

**CNF**: ∀x (¬Raining(x) ∨ Wet(Ground)) (Apply the implication elimination rule: A → B = ¬A ∨ B)

</details>

***

### Question 16:

Convert the following sentence into First-Order Logic and then into CNF: _"John loves Mary and Mary loves John."_

<details>

<summary>Click to reveal the answer</summary>

**FOL**: Loves(John, Mary) ∧ Loves(Mary, John)

**CNF**: Loves(John, Mary) ∧ Loves(Mary, John) (Already in CNF as a conjunction of literals)

</details>

***

### Question 17:

Convert the following sentence into First-Order Logic and then into CNF: _"There is no student who is both a teacher and a student."_

<details>

<summary>Click to reveal the answer</summary>

**FOL**: ¬∃x (Student(x) ∧ Teacher(x))

**CNF**: ∀x (¬Student(x) ∨ ¬Teacher(x)) (Apply negation and convert to CNF)

</details>

***

### Question 18:

Convert the following sentence into First-Order Logic and then into CNF: _"Some birds can fly, but not all birds can fly."_

<details>

<summary>Click to reveal the answer</summary>

**FOL**: ∃x (Bird(x) ∧ CanFly(x)) ∧ ∃x (Bird(x) ∧ ¬CanFly(x))

**CNF**: ∃x (Bird(x) ∧ CanFly(x)) ∧ ∃x (Bird(x) ∧ ¬CanFly(x)) (Already in CNF as a conjunction of literals)

</details>

***

### Question 19:

Convert the following sentence into First-Order Logic and then into CNF: _"All people who study mathematics are good at logic."_

<details>

<summary>Click to reveal the answer</summary>

**FOL**: ∀x (Student(x) ∧ StudiesMath(x) → GoodAtLogic(x))

**CNF**: ∀x (¬Student(x) ∨ ¬StudiesMath(x) ∨ GoodAtLogic(x)) (Apply the implication elimination rule: A → B = ¬A ∨ B)

</details>

***

### Question 20:

Convert the following sentence into First-Order Logic and then into CNF: _"There is at least one person who knows everyone."_

<details>

<summary>Click to reveal the answer</summary>

**FOL**: ∃x (Person(x) ∧ ∀y (Person(y) → Knows(x, y)))

**CNF**: ∃x (Person(x) ∧ ∀y (¬Person(y) ∨ Knows(x, y)))\
∃x ∀y (Person(x) ∧ (¬Person(y) ∨ Knows(x, y))) (Apply CNF transformation)

</details>
