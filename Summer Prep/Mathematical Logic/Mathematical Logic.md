## Mathematical Logic

In this chapter, we cover some of the foundational logical concepts that underlie mathematical reasoning.

### Mathematical statements

A mathematical statement is the most basic unit of meaning in mathematical reasoning every definition, theorem, and proof relies on mathematical statements.
	Mathematical statements are built from atomic statements, called basic propositions, which express elementary claims such as
$$
"x>0"\qquad"\text{3 is a prime number}"\qquad f(x)=0
$$
More complex statements are formed by combining basic propositions using a small collection of logical connectives—such as conjunctions, disjunctions, implications, equivalences (if and only ifs), and negations—as well as quantifiers such as "for all" and "there exists".

-----

- **Definition 1.1**
  A proposition is the simplest kind of mathematical statement and expresses a single, indivisible claim which can be understood on its own.

  - **Example 1.1.1**
    $$
    "\text{7 is a prime number}"\qquad"2x+3y>0"\qquad "f(x)=7"
    $$
    As we will see, the first logical connective that lets us combine basic propositions into more complex mathematical statements is called a conjunction. In everyday language, a conjunction corresponds to the word "and".

  - **Example 1.1.2**
    From the propositions "$0<i$" and "$i<n$", we can form the more complex mathematical statement "$0<i\  \text{and}\ i<n$", commonly rephrased as "$0<i<n$". 

Precisely, while the first proposition asserts that $i$ is greater than $0$ and the second proposition asserts that $n$ is greater than $i$, the conjunction tells us that the value of $i$ is in the open interval $(0,n)$.

- **Remark 1.1**
  Once we know how to combine two basic propositions using a conjunction, we can extend this idea to build even richer expressions. 
  - **Example 1.1.3**
    Consider the propositions "$0<i, i<n$" and "$i\text{ is even}$". We can form the first conjunction "$0<i<n$" and then combine this new statement with "$i\text{ is even}$" to obtain "$0<i<n$ and $i\text{ is even}$". This final conjunction tells us that $i$ is an even number in the open interval $(0,n)$.

-----

- **Definition 1.2**
  Suppose that $P$ and $Q$ represent formed mathematical statements. A conjunction is a new mathematical statement of the form $P \land Q$, where $\land$ is the symbol we use for the word "$\text{and}$". For example

  - **Example 1.2.1**
    Using the formal language, consider again the propositions "$0<i,i<n$" and "$i\text{ is even}$", then we can use the conjunction to obtain
    $$
    \left(0<i<n\right) \land \left(i\text{ is even}\right)
    $$
    

------

The second logical connective that allows us to combine mathematical statements is called disjunction. In everyday language, the disjunction corresponds to the word "$\text{or}$".

- **Definition 1.3**
  Suppose that $P$ and $Q$ represent formed mathematical statements. A disjunction is a new mathematical statement of the form $P \lor Q$, where $\lor$ is the symbol we use for the word "$\text{or}$". 

  - **Example 1.3.1**
    Consider the basic propositions "$0=i$" and "$0<i$" that we can form the disjunction $(0=i)\lor(0<i)$ commonly expressed as $0\leq i$.

  - **Example 1.3.2**
    Consider the propositions "$\sqrt 2^{\sqrt2}\text{ is irrational}$" and "$\sqrt2^{\sqrt2^{\sqrt2}}\text{ is irrational}$" then we can form the disjunction

  $$
  \left(\sqrt 2^{\sqrt2}\text{ is irrational}\right)\lor\left(\sqrt2^{\sqrt2^{\sqrt2}}\text{ is irrational}\right)
  $$

  - **Example 1.3.3**
    Consider the basic propositions "$0=i$" , "$0<i$" and "$i<n$" then we can form first the disjunction $(0=i)\lor(0<i)$, that is, $0\leq i$ and then we can form the conjunction $(0\leq i)\land(i<n)$, that is, $0\leq i<n$.

-----

The third logical connective that allows us to combine and form new mathematical statements is called implication. In everyday language, an implication corresponds to the word "$\text{implies}$".

- **Definition 1.4**
  Suppose that $P$ and $Q$ represent formed mathematical statements. An implication is a new mathematical statement of the form $P\Rightarrow Q$, where $\Rightarrow$ is the symbol we use for the word "$\text{implies}$".
  The statement $P$ is called antecedent and the statement $Q$ is called consequent.
  
  - **Example 1.4.1**
    Consider the propositions "$n\text{ is even}$" and "$n+1\text{ is odd}$" then we can form the new statement "$n\text{ is even implies } n+1\text{ is odd}$", the antecedent is the proposition "$n\text{ is even}$" and the consequent is the proposition "$n+1\text{ is odd}$".
    $$
    (n\text{ is even})\Rightarrow(n+1\text{ is odd})
    $$
  
  - **Example 1.4.2**
  
    Consider the propositions "$f\text{ is differentiable}$" and "$f\text{ is continuous}$", we can form the new proposition "$f\text{ is differentiable implies }f\text{ is continuous}$". The antecedent is the proposition "$f\text{ is differentiable}$" and the consequent is "$f\text{ is continuous}$". Using the formal language
    $$
    f\text{ is differentiable}\Rightarrow f\text{ is continuous}
    $$
    
  
- **Remark 1.4**
  Implications are often expressed in several equivalent ways.

  - **Example 1.4.3**
    $$
    f\text{ is differentiable implies }f\text{ is continuous}
    $$
    can be written as
    $$
    \text{if }f\text{ is differentiable, then }f\text{ is continuous}\\ f\text{ is continuous if }f\text{ is differentiable}\\ f\text{ is continuous whenever }f\text{ is differentiable}
    $$

These different formulations don't change the logical structure, that is, it is always clear which is the antecedent and which is the consequent.

-----

The fourth logical connective that allows us to combine and form new mathematical statements is the equivalence.

- **Definition 1.5**
  Suppose that $P$ and $Q$ represent formed mathematical statements. We combine the logical connectives "$\Rightarrow$" and "$\land$" as
  $$
  (P\Rightarrow Q)\land(Q\Rightarrow P)
  $$
  to obtain a new mathematical statement called equivalence of the form $P\Leftrightarrow Q$, where $\Leftrightarrow$ is the symbol we use for the phrase "$\text{if and only if}$". 

  - **Example 1.5.1**
    Consider the propositions "$\left\lvert x\right\rvert\leq 3$" and "$-3\leq x\leq 3$" then we can form the new mathematical statement "$\left\lvert x\right\rvert\leq 3\text{ if and only if }-3\leq x\leq 3$" and using the formal language
    $$
    \left\lvert x\right\rvert\leq 3\Leftrightarrow -3\leq x\leq 3
    $$

-----

To complete the set of basic logical connectives, we introduce negations. In everyday language a negation corresponds to the word "$\text{not}$".

- **Definition 1.6**
  Suppose that $P$ represents a formed mathematical statement. The negation of $P$ is the new mathematical statement of the form $\neg P$, where $\neg$ is the symbol we use for the word "$\text{not}$". 
  - **Example 1.6.1**
    Consider the proposition "$0=i$", then we can form the negation $\neg(0=i)$, commonly written $0\neq i$.

We will introduce two logical constants verum (truth) and falsum (falsehood), these constants represent statements that are universally true, such as $0=0$ and statements that are inherently contradictory such as $0=1$.

------

- **Definition 1.7**
  The symbol $\top$, called verum, stands for an arbitrary universal mathematical truth. The symbol $\bot$, called falsum, stands for an arbitrary universal mathematical falsehood.
  The logical language developed so far does not allow us to speak about objects or collections of objects. 
  - **Example 1.7.1** 
    "$\text{all squares are positive}$" or "$\text{there exists a function that is differentiable and not continuous}$".

-----

Our language must be extended and this extension is achieved by introducing two logical operators, the quantifiers $\forall$ and $\exists$ , "$\text{for all}$" and "$\text{there exists}$".

- **Definition 1.8**
  Suppose that $P(x)$ is a formed mathematical statement about some variable $x$.
  The universal quantification of $P(x)$ is a new mathematical statement of the form $\forall xP(x)$, where $\forall$ is the symbol we use for "$\text{for all}$".
  The existential quantification of $P(x)$ is a new mathematical statement of the form $\exists xP(x)$, where $\exists$ is the symbol we use for "$\text{there exists}$". 

  - **Example 1.8.1**
    The statement "$\text{there exists a function }f\text{ that is differentiable and not continuous}$" can be written using the formal language
    $$
    \exists f\left(\left(f\text{ is differentiable}\right)\land \neg \left(f\text{ is continuous}\right)\right)
    $$

  - **Example 1.8.2**
    The statement "$\text{for all functions }f,\text{if } f\text{ is differentiable then }f\text{ is continuous}$" can be written as
    $$
    \forall f\left(\left(\text{if }f\text{ is differentiable}\right)\Rightarrow \left(f\text{ is continuous}\right)\right)
    $$


-----

### Truth values

The truth value of a mathematical statement is not determined in isolation, but always relative to a universe of discourse or context, in which the statement is interpreted. For example, consider the statement 
$$
\forall x,y\exists z\left((x\neq y)\Rightarrow (x<z<y)\right)
$$
which may be read as 

$$
\text{"For any two distinct numbers }x,y\text{, there exists a number }z\text{ strictly between them."}
$$

Note that if the statement is interpreted in the context of natural numbers, it is false because there is no natural number between $1$ and $2$. But if the statement is interpreted in the context of rational numbers, it is true because for any two rational numbers $x,y$, the number $z=\dfrac{x+y}{2}$ is a rational number between them.

---

- **Definition 2.1**  
  Let $P$ and $Q$ be mathematical statements interpreted in some context $u$, the truth value of $P\land Q$ in such a context is fully determined by the following truth table:
  $$
  \begin{array}{c|c|c}  P&Q&P\land Q \\  1&1&1 \\ 1&0&0 \\ 0&1&0 \\ 0&0&0  \end{array}
  $$

- **Remark 2.1**  
  The truth table for conjunction can be understood in an even more compact way as follows:

  - **Example 2.1.1**  
    If $\left[P\right]$ is the truth value of $P$ and $\left[Q\right]$ is the truth value of $Q$, then

    $$
    \left[P\land Q\right]=\min\left(\left[P\right],\left[Q\right]\right)
    $$

    This algebraic perspective is useful for replacing structural properties of logical connectives.

---

- **Definition 2.2**  
  Let $P$ and $Q$ be mathematical statements interpreted in some context $u$, the truth value of $P\lor Q$ in such a context is fully determined by the following truth table:
  $$
  \begin{array}{c|c|c}  P&Q&P\lor Q \\  1&1&1 \\ 1&0&1 \\ 0&1&1 \\ 0&0&0  \end{array}
  $$

- **Remark 2.2**  
  The truth table for disjunction can be understood in an even more compact way as follows:

  - **Example 2.2.1**  
    If $\left[P\right]$ is the truth value of $P$ and $\left[Q\right]$ is the truth value of $Q$, then

    $$
    \left[P\lor Q\right]=\max\left(\left[P\right],\left[Q\right]\right)
    $$

---

- **Definition 2.3**  
  Let $P$ and $Q$ be mathematical statements interpreted in some context $u$, the truth value of $P\Rightarrow Q$ in such a context is fully determined by the following truth table:
  $$
  \begin{array}{c|c|c}  P&Q&P\Rightarrow Q \\  1&1&1 \\ 1&0&0 \\ 0&1&1 \\ 0&0&1  \end{array}
  $$

- **Remark 2.3**  
  In algebraic form, the truth table can be understood in an even more compact way as follows:

  - **Example 2.3.1**  
    If $\left[P\right]$ is the truth value of $P$ and $\left[Q\right]$ is the truth value of $Q$, then

    $$
    \left[P\Rightarrow Q\right]=\begin{cases} \left[Q\right]\quad&\text{if } \left[P\right]=1 \\ 1 &\text{otherwise} \end{cases}
    $$

    or in another form:

    $$
    \left[P\Rightarrow Q\right]=\max\left(1-\left[P\right],\left[Q\right]\right)
    $$

---

- **Definition 2.4**  
  Let $P$ and $Q$ be mathematical statements interpreted in some context $u$, the truth value of $P\Leftrightarrow Q$ in such a context is fully determined by the following truth table:

  $$
  \begin{array}{c|c|c}  P&Q&P\Leftrightarrow Q \\  1&1&1 \\ 1&0&0 \\ 0&1&0 \\ 0&0&1  \end{array}
  $$

- **Remark 2.4**  
  In algebraic form, the truth table can be understood in an even more compact way as follows:

  - **Example 2.4.1**  
    If $\left[P\right]$ is the truth value of $P$ and $\left[Q\right]$ is the truth value of $Q$, then

    $$
    \left[P\Leftrightarrow Q\right]=\min\left(1-\left[P\right]+\left[Q\right],1-\left[Q\right]+\left[P\right]\right)
    $$

---

- **Definition 2.5**  
  Let $P$ be a mathematical statement interpreted in some context $u$, the truth value of $\neg P$ in such a context is fully determined by the following truth table:

  $$
  \begin{array}{c|c}  P&\neg P \\  1&0 \\ 0&1  \end{array}
  $$

- **Remark 2.5**  
  In algebraic form, the truth table can be understood in an even more compact way as follows:

  - **Example 2.5.1**  
    If $\left[P\right]$ is the truth value of $P$, then

    $$
    \left[\neg P\right]=1-\left[P\right]
    $$

---

We now turn to the question of how truth values are assigned to statements involving quantifiers.

- **Definition 2.6**  
  A universally quantified statement of the form $\forall xP(x)$ is true if and only if $P(x)$ is true for all possible values of $x$. Note that the universally quantified statement $\forall xP(x)$ is false if $P(x)$ is false for some value of $x$.  
  An existentially quantified statement of the form $\exists xP(x)$ is true if $P(x)$ is true for some value of $x$. Note that the existentially quantified statement $\exists xP(x)$ is false if $P(x)$ is false for all possible values of $x$.

- **Remark 2.6**  
  In algebraic form, the truth values of the quantifiers $\forall xP(x)$ and $\exists xP(x)$ in a context $u$ are:

  - **Example 2.6.1**  

    $$
    \left[\forall xP(x)\right]=\min_{x \text;{ takes a value in } u}(\left[P(x)\right])
    $$

    $$
    \left[\exists xP(x)\right]=\max_{x \text;{ takes a value in } u}(\left[P(x)\right])
    $$

---

- **Definition 2.7**  
  We say that two mathematical statements $P$ and $Q$ are logically equivalent, denoted by $P\equiv Q$, if for any context $u$ we obtain $\left[P\right]=\left[Q\right]$.

  - **Example 2.7.1**  
    Let $P$ and $Q$ be two mathematical statements, then $\neg\left(P\land Q\right)\equiv\left(\neg P \lor \neg Q\right)$.

    $$
    \begin{array}{c|c|c|c|c|c|c} P&Q&P\land Q&\neg\left(P\land Q\right)&\neg P&\neg Q&\left(\neg P \lor \neg Q\right) \\ 1&1&1&0&0&0&0 \\ 1&0&0&1&0&1&1 \\ 0&1&0&1&1&0&1 \\ 0&0&0&1&1&1&1 \end{array}
    $$

    Therefore, $\neg\left(P\land Q\right)\equiv\left(\neg P \lor \neg Q\right)$.

  - **Example 2.7.2**  
    Let $P$ and $Q$ be two mathematical statements, then $\neg\left(P\Rightarrow Q\right)\equiv P \land \neg Q$.
    $$
    \begin{array}{c|c|c|c|c|c} P&Q&P\Rightarrow Q&\neg\left(P\Rightarrow Q\right)&\neg Q&\left(P \land \neg Q\right) \\ 1&1&1&0&0&0 \\ 1&0&0&1&1&1 \\ 0&1&1&0&0&0 \\ 0&0&1&0&1&0 \end{array}
    $$

    Therefore, $\neg\left(P\Rightarrow Q\right)\equiv P \land \neg Q$.

  - **Example 2.7.3**  
    Determine if $\forall xP(x)\equiv\neg\exists x\left(\neg P(x)\right)$.

    - **Solution 2.7.3.1**
      We consider two possible cases for the truth value of $\forall xP(x)$ in any given context $u$:

      **Case 1:** If $\forall xP(x)$ is true, then $\left[\forall xP(x)\right]=1$. This implies that $[P(x)]=1$ for all $x$ in $u$. Consequently, the truth value of its negation is $\left[\neg P(x)\right]=1-[P(x)]=0$ for all $x$ in $u$. Taking the maximum over all $x$, we get:
      $$
      \left[\exists x(\neg P(x))\right]=\max_{x}(\left[\neg P(x)\right])=0
      $$

      Thus, its negation evaluates to:

      $$
      \left[\neg\exists x\left(\neg P(x)\right)\right]=1-0=1
      $$

      **Case 2:** If $\forall xP(x)$ is false, then $\left[\forall xP(x)\right]=0$. This implies that there exists at least one element $x_0$ in $u$ such that $\left[P\left(x_0\right)\right]=0$. For this specific element, we have $\left[\neg P\left(x_0\right)\right]=1-\left[P\left(x_0\right)\right]=1$. Since there is at least one element where $\neg P(x)$ is true, taking the maximum yields:
      $$
      \left[\exists x(\neg P(x))\right]=\max_{x}(\left[\neg P(x)\right])=1
      $$

      Thus, its negation evaluates to:

      $$
      \left[\neg\exists x\left(\neg P(x)\right)\right]=1-1=0
      $$

      In both cases, we obtain:

      $$
      \left[\forall xP(x)\right]=\left[\neg\exists x\left(\neg P(x)\right)\right]
      $$

      By Definition 2.7, we conclude that $\forall xP(x)\equiv\neg\exists x\left(\neg P(x)\right)$.

  - **Example 2.7.4**
    Let $P,Q$ and $R$ be three mathematical statements, we want to prove that the propositions
    $$
    \begin{aligned}
    
    &A:P\Rightarrow \left(Q\Rightarrow R\right)\\
    &B:\left(P\and Q\right)\Rightarrow R
    
    \end{aligned}
    $$
    are equivalent. 

    - **Solution 2.7.4.1**
      We have

    $$
    \begin{array}{c|c|c|c|c|c|c}
    
    P&Q&R&Q\Rightarrow R&P\and Q&P\Rightarrow \left(Q\Rightarrow R\right)&\left(P\and Q\right)\Rightarrow R \\
    1&1&1&1&1&1&1 \\
    1&1&0&0&1&0&0 \\
    1&0&1&1&0&1&1 \\
    1&0&0&1&0&1&1 \\
    0&1&1&1&0&1&1 \\
    0&1&0&0&0&1&1 \\
    0&0&1&1&0&1&1 \\
    0&0&0&1&0&1&1
    
    \end{array}
    $$

    Therefore, $A\equiv B$.

  - **Example 2.7.5**
    Let $P,Q$ and $R$ be three mathematical statements, we want to prove that the propositions
    $$
    \begin{aligned}
    
    &A:\left(P\Rightarrow Q\right)\and\left(Q\Rightarrow R\right)\\
    &B:\left(\neg P\or Q\right)\and\left(Q \or R\right)
    
    \end{aligned}
    $$
    are equivalent.

    - **Solution 2.7.5.1**
      **Case 1**: $A$ is false if and only if
      $$
      (P\Rightarrow Q)\text{ is false or } (\neg Q\Rightarrow R)\text{ is false}
      $$
      which means
      $$
      \begin{pmatrix}
      P\text{ is true}\\
      \text{and} \\
      Q\text{ is false}
      \end{pmatrix} \text{or}
      
      \begin{pmatrix}
      Q\text{ is false}\\
      \text{and} \\
      R\text{ is false}
      \end{pmatrix}
      $$
      **Case 2**: $B$ is false if and only if
      $$
      \left(\neg P\or Q\right)\text{ is false or }\left(Q \or R\right)\text{ is false}
      $$
      which means
      $$
      \begin{pmatrix}
      P\text{ is true}\\
      \text{and} \\
      Q\text{ is false}
      \end{pmatrix} \text{or}
      
      \begin{pmatrix}
      Q\text{ is false}\\
      \text{and} \\
      R\text{ is false}
      \end{pmatrix}
      $$
      In conclusion, both propositions are false exactly in the same cases.
      Therefore, $A\equiv B$.

  - **Example 2.7.6**
    Let $P,Q$ and $R$ be three mathematical statements, we want to prove that the propositions
    $$
    \begin{aligned}
    
    &A:P\Rightarrow(Q\Rightarrow R) \\
    &B:(P\Rightarrow Q)\Rightarrow R
    
    \end{aligned}
    $$
    are not equivalent.

    - **Solution 2.7.6.1**
      if $P$ is false, $Q$ is true and $R$ is false, then the proposition $A$ is true and the proposition $B$ is false, then $A,B$ are not equivalent.

  - **Example 2.7.7**
    Are $A:\neg(P\and Q),B:\neg P\and \neg Q$ are equivalent?

    - **Solution 2.7.7.1**
      If $P$ is true and $Q$ is false, then $A$ is true and $B$ is false, then $A,B$ are not equivalent.

  - **Example 2.7.8**
    Are $A:(P\Rightarrow Q)\and R,B:P\Rightarrow(Q\and R)$ are equivalent?

    - **Solution 2.7.8.1**
      If $P$ is false, then $B$ is always true. In this case, if $R$ is false, $A$ is false, then $A,B$ are not equivalent.