---
description: Convert English to First Order Logic
---

# English to FOL

### Question 1

Convert the following sentence into First-Order Logic: _"John is a person."_

<details>

<summary>Click to reveal the answer</summary>

Answer: Person(John)

</details>

***

### Question 2

Convert the following sentence into First-Order Logic: _"Sally is a student."_

<details>

<summary>Click to reveal the answer</summary>

Answer: Student(Sally)

</details>

***

### Question 3

Convert the following sentence into First-Order Logic: _"Tom likes ice cream."_

<details>

<summary>Click to reveal the answer</summary>

Answer: Likes(Tom, IceCream)

</details>

***

### Question 4

Convert the following sentence into First-Order Logic: _"Every cat is an animal."_

<details>

<summary>Click to reveal the answer</summary>

Answer: ∀x (Cat(x) → Animal(x))

</details>

***

### Question 5

Convert the following sentence into First-Order Logic: _"There is a dog."_

<details>

<summary>Click to reveal the answer</summary>

Answer: ∃x (Dog(x))

</details>

***

### Question 6

Convert the following sentence into First-Order Logic: _"Alice knows Bob."_

<details>

<summary>Click to reveal the answer</summary>

Answer: Knows(Alice, Bob)

</details>

***

### Question 7

Convert the following sentence into First-Order Logic: _"All students attend school."_

<details>

<summary>Click to reveal the answer</summary>

Answer: ∀x (Student(x) → AttendsSchool(x))

</details>

***

### Question 8

Convert the following sentence into First-Order Logic: _"There is a book on the table."_

<details>

<summary>Click to reveal the answer</summary>

Answer: ∃x (Book(x) ∧ OnTable(x))

</details>

***

### Question 9

Convert the following sentence into First-Order Logic: _"Bob is older than Alice."_

<details>

<summary>Click to reveal the answer</summary>

Answer: OlderThan(Bob, Alice)

</details>

***

### Question 10

Convert the following sentence into First-Order Logic: _"Some birds can sing."_

<details>

<summary>Click to reveal the answer</summary>

Answer: ∃x (Bird(x) ∧ CanSing(x))

</details>

### Question 11

Convert the following sentence into First-Order Logic: _"All dogs are mammals."_

<details>

<summary>Click to reveal the answer</summary>

Answer: ∀x (Dog(x) → Mammal(x))

</details>

***

### Question 12

Convert the following sentence into First-Order Logic: _"There exists a student who has a pet dog."_

<details>

<summary>Click to reveal the answer</summary>

Answer: ∃x (Student(x) ∧ ∃y (Dog(y) ∧ Pet(x, y)))

</details>

***

### Question 13

Convert the following sentence into First-Order Logic: _"No cats are dogs."_

<details>

<summary>Click to reveal the answer</summary>

Answer: ∀x (Cat(x) → ¬∃y (Dog(y) ∧ Same(x, y)))

</details>

***

### Question 14

Convert the following sentence into First-Order Logic: _"Every human has a mother."_

<details>

<summary>Click to reveal the answer</summary>

Answer: ∀x (Human(x) → ∃y (Mother(y) ∧ Parent(y, x)))

</details>

***

### Question 15

Convert the following sentence into First-Order Logic: _"If it is raining, then the ground is wet."_

<details>

<summary>Click to reveal the answer</summary>

Answer: ∀x (Raining(x) → Wet(Ground))

</details>

***

### Question 16

Convert the following sentence into First-Order Logic: _"John loves Mary and Mary loves John."_

<details>

<summary>Click to reveal the answer</summary>

Answer: Loves(John, Mary) ∧ Loves(Mary, John)

</details>

***

### Question 17

Convert the following sentence into First-Order Logic: _"There is no student who is both a teacher and a student."_

<details>

<summary>Click to reveal the answer</summary>

Answer: ¬∃x (Student(x) ∧ Teacher(x))

</details>

***

### Question 18

Convert the following sentence into First-Order Logic: _"Some birds can fly, but not all birds can fly."_

<details>

<summary>Click to reveal the answer</summary>

Answer: ∃x (Bird(x) ∧ CanFly(x)) ∧ ∃x (Bird(x) ∧ ¬CanFly(x))

</details>

***

### Question 19

Convert the following sentence into First-Order Logic: _"All people who study mathematics are good at logic."_

<details>

<summary>Click to reveal the answer</summary>

Answer: ∀x (Student(x) ∧ StudiesMath(x) → GoodAtLogic(x))

</details>

***

### Question 20

Convert the following sentence into First-Order Logic: _"There is at least one person who knows everyone."_

<details>

<summary>Click to reveal the answer</summary>

Answer: ∃x (Person(x) ∧ ∀y (Person(y) → Knows(x, y)))

</details>
