## Week 2

- **Problem 1**
  Draw a Venn diagram for three sets $X, Y, Z$ to represent each expression:
  (a) $(X \setminus Y) \cup Z$
  (b) $(X \cap Y)^\complement \setminus Z$

  - **Solution 1.1**
    Skip.

---

- **Problem 2**
  Let $M = \{4, \{5\}, \{4, 5\}\}$. Determine which of the following assertions are correct.
  (a) $5 \in M$
  (c) $\{5\} \subseteq M$
  (b) $(A \setminus B)^\complement = A^\complement \cup B$
  (f) $A \subseteq B \iff A \cap B = A$
  (g) $A \cup (A \cap B) = A$
  (j) $A \cap (B \setminus D) = (A \cap B) \setminus (A \cap D)$
  (e) $\{4, 5\} \in M$
  (g) $\{\{4, 5\}\} \in M$
  (i) $\varnothing \in M$
  (k) $M \in M$

  - **Solution 2.1**
    * **(a) Incorrect.** The number $5$ is not a direct element of $M$; the set $\{5\}$ is.
    * **(c) Incorrect.** For $\{5\} \subseteq M$ to be true, $5 \in M$ must hold, which is false.
    * **(b) Correct.** By definition, 
      $$
      \begin{aligned}
      x \in (A \setminus B)^\complement &\iff x \notin A \setminus B\\
      &\iff \neg(x \in A \land x \notin B) \\
      &\iff x \notin A \lor x \in B \\
      &\iff x \in A^\complement \lor x \in B \\
      &\iff x \in A^\complement \cup B
      
      \end{aligned}
      $$
    * **(f) Correct.** 
      $(\Longrightarrow)$ If $A \subseteq B$, then for any $x \in A$, $x \in B$ must hold. Thus $x \in A \implies x \in A \land x \in B \implies x \in A \cap B$, showing $A \subseteq A \cap B$. Since $A \cap B \subseteq A$ always holds by definition, $A \cap B = A$.
      $(\Longleftarrow)$ If $A \cap B = A$, then for any $x \in A$, we have $x \in A \cap B$, which means $x \in B$ by definition of intersection. Thus $A \subseteq B$.
    * **(g) Correct.** By definition, $x \in A \cup (A \cap B) \iff x \in A \lor (x \in A \land x \in B) \iff x \in A$ .
    * **(j) Correct.** By definition:
      $$
      x \in A \cap (B \setminus D) \iff x \in A \land (x \in B \land x \notin D) \iff (x \in A \land x \in B) \land x \notin D
      $$
      On the other side:
      $$
      x \in (A \cap B) \setminus (A \cap D) \iff (x \in A \land x \in B) \land \neg(x \in A \land x \in D) \iff (x \in A \land x \in B) \land (x \notin A \lor x \notin D)
      $$
      Since $x \in A$ is already true from the first part, $x \notin A$ is false, so $(x \notin A \lor x \notin D)$ simplifies directly to $x \notin D$. Thus, both sides mean $(x \in A \land x \in B) \land x \notin D$.
    * **(e) Correct.** The set $\{4, 5\}$ is explicitly listed as the third element of $M$.
    * **(g) Incorrect.** The nested set $\{\{4, 5\}\}$ is not an element belonging to $M$.
    * **(i) Incorrect.** The empty set $\varnothing$ is not explicitly listed inside $M$.
    * **(k) Incorrect.** By the Axiom of Regularity, no set can contain itself as an element.

---

- **Problem 3**
  Suppose $A, B, D \subseteq U$. Prove the following properties.
  (a) $A \cap (A \cup B) = A$
  (c) $A \setminus (B \cup D) = (A \setminus B) \cap (A \setminus D)$
  (d) $(A \cap B)^\complement = A^\complement \cup B^\complement$
  (e) $A \subseteq B \iff A \cup B = B$
  (h) $(A \cup B)^\complement = A^\complement \cap B^\complement$
  (i) $(A \setminus B) \cup (A \cap B) = A$

  - **Solution 3.1**
    * **(a) Proof:**
      We prove this by showing $x \in A \cap (A \cup B) \iff x \in A$:
      $$
      x \in A \cap (A \cup B) \iff x \in A \land (x \in A \lor x \in B) \iff x \in A
      $$
      
    * **(c) Proof:**
      We use the element-hood definition to show logical equivalence:
      $$
      \begin{aligned}
      x \in A \setminus (B \cup D) &\iff x \in A \land x \notin (B \cup D) \\
      &\iff x \in A \land \neg(x \in B \lor x \in D) \\
      &\iff x \in A \land (x \notin B \land x \notin D) \\
      &\iff (x \in A \land x \notin B) \land (x \in A \land x \notin D)  \\
      &\iff x \in (A \setminus B) \land x \in (A \setminus D) \\
      &\iff x \in (A \setminus B) \cap (A \setminus D)
      \end{aligned}
      $$
      
    * **(d) Proof:**
      By definition of the complement and logical negation:
      $$
      \begin{aligned}
      
      x \in (A \cap B)^\complement &\iff x \notin A \cap B \\
      &\iff \neg(x \in A \land x \in B) \\
      &\iff x \notin A \lor x \notin B \\
      &\iff x \in A^\complement \lor x \in B^\complement \\
      &\iff x \in A^\complement \cup B^\complement
      
      \end{aligned}
      $$
      
    * **(e) Proof:**
      $(\Longrightarrow)$ Assume $A \subseteq B$, meaning if $x \in A$ then $x \in B$. We show $A \cup B = B$:
      
      * If $x \in A \cup B$, then $x \in A$ or $x \in B$. If $x \in A$, then $x \in B$ by assumption. Thus $x \in B$ in both cases, which means $A \cup B \subseteq B$.
      * If $x \in B$, then $x \in A \lor x \in B$ is automatically true, so $x \in A \cup B$, meaning $B \subseteq A \cup B$. Thus, $A \cup B = B$.
      
      $(\Longleftarrow)$ Assume $A \cup B = B$. Let $x \in A$. Then $x \in A \lor x \in B$ is true, so $x \in A \cup B$. Since $A \cup B = B$, it follows that $x \in B$. Hence, $A \subseteq B$.
      
    * **(h) Proof:**
      By definition of the complement and logical negation:
      $$
      \begin{aligned}
      
      x \in (A \cup B)^\complement &\iff x \notin A \cup B \\
      &\iff \neg(x \in A \lor x \in B) \\
      &\iff x \notin A \land x \notin B \\
      &\iff x \in A^\complement \land x \in B^\complement \\
      &\iff x \in A^\complement \cap B^\complement
      
      \end{aligned}
      $$
      
    * **(i) Proof:**
      We use the element-hood definition to show logical equivalence:
      $$
      \begin{aligned}
      x \in (A \setminus B) \cup (A \cap B) &\iff x \in (A \setminus B) \lor x \in (A \cap B) \\
      &\iff (x \in A \land x \notin B) \lor (x \in A \land x \in B) \\
      &\iff x \in A \land (x \notin B \lor x \in B)\\
      &\iff x \in A \land \text{True} \\
      &\iff x \in A
      \end{aligned}
      $$

---

- **Problem 4**
  Let $A, B, C$ be subsets of a universal set $X$. Prove the implication: If $A \cap B \subseteq C$ and $C \subseteq A \cup B$, then $C \setminus A \subseteq B$.

  - **Solution 4.1**
    **Proof:**
    Let $x \in C \setminus A$. By definition of set difference, this means:
    $$
    x \in C \quad \text{and} \quad x \notin A
    $$
    We are given the condition $C \subseteq A \cup B$. Since $x \in C$, it must follow by definition of subset that:
    $$
    x \in A \cup B
    $$
    By definition of union, this means $x \in A$ or $x \in B$.  
    However, we already established from the definition of $C \setminus A$ that $x \notin A$.  
    Therefore, for the disjunction $(x \in A \lor x \in B)$ to hold true while $x \in A$ is false, $x \in B$ must be true.
    
    Since any arbitrary element $x \in C \setminus A$ satisfies $x \in B$, we conclude by definition of subset that:
    $$
    C \setminus A \subseteq B
    $$
    The proof is complete.

---

- **Problem 5**
  Let $A, B$ be arbitrary sets. Prove or disprove: $\mathscr{P}(A \setminus B) = \mathscr{P}(A) \setminus \mathscr{P}(B)$. If false, provide an explicit counterexample.

  - **Solution 5.1**
    The statement is **false**.
    
    **Counterexample:**
    Let $A = \{1\}$ and $B = \{2\}$.  
    Then, the set difference is $A \setminus B = \{1\}$.  
    The power sets of these collections are:
    $$
    \mathscr{P}(A \setminus B) = \{\varnothing, \{1\}\}
    $$
    $$
    \mathscr{P}(A) = \{\varnothing, \{1\}\}, \quad \mathscr{P}(B) = \{\varnothing, \{2\}\}
    $$
    Evaluating the right side of the proposed equation yields:
    $$
    \mathscr{P}(A) \setminus \mathscr{P}(B) = \{\{1\}\}
    $$
    Since $\{\varnothing, \{1\}\} \neq \{\{1\}\}$, the statement does not hold in general.

---

- **Problem 6**
  Let $A, B \subseteq X$. Prove that $A \subseteq B$ if and only if for every set $C$, $A \cap C \subseteq B \cap C$.

  - **Solution 6.1**
    **Proof:**
    $(\Longrightarrow)$ Assume $A \subseteq B$. Let $C$ be any arbitrary set, and let $x \in A \cap C$. By definition of intersection, this means:
    $$
    x \in A \quad \text{and} \quad x \in C
    $$
    Since $A \subseteq B$, by definition of subset, $x \in A \implies x \in B$. Therefore, we have:
    $$
    x \in B \quad \text{and} \quad x \in C
    $$
    By definition of intersection, $x \in B \cap C$. Since any arbitrary element $x \in A \cap C$ satisfies $x \in B \cap C$, we conclude that $A \cap C \subseteq B \cap C$.

    $(\Longleftarrow)$ Assume that for every set $C$, $A \cap C \subseteq B \cap C$ holds. We need to show $A \subseteq B$.
    Let $x$ be an arbitrary element such that $x \in A$. 
    Since the given hypothesis holds true for any choice of set $C$, we can choose $C$ to be the singleton set containing only $x$, that is, $C = \{x\}$.
    Now evaluate the intersection $A \cap \{x\}$: since $x \in A$ and $x \in \{x\}$, we have:
    $$
    x \in A \cap \{x\}
    $$
    By our hypothesis, $A \cap \{x\} \subseteq B \cap \{x\}$, which implies:
    $$
    x \in B \cap \{x\}
    $$
    By definition of intersection, this means $x \in B$ and $x \in \{x\}$. In particular, we obtain:
    $$
    x \in B
    $$
    Since $x \in A \implies x \in B$ for any arbitrary element, we conclude by definition of subset that $A \subseteq B$.
    The proof is complete.

---

- **Problem 7**
  Let $U$ be a universal set, and let $A, B \subseteq U$. Prove or disprove: $(A \cup B)^\complement = A^\complement \cup B^\complement$. If the statement is false, give a counterexample.

  - **Solution 7.1**
    The statement is **false**.
    
    **Counterexample:**
    Let the universal set be $U = \{1, 2\}$, and let $A = \{1\}$ and $B = \{2\}$.  
    First, find the union of $A$ and $B$:
    $$
    A \cup B = \{1, 2\}
    $$
    By definition of complement, the left-hand side is:
    $$
    (A \cup B)^\complement = U \setminus \{1, 2\} = \varnothing
    $$
    Now, calculate the complements of $A$ and $B$ separately:
    $$
    A^\complement = \{2\}, \quad B^\complement = \{1\}
    $$
    Thus, the right-hand side is:
    $$
    A^\complement \cup B^\complement = \{1, 2\}
    $$
    Since $\varnothing \neq \{1, 2\}$, the statement does not hold.

---

- **Problem 8**
  Suppose $A \subseteq B \cup C$. Does it follow that $A \subseteq B$ or $A \subseteq C$? If not, construct a concrete counterexample.

  - **Solution 8.1**
    No, it **does not follow**.
    
    **Counterexample:**
    Let $A = \{1, 2\}$, $B = \{1\}$, and $C = \{2\}$.  
    First, evaluate the union of $B$ and $C$:
    $$
    B \cup C = \{1, 2\}
    $$
    Since every element of $A$ is in $B \cup C$, the condition $A \subseteq B \cup C$ is satisfied.  
    However, $A \nsubseteq B$ because $2 \in A$ but $2 \notin B$.  
    Similarly, $A \nsubseteq C$ because $1 \in A$ but $1 \notin C$.  
    Therefore, the implication is false.

---

- **Problem 9**
  Let $A, B, C \subseteq X$. Prove: $(A \setminus B) \setminus C = A \setminus (B \cup C)$.

  - **Solution 9.1**
    **Proof:**
    We show that an element $x$ belongs to the left-hand side if and only if it belongs to the right-hand side using basic definition of set-membership:
    $$
    \begin{aligned}
    x \in (A \setminus B) \setminus C &\iff x \in (A \setminus B) \land x \notin C \\
    &\iff (x \in A \land x \notin B) \land x \notin C \\
    &\iff x \in A \land (x \notin B \land x \notin C) \\
    &\iff x \in A \land \neg(x \in B \lor x \in C)\\
    &\iff x \in A \land x \notin (B \cup C) \\
    &\iff x \in A \setminus (B \cup C)
    \end{aligned}
    $$
    Since $x \in (A \setminus B) \setminus C \iff x \in A \setminus (B \cup C)$ is logically equivalent, the two sets are equal.

---

- **Problem 10**
  Let $A, B, C \subseteq X$. Show that $A \cap (B \Delta C) = (A \cap B) \Delta (A \cap C)$, where $\Delta$ denotes symmetric difference: $X \Delta Y = (X \setminus Y) \cup (Y \setminus X)$.

  - **Solution 10.1**
    **Proof:**
    By definition of symmetric difference, $B \Delta C = (B \setminus C) \cup (C \setminus B)$. We unpack the condition $x \in A \cap (B \Delta C)$ step by step:
    $$
    \begin{aligned}
    x \in A \cap (B \Delta C) &\iff x \in A \land x \in (B \Delta C) \\
    &\iff x \in A \land (x \in B \setminus C \lor x \in C \setminus B) \\
    &\iff x \in A \land ((x \in B \land x \notin C) \lor (x \in C \land x \notin B)) \\
    &\iff (x \in A \land x \in B \land x \notin C) \lor (x \in A \land x \in C \land x \notin B) 
    \end{aligned}
    $$
    Now, we unpack the right-hand side expression, $x \in (A \cap B) \Delta (A \cap C)$:
    $$
    \begin{aligned}
    x \in (A \cap B) \Delta (A \cap C) &\iff x \in ((A \cap B) \setminus (A \cap C)) \lor x \in ((A \cap C) \setminus (A \cap B)) \\
    &\iff (x \in A \cap B \land x \notin A \cap C) \lor (x \in A \cap C \land x \notin A \cap B) \\
    &\iff ((x \in A \land x \in B) \land \neg(x \in A \land x \in C)) \lor ((x \in A \land x \in C) \land \neg(x \in A \land x \in B)) \\
    &\iff ((x \in A \land x \in B) \land (x \notin A \lor x \notin C)) \lor ((x \in A \land x \in C) \land (x \notin A \lor x \notin B))
    \end{aligned}
    $$
    In the first component, since $x \in A$ is true, the statement $(x \notin A \lor x \notin C)$ simplifies directly to $x \notin C$.  
    In the second component, since $x \in A$ is true, the statement $(x \notin A \lor x \notin B)$ simplifies directly to $x \notin B$.  
    Substituting these simplifications back, we get:
    $$
    (x \in A \land x \in B \land x \notin C) \lor (x \in A \land x \in C \land x \notin B)
    $$
    Since both sides reduce to the exact same logical statement, $A \cap (B \Delta C) = (A \cap B) \Delta (A \cap C)$ is proven.

---

- **Problem 11**
  Another Morgan's Law (Indexed Families): Let $\{A_i\}_{i \in I}$ be a family of sets. Prove:
  $$
  \left(\bigcap_{i \in I} A_i\right)^\complement = \bigcup_{i \in I} A_i^\complement
  $$

  - **Solution 11.1**
    **Proof:**
    We apply the logical definitions of indexed intersection, union, and complement to show element-hood equivalence:
    $$
    \begin{aligned}
    x \in \left(\bigcap_{i \in I} A_i\right)^\complement &\iff x \notin \bigcap_{i \in I} A_i \\
    &\iff \neg \left( \forall i \in I, \, x \in A_i \right) \\
    &\iff \exists i \in I, \, \neg(x \in A_i) \\
    &\iff \exists i \in I, \, x \notin A_i \\
    &\iff \exists i \in I, \, x \in A_i^\complement \\
    &\iff x \in \bigcup_{i \in I} A_i^\complement
    \end{aligned}
    $$
    Since the logical statements match at every point, the set identity holds true.

---

- **Problem 12**
  Properties of a Relation
  Let
  $$
  A = \{1, 2, 3, 4\}
  $$
  and
  $$
  R = \{(1, 1), (2, 2), (3, 3), (4, 4), (1, 2), (2, 1)\}
  $$
  Determine whether $R$ is:
  (a) reflexive;
  (b) symmetric;
  (c) antisymmetric;
  (d) transitive.

  - **Solution 12.1**
    * **(a) Reflexive:** Yes. By definition, a relation $R$ on $A$ is reflexive if for every $x \in A$, $(x, x) \in R$. For $A = \{1, 2, 3, 4\}$, the pairs $(1, 1), (2, 2), (3, 3),$ and $(4, 4)$ are all explicitly present in $R$.
    * **(b) Symmetric:** Yes. By definition, a relation is symmetric if for any $x, y \in A$, $(x, y) \in R \implies (y, x) \in R$. The only distinct pairs in $R$ are $(1, 2)$ and $(2, 1)$. Since $(1, 2) \in R \implies (2, 1) \in R$ and $(2, 1) \in R \implies (1, 2) \in R$, the condition holds.
    * **(c) Antisymmetric:** No. By definition, a relation is antisymmetric if for any $x, y \in A$, $((x, y) \in R \land (y, x) \in R) \implies x = y$. In this relation, we have $(1, 2) \in R$ and $(2, 1) \in R$, but $1 \neq 2$.
    * **(d) Transitive:** Yes. By definition, a relation is transitive if for any $x, y, z \in A$, $((x, y) \in R \land (y, z) \in R) \implies (x, z) \in R$. Checking the non-trivial combinations:
      $$
      ((1, 2) \in R \land (2, 1) \in R) \implies (1, 1) \in R
      $$
      $$
      ((2, 1) \in R \land (1, 2) \in R) \implies (2, 2) \in R
      $$
      Any other compositions with diagonal relations automatically satisfy the implication.

---

- **Problem 13**
  Relations on Integers
  For each of the following relations on $\mathbb{Z}$, determine whether it is reflexive, symmetric, antisymmetric, and transitive. For every property that fails, give a counterexample.
  (a)
  $$
  a \sim b \iff a = b
  $$
  (b)
  $$
  a \sim b \iff a \leqslant b
  $$
  (c)
  $$
  a \sim b \iff |a - b| \leqslant 2
  $$

  - **Solution 13.1**
    **Part (a):**
    * **Reflexive:** Yes. For any integer $a \in \mathbb{Z}$, the statement $a = a$ is universally true. Therefore, $a \sim a$ holds for all $a \in \mathbb{Z}$.
    * **Symmetric:** Yes. Let $a, b \in \mathbb{Z}$ such that $a \sim b$. By definition, this means $a = b$. Since equality is symmetric, it follows that $b = a$, which means $b \sim a$.
    * **Antisymmetric:** Yes. Let $a, b \in \mathbb{Z}$ such that $a \sim b$ and $b \sim a$. By definition, this implies $a = b$ and $b = a$. This directly satisfies the requirement that $a = b$.
    * **Transitive:** Yes. Let $a, b, c \in \mathbb{Z}$ such that $a \sim b$ and $b \sim c$. By definition, this yields $a = b$ and $b = c$. Substituting $b$ gives $a = c$, which means $a \sim c$.

  - **Solution 13.2**
    **Part (b):**
    * **Reflexive:** Yes. For any integer $a \in \mathbb{Z}$, the statement $a \leqslant a$ is always true. Thus, $a \sim a$ holds for all $a \in \mathbb{Z}$.
    * **Symmetric:** No. Let $a = 1$ and $b = 2$. We have $1 \leqslant 2$, so $1 \sim 2$ is true. However, $2 \leqslant 1$ is false, so $2 \sim 1$ does not hold.
    * **Antisymmetric:** Yes. Let $a, b \in \mathbb{Z}$ such that $a \sim b$ and $b \sim a$. By definition, this means $a \leqslant b$ and $b \leqslant a$. By the properties of the standard order relation on integers, $a \leqslant b \land b \leqslant a \implies a = b$.
    * **Transitive:** Yes. Let $a, b, c \in \mathbb{Z}$ such that $a \sim b$ and $b \sim c$. By definition, this yields $a \leqslant b$ and $b \leqslant c$. By the transitivity property of inequalities, $a \leqslant b \land b \leqslant c \implies a \leqslant c$, which means $a \sim c$.

  - **Solution 13.3**
    **Part (c):**
    * **Reflexive:** Yes. For any integer $a \in \mathbb{Z}$, we have $|a - a| = |0| = 0$. Since $0 \leqslant 2$, the condition $|a - a| \leqslant 2$ is satisfied, so $a \sim a$ holds for all $a \in \mathbb{Z}$.
    * **Symmetric:** Yes. Let $a, b \in \mathbb{Z}$ such that $a \sim b$. By definition, $|a - b| \leqslant 2$. Since $|a - b| = |-(b - a)| = |b - a|$, we have $|b - a| \leqslant 2$, which means $b \sim a$.
    * **Antisymmetric:** No. Let $a = 1$ and $b = 2$. We have $|1 - 2| = |-1| = 1 \leqslant 2$, so $1 \sim 2$ holds. Similarly, $|2 - 1| = |1| = 1 \leqslant 2$, so $2 \sim 1$ holds. However, $1 \neq 2$.
    * **Transitive:** No. Let $a = 1$, $b = 3$, and $c = 5$. We have $|1 - 3| = |-2| = 2 \leqslant 2$, so $1 \sim 3$ holds. We also have $|3 - 5| = |-2| = 2 \leqslant 2$, so $3 \sim 5$ holds. However, for $a$ and $c$, we have $|1 - 5| = |-4| = 4 > 2$, which means $1 \sim 5$ does not hold.

---

- **Problem 14**
  An Equivalence Relation on Integers
  Define a relation $\sim$ on $\mathbb{Z}$ by
  $$
  a \sim b \iff a - b \text{ is divisible by } 4.
  $$
  (a) Prove that $\sim$ is an equivalence relation.
  (b) Find $[0]$, $[1]$, $[2]$, $[3]$, $[5]$.
  (c) How many distinct equivalence classes are there?

  - **Solution 14.1**
    **Part (a):**
    * **Reflexive:** Let $a \in \mathbb{Z}$. Then $a - a = 0$. Since $0 = 4 \times 0$, $0$ is divisible by $4$. Thus, $a \sim a$ for all $a \in \mathbb{Z}$.
    * **Symmetric:** Let $a, b \in \mathbb{Z}$ such that $a \sim b$. By definition, $a - b = 4k$ for some $k \in \mathbb{Z}$. Then $b - a = -(a - b) = -4k = 4(-k)$. Since $-k \in \mathbb{Z}$, $b - a$ is divisible by $4$, so $b \sim a$.
    * **Transitive:** Let $a, b, c \in \mathbb{Z}$ such that $a \sim b$ and $b \sim c$. By definition, $a - b = 4k$ and $b - c = 4m$ for some $k, m \in \mathbb{Z}$. Adding these equations gives $(a - b) + (b - c) = 4k + 4m \implies a - c = 4(k + m)$. Since $k + m \in \mathbb{Z}$, $a - c$ is divisible by $4$, so $a \sim c$.
    Since $\sim$ is reflexive, symmetric, and transitive, it is an equivalence relation.

  - **Solution 14.2**
    **Part (b):**
    By definition, $[a] = \{x \in \mathbb{Z} \mid x - a = 4k, k \in \mathbb{Z}\} = \{a + 4k \mid k \in \mathbb{Z}\}$.
    * $[0] = \{\dots, -8, -4, 0, 4, 8, \dots\} = \{4k \mid k \in \mathbb{Z}\}$
    * $[1] = \{\dots, -7, -3, 1, 5, 9, \dots\} = \{1 + 4k \mid k \in \mathbb{Z}\}$
    * $[2] = \{\dots, -6, -2, 2, 6, 10, \dots\} = \{2 + 4k \mid k \in \mathbb{Z}\}$
    * $[3] = \{\dots, -5, -1, 3, 7, 11, \dots\} = \{3 + 4k \mid k \in \mathbb{Z}\}$
    * $[5] = \{\dots, -3, 1, 5, 9, 13, \dots\} = [1]$

  - **Solution 14.3**
    **Part (c):**
    There are exactly $4$ distinct equivalence classes, which are $[0], [1], [2],$ and $[3]$.

---

- **Problem 15**
  Same Remainder
  Let
  $$
  A = \{0, 1, 2, 3, 4, 5, 6, 7\}.
  $$
  Define a relation $\sim$ on $A$ by
  $$
  a \sim b \iff a \text{ and } b \text{ have the same remainder when divided by } 3.
  $$
  (a) Write down all equivalence classes.
  (b) Write the relation $\sim$ explicitly as a set of ordered pairs.

  - **Solution 15.1**
    **Part (a):**
    We group the elements of $A$ by their remainder when divided by $3$:
    * Remainder $0$: $[0] = \{0, 3, 6\}$
    * Remainder $1$: $[1] = \{1, 4, 7\}$
    * Remainder $2$: $[2] = \{2, 5\}$

  - **Solution 15.2**
    **Part (b):**
    The relation $\sim$ consists of all pairs $(x, y)$ such that $x$ and $y$ belong to the same equivalence class:
    $$
    \begin{aligned}
    \sim = \{ &(0,0), (0,3), (0,6), (3,0), (3,3), (3,6), (6,0), (6,3), (6,6), \\
              &(1,1), (1,4), (1,7), (4,1), (4,4), (4,7), (7,1), (7,4), (7,7), \\
              &(2,2), (2,5), (5,2), (5,5) \}
    \end{aligned}
    $$

---

- **Problem 16**
  A Partial Order on Sets
  Let
  $$
  X = \{1, 2, 3\}.
  $$
  Consider the relation $\subseteq$ on $\mathscr{P}(X)$. Prove that $\subseteq$ is a partial order.

  - **Solution 16.1**
    **Proof:**
    * **Reflexive:** Let $A \in \mathscr{P}(X)$. For any $x \in A$, the statement $x \in A$ is true, so $A \subseteq A$ holds by definition of subset.
    * **Antisymmetric:** Let $A, B \in \mathscr{P}(X)$ such that $A \subseteq B$ and $B \subseteq A$. By definition of subset, $A \subseteq B \implies (\forall x \in A \implies x \in B)$ and $B \subseteq A \implies (\forall x \in B \implies x \in A)$. Thus $x \in A \iff x \in B$, which implies $A = B$.
    * **Transitive:** Let $A, B, C \in \mathscr{P}(X)$ such that $A \subseteq B$ and $B \subseteq C$. Let $x \in A$. Since $A \subseteq B$, it follows that $x \in B$. Since $B \subseteq C$ and $x \in B$, it follows that $x \in C$. Thus $x \in A \implies x \in C$, meaning $A \subseteq C$.
    Since $\subseteq$ is reflexive, antisymmetric, and transitive, it is a partial order.

---

- **Problem 17**
  Divisibility as a Partial Order
  Let $\mathbb{N}$ denote the set of positive integers. Define a relation $\preceq$ on $\mathbb{N}$ by
  $$
  x \preceq y \iff x \mid y.
  $$
  Recall that $x \mid y$ means that there exists $k \in \mathbb{N}$ such that $y = xk$. Prove that $\preceq$ is a partial order on $\mathbb{N}$.

  - **Solution 17.1**
    **Proof:**
  
    * **Reflexive:** Let $x \in \mathbb{N}$. We can write $x = x \times 1$. Since $1 \in \mathbb{N}$, there exists a positive integer $k=1$ such that $x = xk$, meaning $x \mid x$. Thus, $x \preceq x$.
  
    * **Antisymmetric:** Let $x, y \in \mathbb{N}$ such that $x \preceq y$ and $y \preceq x$. By definition, $y = xk$ and $x = ym$ for some $k, m \in \mathbb{N}$. Substituting $x$ into the first equation yields $y = (ym)k = y(mk)$. Dividing both sides by $y$ (since $y \ge 1$) gives $1 = mk$. Since $m, k$ are positive integers, the only solution is $m = 1$ and $k = 1$. Substituting $k = 1$ into $y = xk$ gives $y = x$.
  
    * **Transitive:** Let $x, y, z \in \mathbb{N}$ such that $x \preceq y$ and $y \preceq z$. By definition, $y = xk$ and $z = ym$ for some $k, m \in \mathbb{N}$. Substituting $y$ into the equation for $z$ gives $z = (xk)m = x(km)$. Since $k, m \in \mathbb{N}$, their product $km \in \mathbb{N}$. Thus, there exists an integer $k' = km$ such that $z = xk'$, meaning $x \mid z$, so $x \preceq z$.
  
      Since the relation $\preceq$ is reflexive, antisymmetric, and transitive, it is a partial order on $\mathbb{N}$.

---

- **Problem 18**
  Inverse Relation
  Let $\sim$ be a relation on a set $X$. The inverse relation $\sim^{-1}$ is defined by
  $$
  x \sim^{-1} y \iff y \sim x.
  $$
  Prove that $\sim$ is symmetric if and only if
  $$
  \sim \,=\, \sim^{-1}.
  $$

  - **Solution 18.1**
    **Proof:**
    $(\Longrightarrow)$ Assume $\sim$ is symmetric. We prove $\sim \,=\, \sim^{-1}$ by showing mutual inclusion:
    * Let $(x, y) \in \;\sim$, meaning $x \sim y$. Since $\sim$ is symmetric, we have $y \sim x$. By definition of the inverse relation, $y \sim x \iff x \sim^{-1} y$, which means $(x, y) \in \;\sim^{-1}$. Thus, $\sim \,\subseteq\, \sim^{-1}$.
    * Let $(x, y) \in \;\sim^{-1}$, meaning $x \sim^{-1} y$. By definition of the inverse relation, this means $y \sim x$. Since $\sim$ is symmetric, $y \sim x \implies x \sim y$, which means $(x, y) \in \;\sim$. Thus, $\sim^{-1} \,\subseteq\, \sim$.
    Therefore, $\sim \,=\, \sim^{-1}$.

    $(\Longleftarrow)$ Assume $\sim \,=\, \sim^{-1}$. To show $\sim$ is symmetric, let $x, y \in X$ such that $x \sim y$, which means $(x, y) \in \;\sim$.
    Since $\sim \,=\, \sim^{-1}$, it follows that $(x, y) \in \;\sim^{-1}$, meaning $x \sim^{-1} y$.
    By definition of the inverse relation, $x \sim^{-1} y \iff y \sim x$.
    Thus, $x \sim y \implies y \sim x$, proving that $\sim$ is symmetric.

---

- **Problem 19**
  Identity Relation and Antisymmetry
  Let $\sim_X$ be the identity relation on $X$, defined by
  $$
  x \sim_X y \iff x = y.
  $$
  Let $\sim$ be a relation on $X$, and let $\sim^{-1}$ denote its inverse relation. Prove that $\sim$ is antisymmetric if and only if
  $$
  \{(x, y) \in X \times X \mid x \sim y\} \cap \{(x, y) \in X \times X \mid x \sim^{-1} y\} \subseteq \{(x, y) \in X \times X \mid x \sim_X y\}.
  $$

  - **Solution 19.1**
    **Proof:**
    For simplicity, let $R = \{(x, y) \in X \times X \mid x \sim y\}$, $R^{-1} = \{(x, y) \in X \times X \mid x \sim^{-1} y\}$, and $I = \{(x, y) \in X \times X \mid x \sim_X y\}$.
    
    $(\Longrightarrow)$ Assume $\sim$ is antisymmetric. Let $(x, y) \in R \cap R^{-1}$.
    By definition of intersection, $(x, y) \in R$ and $(x, y) \in R^{-1}$.
    This means $x \sim y$ and $x \sim^{-1} y$.
    By definition of the inverse relation, $x \sim^{-1} y \iff y \sim x$.
    Since $\sim$ is antisymmetric, $x \sim y \land y \sim x \implies x = y$.
    By definition of the identity relation, $x = y \iff x \sim_X y \iff (x, y) \in I$.
    Thus, $R \cap R^{-1} \subseteq I$.

    $(\Longleftarrow)$ Assume $R \cap R^{-1} \subseteq I$. To prove $\sim$ is antisymmetric, let $x, y \in X$ such that $x \sim y$ and $y \sim x$.
    Since $x \sim y$, we have $(x, y) \in R$.
    Since $y \sim x$, by definition of the inverse relation, we have $x \sim^{-1} y$, which means $(x, y) \in R^{-1}$.
    Therefore, $(x, y) \in R \cap R^{-1}$.
    By our inclusion hypothesis, $(x, y) \in R \cap R^{-1} \implies (x, y) \in I$.
    By definition of $I$, $(x, y) \in I \iff x \sim_X y \iff x = y$.
    Thus, $x \sim y \land y \sim x \implies x = y$, proving that $\sim$ is antisymmetric.

---

- **Problem 20**
  Which Relations Define Functions?
  For each of the following relations $R \subseteq \mathbb{R} \times \mathbb{R}$, determine whether $R$ defines a function
  $$
  f \colon \mathbb{R} \rightarrow \mathbb{R}.
  $$
  Explain your answer.
  (a) $R = \{(x, y) \in \mathbb{R}^2 : y = x^2\}$.
  (b) $R = \{(x, y) \in \mathbb{R}^2 : y^2 = x\}$.
  (c) $R = \{(x, y) \in \mathbb{R}^2 : xy = 1\}$.
  (d) $R = \{(x, y) \in \mathbb{R}^2 : y^3 = x\}$.

  - **Solution 20.1**
    By definition, a relation $R \subseteq \mathbb{R} \times \mathbb{R}$ defines a function $f \colon \mathbb{R} \rightarrow \mathbb{R}$ if for every $x \in \mathbb{R}$, there exists a unique $y \in \mathbb{R}$ such that $(x, y) \in R$.
    * **(a) Yes.** For every $x \in \mathbb{R}$, the value $y = x^2$ is a uniquely determined real number.
    * **(b) No.** It fails on two conditions of the definition:
      * For $x = -1 \in \mathbb{R}$, there is no $y \in \mathbb{R}$ such that $y^2 = -1$.
      * For $x = 4 \in \mathbb{R}$, there is no unique $y$ because both $y = 2$ and $y = -2$ satisfy $y^2 = 4$.
    * **(c) No.** For $x = 0 \in \mathbb{R}$, there is no $y \in \mathbb{R}$ such that $0 \cdot y = 1$. Thus, $f(0)$ is undefined, so it cannot be a function from the entire domain $\mathbb{R}$.
    * **(d) Yes.** For every $x \in \mathbb{R}$, every real number has a unique real cube root, so $y = \sqrt[3]{x}$ exists and is uniquely determined for all $x$.

---

- **Problem 21**
  Natural Domains and Ranges
  Verify the natural domains and corresponding ranges of the following functions. The domain in each case consists of all values of $x$ for which the formula is well-defined.
  $$
  \begin{array}{c|c|c}
  \text{Function} & \text{Domain} & \text{Range} \\ \hline
  y = x^2 & (-\infty, \infty) & [0, \infty) \\
  y = \frac{1}{x} & (-\infty, 0) \cup (0, \infty) & (-\infty, 0) \cup (0, \infty) \\
  y = \sqrt{x} & [0, \infty) & [0, \infty) \\
  y = \sqrt{4 - x} & (-\infty, 4] & [0, \infty) \\
  y = \sqrt{1 - x^2} & [-1, 1] & [0, 1]
  \end{array}
  $$

  - **Solution 21.1**
    * **For $y = x^2$:**
      * **Domain:** The expression $x^2$ is defined for all real numbers, so the domain is $(-\infty, \infty)$.
      * **Range:** Since the square of any real number is non-negative, $x^2 \ge 0$, and for any $y \ge 0$, $x = \sqrt{y}$ exists. Thus, the range is $[0, \infty)$.
    * **For $y = \frac{1}{x}$:**
      * **Domain:** The expression is well-defined as long as the denominator is non-zero, so $x \neq 0$, which gives $(-\infty, 0) \cup (0, \infty)$.
      * **Range:** Since $y = \frac{1}{x}$, $y$ can never be $0$. For any $y \neq 0$, we can choose $x = \frac{1}{y}$, so the range is $(-\infty, 0) \cup (0, \infty)$.
    * **For $y = \sqrt{x}$:**
      * **Domain:** The square root is defined for non-negative real numbers, so $x \ge 0$, giving the domain $[0, \infty)$.
      * **Range:** The principal square root function always yields non-negative values, so $y \ge 0$, and for any $y \ge 0$, $x = y^2$ is in the domain. Thus, the range is $[0, \infty)$.
    * **For $y = \sqrt{4 - x}$:**
      * **Domain:** We require $4 - x \ge 0 \iff x \le 4$, which gives the interval $(-\infty, 4]$.
      * **Range:** The square root outputs non-negative values, $y \ge 0$. For any $y \ge 0$, setting $y = \sqrt{4-x} \iff y^2 = 4 - x \iff x = 4 - y^2$, which is always $\le 4$. Thus, the range is $[0, \infty)$.
    * **For $y = \sqrt{1 - x^2}$:**
      * **Domain:** We require $1 - x^2 \ge 0 \iff x^2 \le 1 \iff -1 \le x \le 1$, which gives the interval $[-1, 1]$.
      * **Range:** Since $-1 \le x \le 1$, we have $0 \le x^2 \le 1$, which implies $0 \le 1 - x^2 \le 1$. Taking the square root gives $0 \le y \le 1$. For any $y \in [0, 1]$, $x = \sqrt{1-y^2}$ is a valid domain element. Thus, the range is $[0, 1]$.

---

- **Problem 22**
  Domain, Codomain, and Image
  Let
  $$
  f \colon \mathbb{Z} \rightarrow \mathbb{Z}, \quad f(n) = 2n.
  $$
  Determine:
  (a) the domain of $f$;
  (b) the codomain of $f$;
  (c) the image of $f$.
  Is the image equal to the codomain?

  - **Solution 22.1**
    * **(a) Domain of $f$:**
      By definition, for a function written as $f \colon A \rightarrow B$, the set $A$ is the domain. Therefore, the domain of $f$ is $\mathbb{Z}$ (the set of all integers).
    * **(b) Codomain of $f$:**
      By definition, for a function written as $f \colon A \rightarrow B$, the set $B$ is the codomain. Therefore, the codomain of $f$ is $\mathbb{Z}$ (the set of all integers).
    * **(c) Image of $f$:**
      The image of $f$ is the set of all outputs generated by the function:
      $$
      \text{Image}(f) = \{f(n) \mid n \in \mathbb{Z}\} = \{2n \mid n \in \mathbb{Z}\}
      $$
      This is the set of all even integers, which can be written as $2\mathbb{Z} = \{\dots, -4, -2, 0, 2, 4, \dots\}$.
    * **Is the image equal to the codomain?**
      No. The image is the set of even integers $2\mathbb{Z}$, while the codomain is the set of all integers $\mathbb{Z}$. Since there are odd integers in the codomain (such as $1 \in \mathbb{Z}$) that do not belong to the image ($1 \notin 2\mathbb{Z}$), the image is a proper subset of the codomain, meaning they are not equal.

---

- **Problem 24**
  Identity and Inclusion
  Let
  $$
  A = \{1, 2, 3\}, \quad B = \{1, 2, 3, 4\}.
  $$
  Define
  $$
  \text{id}_A \colon A \rightarrow A, \quad \text{id}_A(x) = x,
  $$
  and the inclusion map
  $$
  \iota \colon A \rightarrow B, \quad \iota(x) = x.
  $$
  (a) Find all values of $\text{id}_A$ and $\iota$.
  (b) Do the two functions have the same rule?
  (c) Are they equal as functions? Explain.

  - **Solution 24.1**
    * **(a)** By evaluating each element of the domain $A = \{1, 2, 3\}$ under their respective definitions:
      $$
      \text{id}_A(1) = 1, \quad \text{id}_A(2) = 2, \quad \text{id}_A(3) = 3
      $$
      $$
      \iota(1) = 1, \quad \iota(2) = 2, \quad \iota(3) = 3
      $$
    * **(b) Yes.** Both functions have the exact same assignment rule, which maps any input element $x$ directly to itself without alteration.
    * **(c) No.** By definition, two functions are equal if and only if their domains, codomains, and rules are all identical. Here, the codomain of $\text{id}_A$ is $A = \{1, 2, 3\}$, whereas the codomain of $\iota$ is $B = \{1, 2, 3, 4\}$. Since their codomains are not the same set ($A \neq B$), they are not equal as functions.

---

- **Problem 25**
  Restriction of a Function
  Let
  $$
  f \colon \mathbb{R} \rightarrow \mathbb{R}, \quad f(x) = x^2 - 1.
  $$
  Let
  $$
  A = [-1, 1]
  $$
  and define
  $$
  g = f|_A.
  $$
  (a) Write the domain and codomain of $g$.
  (b) Find $g(-1)$, $g(0)$, $g(1)$.
  (c) Are $f$ and $g$ equal?
  (d) Do they have the same formula?

  - **Solution 25.1**
    * **(a)** By definition of a function restriction, restricting a function $f \colon X \rightarrow Y$ to a subset $A \subseteq X$ means the new function has domain $A$ while retaining the original rule and codomain. Therefore:
      * Domain of $g$ is $A = [-1, 1]$.
      * Codomain of $g$ is $\mathbb{R}$.
    * **(b)** Since $g(x) = f(x)$ for all $x \in A$, we substitute the values into the formula $x^2 - 1$:
      $$
      g(-1) = (-1)^2 - 1 = 1 - 1 = 0
      $$
      $$
      g(0) = (0)^2 - 1 = 0 - 1 = -1
      $$
      $$
      g(1) = (1)^2 - 1 = 1 - 1 = 0
      $$
    * **(c) No.** By definition, two functions are equal if and only if they share the exact same domain, codomain, and assignment rule. Here, the domain of $f$ is $\mathbb{R}$ while the domain of $g$ is $[-1, 1]$. Since their domains are different ($\mathbb{R} \neq [-1, 1]$), the functions are not equal.
    * **(d) Yes.** Both functions use the exact same algebraic formula $x^2 - 1$ to compute outputs from inputs, although $g$ is only allowed to apply this formula to elements within the restricted set $A$.

---

- **Problem 26**
  Construct Your Own Relation
  Let
  $$
  A = \{1, 2, 3, 4\}.
  $$
  Construct:
  (a) a relation that is reflexive but not symmetric;
  (b) a relation that is symmetric but not reflexive;
  (c) an equivalence relation with exactly two equivalence classes;
  (d) a partial order different from the equality relation.

  - **Solution 26.1**
    * **(a)** To be reflexive, the relation must contain $(1,1), (2,2), (3,3),$ and $(4,4)$. To violate symmetry, we add a directional pair without its inverse, such as $(1,2)$ without $(2,1)$:
      $$
      R = \{(1, 1), (2, 2), (3, 3), (4, 4), (1, 2)\}
      $$
    * **(b)** To violate reflexivity, at least one diagonal element must be missing (e.g., $(1,1) \notin R$). To maintain symmetry, any ordered pair must have its coordinates flipped within the set:
      $$
      R = \{(1, 2), (2, 1)\}
      $$
    * **(c)** To form an equivalence relation with exactly two classes, we can partition $A$ into two disjoint non-empty subsets, for instance, $A_1 = \{1, 2\}$ and $A_2 = \{3, 4\}$. The relation is constructed by taking $(A_1 \times A_1) \cup (A_2 \times A_2)$:
      $$
      R = \{(1, 1), (1, 2), (2, 1), (2, 2), (3, 3), (3, 4), (4, 3), (4, 4)\}
      $$
      Explicitly rewritten for verification:
      $$
      R = \{(1, 1), (1, 2), (2, 1), (2, 2), (3, 3), (3, 4), (4, 3), (4, 4)\}
      $$
    * **(d)** A partial order must be reflexive, antisymmetric, and transitive. The standard total order relation "less than or equal to" on integers satisfies this. Restricting it to $A$ yields:
      $$
      R = \{(1, 1), (2, 2), (3, 3), (4, 4), (1, 2), (1, 3), (1, 4), (2, 3), (2, 4), (3, 4)\}
      $$
      This relation is distinctly different from the pure equality relation because it contains pairs where $x \neq y$ (such as $(1,2)$).