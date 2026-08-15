## Proofs

Proofs are the primary means by which mathematical truth is established. The purpose of a proof is to justify the truth of a mathematical statement (called the **conclusion**) by considering other mathematical statements (called **premises**). Once a statement is proved, we refer to it as a **theorem**.

---

- **Definition 1: Conjunctions ($P \land Q$)**  
  A statement of the form $P \land Q$ is true when both $P$ and $Q$ are true. To prove a conjunction, it suffices to prove each of its component statements separately. That is, if we establish $P$ and we also establish $Q$, we may conclude $P \land Q$.   
  - **Example 1.1**  
    To prove that a number $n$ is even and greater than $10$, we prove separately that $n$ is an even number and that $n > 10$. Combining them yields the result.

---

- **Definition 2: Disjunctions ($P \lor Q$)**  
  A statement of the form $P \lor Q$ is true whenever at least one of its components is true. Therefore, to prove a disjunction, it is enough to prove one of its disjuncts (though a false disjunct cannot establish the disjunction).    
  - **Example 2.1**  
    To prove that a number $n$ is either even or odd, it suffices to prove that $n$ is even, and the disjunction follows.    
  - **Example 2.2**  
    Let $a, b \in \mathbb{R}$ that satisfy $a+b=10$. Prove that $ab\leq 25$ or $a^2+b^2<10$.      
    - **Solution 2.2.1**  
      Suppose $a, b \in \mathbb{R}$ satisfy $a+b=10$, then $a=10-b$, and we have       
      $$
      \begin{aligned}       
      ab &= (10-b)b \\       
      &= 10b-b^2 \\       
      &= -(b^2-10b) \\       
      &= -(b^2-10b+25)+25 \\       
      &= -(b-5)^2+25 \\       
      &\leq 25       
      \end{aligned}       
      $$
      So $ab\leq 25$, then $ab\leq 25$ or $a^2+b^2<10$.    
  - **Example 2.3**  
    Prove that $\left(\forall x\right)P(x) \lor \left(\forall x\right)Q(x)\implies \left(\forall x\right)\left( P(x)\lor Q(x)\right)$ and refute the converse implication.      
    - **Solution 2.3.1**  
      Suppose $(\forall x)P(x) \lor (\forall x) Q(x)$ is true, then $(\forall x)P(x)$ is true or $(\forall x)Q(x)$ is true.       
      Suppose $(\forall x)P(x)$ is true, then $\forall x, P(x)$ is true, then $\forall x, P(x)\lor Q(x)$ is true and then $\forall x, (P(x)\lor Q(x))$ is true.       
      To check that the converse is false, consider $P(x): x\text{ is even}, Q(x): x\text{ is odd}$.

---

- **Definition 3: Indirect Strategy for Disjunction**  
  Another useful strategy to prove $P \lor Q$ is to proceed indirectly. Assume that one of the disjuncts is false (say $\neg P$) and then prove the other ($Q$):  
  $$
  P \lor Q \equiv \neg P \implies Q
  $$

---

- **Definition 4: Proof by Cases**  
  If we know that $P \lor Q$ is true, and we can prove $R$ from $P$, and also prove $R$ from $Q$, we may conclude $R$:    
  - **Example 4.1**  
    Suppose a natural number is either even or odd, and we want to prove that $n^2$ is even. We divide the argument into two cases: if $n$ is even, $n^2$ is even; if $n$ is odd, $n^2$ is even. Since one of these cases must be true, $n^2$ is even in either case.    
    
  - **Example 4.2**  
    Proof: $P\land\left(Q\lor R\right)\equiv\left(P\land Q\right)\lor\left(P\land R\right)$      
    
    - **Solution 4.2.1**  
      We want to prove $\forall a,b,c\in\mathbb R,\min\{a,\max\{b,c\}\}=\max\{\min\{a,b\},\min\{a,c\}\}$. Let       
      $$
      \begin{aligned}              
      M_1 &:= \min\{a,\max\{b,c\}\} \\       
      M_2 &:= \max\{\min\{a,b\},\min\{a,c\}\}              
      \end{aligned}       
      $$
      we want to prove $M_1\leq M_2$ and $M_2\leq M_1$.        
      For the case $M_1\leq M_2$, by the definition of $\min$ and $\max$       
      $$
      \begin{aligned}              
      &M_1 \leq a \land M_1 \leq \max\{b,c\} \\       
      \implies& M_1 \leq a \land \left(M_1 \leq b \lor M_1 \leq c\right) \\       
      \implies& \left(M_1 \leq a \land M_1 \leq b\right) \lor \left(M_1 \leq a \land M_1 \leq c\right) \\       
      \implies& M_1 \leq \min\{a,b\} \lor M_1 \leq \min\{a,c\} \\       
      \implies& M_1 \leq \max\{\min\{a,b\},\min\{a,c\}\} \\       
      \implies& M_1 \leq M_2              
      \end{aligned}
      $$
      For the case $M_2\leq M_1$, by the definition of $\min$ and $\max$, we have       
      $$
      \min\{a,b\}\leq a, \min\{a,b\}\leq b\leq\max\{b,c\}
      $$
      then $\min\{a,b\}\leq\min\{a,\max\{b,c\}\}$.       
      The other inequality is almost the same. Then $M_2=\max\{\min\{a,b\},\min\{a,c\}\}$.    
      
    - **Solution 4.2.2**
      We want to prove $\forall a,b,c\in\mathbb R,\min\{a,\max\{b,c\}\}=\max\{\min\{a,b\},\min\{a,c\}\}$.
      Suppose $a,b,c\in\left\{0,1\right\}$. We split into two cases depending on the value of $a$.
      **Case 1** $a=0$
      $$
      \text{LHS}=\min\left\{0,\max\left\{b,c\right\}\right\}=0 \\
      \text{RHS}=\max\left\{\min\left\{0,b\right\},\min\left\{0,c\right\}\right\}=\max\left\{0,0\right\}=0
      $$
      Thus $\text{LHS}=\text{RHS}$.
      **Case 2** $a=1$
      $$
      \text{LHS}=\min\left\{1,\max\left\{b,c\right\}\right\}=\max\left\{b,c\right\} \\
      \text{RHS}=\max\left\{\min\left\{1,b\right\},\min\left\{1,c\right\}\right\}=\min\left\{b,c\right\}
      $$
      Thus $\text{LHS}=\text{RHS}$.
      Since equality holds for $a=0$ and $a=1$, the identity is true for all $a,b,c\in\left\{0,1\right\}$.
    
  - **Example 4.3**  
    Let $a_1,a_2,\cdots,a_7\in\mathbb Z$, prove that among these seven integers, one can always choose four numbers whose sum is even.      
    
    - **Solution 4.3.1**  
      Suppose $a_1,a_2,\cdots,a_7\in\mathbb Z$. Let $K$ be the number of odd integers among $a_1,a_2,\cdots,a_7$.       
      If $4\leq K\leq 7$, then take $4$ of these odd integers, their sum is even:       
      $$
      (2a+1)+(2b+1)+(2c+1)+(2d+1)=2(a+b+c+d+2)
      $$
      If $0\leq K<4$, then take $4$ of these even integers, their sum is even:       
      $$
      2a+2b+2c+2d=2(a+b+c+d)
      $$
      In both cases, we obtain that we can always choose four numbers whose sum is even.    
    
  - **Example 4.4**  
    Prove that $\forall n\in\mathbb Z$, if $n$ is odd, then $3n$ is odd.      
    - **Solution 4.4.1**  
      Suppose $n\in\mathbb Z$, and $n$ is odd. Then, there exists an integer $k\in\mathbb Z$ such that $n=2k+1$. Then       
      $$
      \begin{aligned}       
      3n &= 3(2k+1) \\       
      &= 6k+3 \\       
      &= 2(3k+1)+1       
      \end{aligned}       
      $$
      Since $3k+1$ is an integer, $3n$ is odd.    
    
  - **Example 4.5**  
    For every $a,b,c\in\mathbb Z$, prove that if $a\mid b$ and $b\mid c$, then $a\mid c$.      
    - **Solution 4.5.1**  
      Suppose $a,b,c\in\mathbb Z$ and $a\mid b \land b\mid c$. Then there exist $k,q\in\mathbb Z$ such that $b=ka$ and $c=qb$. Then $c=qka$, and since $qk\in \mathbb Z$, by definition, $a\mid c$.    
    
  - **Example 4.6**  
    Let $n\in \mathbb Z$. Prove that if $n^2$ is even, then $n$ is even.      
    - **Solution 4.6.1**  
      We will prove the contrapositive: $\forall n\in\mathbb Z$, if $n$ is odd, then $n^2$ is odd.       
      Suppose $n\in\mathbb Z$ is odd. Then $\exists k\in\mathbb Z$ such that $n=2k+1$. Then       
      $$
      n^2=(2k+1)^2=4k^2+4k+1=2(2k^2+2k)+1
      $$
      is odd because $2k^2+2k$ is an integer.    
    
  - **Example 4.7**  
    Prove that there is no smallest positive rational number.      
    - **Solution 4.7.1**  
      By contradiction, suppose there exists a smallest positive rational number $r$. Then $\frac{r}{2}$ is a smaller positive rational number. This is a contradiction because $r$ was assumed to be the smallest. Thus, there doesn't exist a smallest positive rational number.    
    
  - **Example 4.8**  
    $\forall \epsilon>0$, prove that $\exists N\in\mathbb N$ such that $\forall n\geq N$, $\dfrac{1}{n}<\epsilon$.      
    - **Solution 4.8.1**  
      Suppose $\epsilon > 0$. We will first prove that $\exists N\in\mathbb N$ such that $\dfrac{1}{N}<\epsilon$.        
      The Archimedean Property states that for any real number $x\in\mathbb R$, there exists a natural number $N\in\mathbb{N}$ such that $N>x$. By setting $x=\dfrac{1}{\epsilon}$ in the Archimedean Property, we guarantee that $\exists N \in \mathbb{N}$ satisfying $N>\dfrac{1}{\epsilon}$, and then $\epsilon >\dfrac{1}{N}$. Then if $n\geq N$, $\dfrac{1}{N}\geq\dfrac{1}{n}$ and $\dfrac{1}{n}<\epsilon$.

---

- **Definition 5: Direct Strategy for Implications ($P \implies Q$)**  
  To prove a statement of the form $P \implies Q$, we must show that whenever $P$ is true, $Q$ is also true.   
  - **Example 5.1**  
    To prove that if $n$ is even, then $n+1$ is odd, we assume that $n$ is even and then show that $n+1$ is odd.   
  - **Modus Ponens**  
    If we establish both $P \implies Q$ and $P$, we can conclude $Q$.

---

- **Definition 6: Indirect Strategy (Proof by Contrapositive)**  
  Since $P \implies Q \equiv \neg Q \implies \neg P$, we can prove $\neg Q \implies \neg P$ instead of $P \implies Q$.

---

- **Definition 7: Proof by Contradiction**  
  To prove $P \implies Q$, suppose that $P$ is true and $Q$ is false ($P \land \neg Q$) and show that this assumption leads to a contradiction ($R \land \neg R$):  
  $$
  P \implies Q \equiv (P \land \neg Q) \implies (R \land \neg R)
  $$
  We have:  
  $$
  \begin{array}{c|c|c|c|c|c|c|c} P & Q & R & \neg Q & P\land\neg Q & R\land\neg R & P\implies Q & (P\and \neg Q)\implies(R\and \neg R) \\ \hline 1 & 1 & 1 & 0 & 0 & 0 & 1 & 1 \\ 1 & 1 & 0 & 0 & 0 & 0 & 1 & 1 \\ 1 & 0 & 1 & 1 & 1 & 0 & 0 & 0 \\ 1 & 0 & 0 & 1 & 1 & 0 & 0 & 0 \\ 0 & 1 & 1 & 0 & 0 & 0 & 1 & 1 \\ 0 & 1 & 0 & 0 & 0 & 0 & 1 & 1 \\ 0 & 0 & 1 & 1 & 0 & 0 & 1 & 1 \\ 0 & 0 & 0 & 1 & 0 & 0 & 1 & 1 \end{array}
  $$

---

- **Definition 8: Disproofs and Counterexamples**  
  A statement is disproved if we show a single instance in which it is false, known as a **counterexample**.    
  For a universally quantified statement $\forall x P(x)$, a single object $x_0$ for which $P(x_0)$ is false suffices to disprove the statement.   
  For an implication $P \implies Q$, a counterexample consists of a situation where $P$ is true and $Q$ is false.   
  
  - **Example 8.1**  
    Consider the statement $x^2 - 1 > 0$ for all $x \in \mathbb{R}$. To disprove it, use the counterexample $x_0 = 1$, which gives $1^2 - 1 = 0 \ngtr 0$. Thus, the statement is false.    
  - **Example 8.2**  
    Prove that the existentially quantified statement $(\exists x \in \mathbb{R})\left(\frac{1}{x^2+1} > 1\right)$ is false.     
    - **Solution 8.2.1** 
    
    - We need to show that $\frac{1}{x^2+1} \le 1$ for every $x \in \mathbb{R}$. Since $0 \le x^2$ for all $x \in \mathbb{R}$, it follows that $1 \le x^2 + 1$. Because $x^2 + 1 > 0$, taking the reciprocal reverses the inequality:
      $$
      \frac{1}{x^2+1} \le 1
      $$
      for every $x \in \mathbb{R}$. Thus, the original statement is false.
