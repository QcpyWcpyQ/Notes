## Sets

- **Exercise 1**
  Suppose $A,B,D\subseteq X$. Prove the following properties

  1. $\left(A\setminus B\right)^\complement=A^\complement\cup B$.
     **Proof**
     $$
     \begin{aligned}
     x\in\left(A\setminus B\right)^\complement&\iff x\not\in\left(A\setminus B\right)\iff\text{It is false that } x\in A\setminus B \\
     &\iff\text{It is false that }x\in A\land x\not\in B \\
     &\iff\text{It is true that }\neg(x\in A\land x\not\in B)\\
     &\iff x\not\in A\lor x\in B\iff x\not\in A\text{ or } x\in B \\
     &\iff x\in A^\complement\cup B
     \end{aligned}
     $$
     Thus $\left(A\setminus B\right)^\complement=A^\complement\cup B$.

  2. $A\cap\left(B\setminus D\right)=\left(A\cap B\right)\setminus\left(A\cap D\right)$.
     **Proof**
     $$
     \begin{aligned}
     x\in A\cap\left(B\setminus D\right)&\iff x\in A \land x\in B\setminus D \\
     &\iff x\in A \land x\in B\land x\not\in D \\
     &\iff \left(x\in A \land x \in B\right)\land\left(x\in A\land x\not\in D\right) \\
     &\iff x\in A\cap B\land x\not\in A\cap D \\
     &\iff x\in\left(A\cap B\right)\setminus\left(A\cap D\right)
     \end{aligned}
     $$
     Thus $A\cap\left(B\setminus D\right)=\left(A\cap B\right)\setminus\left(A\cap D\right)$.

- **Exercise 2**
  Let $A$ and $B$ be two sets. Prove that $\mathscr P(A)\cup \mathscr P(B)\subseteq\mathscr P(A\cup B)$.

  - **Proof 2.1**
    Suppose
    $$
    \begin{aligned}
    X\in\mathscr P(A)\cup \mathscr P(B)&\implies X\in\mathscr P(A)\text{ or }X\in \mathscr P(B) \\
    &\iff X\subseteq A\text{ or }X\subseteq B \\
    &\implies X\subseteq A\subseteq A\cup B \text{ or }X\subseteq B\subseteq A\cup B \\
    &\implies \text{In any case, } X\subseteq A\cup B \\
    &\implies X\in\mathscr P(A\cup B)
    \end{aligned}
    $$
    Thus $\mathscr P(A)\cup \mathscr P(B)\subseteq\mathscr P(A\cup B)$.

- **Exercise 3**  
  Suppose $A_n = \left[-\dfrac{1}{n}, 1 + \dfrac{1}{n}\right]$ for $n \in \mathbb{N}$, find $\bigcup\limits_{n\in\mathbb{N}} A_n$, $\bigcap\limits_{n\in\mathbb{N}} A_n$, $\bigcup\limits_{n\in\mathbb{N}} A_n^\complement$, and $\bigcap\limits_{n\in\mathbb{N}} A_n^\complement$.  

  - **Solution 3.1**  
    As $n$ increases, the intervals $A_n$ become nested, meaning $A_1 \supseteq A_2 \supseteq A_3 \supseteq \dots$  
    For $n=1$, we have $A_1 = [-1, 2]$.  

    The **union** is equal to the largest interval
    $$
    \bigcup_{n\in\mathbb{N}} A_n = [-1, 2]
    $$
    The **intersection** approaches the limit points $0$ and $1$ from the outside, including them
    $$
    \bigcap_{n\in\mathbb{N}} A_n = [0, 1]
    $$
    By **De Morgan's laws**, the union of the complements is the complement of the intersection
    $$
    \bigcup_{n\in\mathbb{N}} A_n^\complement = \left(\bigcap_{n\in\mathbb{N}} A_n\right)^\complement = (-\infty, 0) \cup (1, \infty)
    $$
    Similarly, the intersection of the complements is the complement of the union
    $$
    \bigcap_{n\in\mathbb{N}} A_n^\complement = \left(\bigcup_{n\in\mathbb{N}} A_n\right)^\complement = (-\infty, -1) \cup (2, \infty)
    $$
