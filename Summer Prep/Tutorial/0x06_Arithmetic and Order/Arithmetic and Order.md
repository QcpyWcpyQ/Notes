## Arithmetic and Order

- **Exercise 1 (Additive Cancellation)**
  Let $a,b,c\in\mathbb Z$. Prove that $a+b=a+c\implies b=c$.

  - **Proof 1.1**
    Suppose $a,b,c\in\mathbb Z,a+b=a+c$. Consider the additive inverse of $-a$ of a.
    $$
    \begin{aligned}
    
    -a+(a+b)&=-a+(a+c) \\
    (-a+a)+b&=(-a+a)+c \\
    0+b&=0+c \\
    b&=c.
    
    \end{aligned}
    $$

---

- **Exercise 2 (If adding something changes nothing)**
  Suppose $a,b\in\mathbb Z$ and $a+b=a$. Prove that $b=0$.

  - **Proof 2.1**
    Suppose $a,b\in\mathbb Z$ and $a+b=a$. By propoties,
    $$
    \begin{aligned}
    
    a+0&=a \\
    a+b&=a+0 \\
    b&=0.
    
    \end{aligned}
    $$

---

- **Exercise 3**
  Suppose $a,b\in\mathbb Z$ and $a+b=0$. Prove that $b=-a$.

  - **Proof 3.1**
    Suppose $a,b\in\mathbb Z$ and $a+b=0$. By propoties, 
    $$
    \begin{aligned}
    a+(-a)&=0\\
    a+b&=a+(-a)\\
    b&=-a.
    \end{aligned}
    $$

---

- **Exercise 4**
  Suppose $a,b,x,y\in\mathbb Z$, $a+x=b\land a+y=b$. Prove $x=y$.

  - **Prove 4.1**
    Suppose $a,b,x,y\in\mathbb Z$, $a+x=b$, $a+y=b$. Then $a+x=a+y$. By cancellation law $x=y$.

---

- **Exercise 5**
  Suppose $e\in\mathbb Z$ has the property that $\forall a\in\mathbb Z,a+e=a$. Prove that $e=0$.
  - **Proof 5.1**
    Suppose $e,a\in\mathbb Z$, $a+e=a=a+0\implies e=0$.

---

- **Exercise 6**
  Suppose $a,b,c\in\mathbb Z,a+b=0\land a+c=0$. Prove that $b=c$.
  - **Proof 6.1**
    Suppose $a,b,c\in\mathbb Z,a+b=0\land a+c=0$. Then, $a+c=a+b$. By cancellation law, c=b.

---

- **Exercise 7**
  Prove that $-0=0$.
  - **Proof 7.1**
    $0+(-0)=0=0+0$. By cancellation law, $-0=0$.

---

- **Exercise 8 (Negating an inequality)**
  Suppose $a,b\in\mathbb Z,a<b\implies -b<-a$.
  
  - **Proof 8.1**
    Suppose $a,b\in\mathbb Z,a<b$. By definition, $a<b\iff a\leqslant b \land a\neq b$. Then
    $$
    \begin{aligned}
    
    a+(-a-b)&\leqslant b+(-a-b)\\
    (a+(-a))+(-b) &\leqslant (b+(-b)) +(-a) \\
    0+(-b) &\leqslant 0+(-a) \\
    -b&\leqslant -a
    
    \end{aligned}
    $$
    As $-a\neq -b\implies -b<-a$.

---

- **Exercise 9**
  Suppose $a,b\in\mathbb Z,c<0,a<b$ Prove that $ac>bc$.

  - **Proof 9.1**
    Suppose $a,b\in\mathbb Z,c<0,a<b$. By definition, $a<b\iff a\leqslant b\land a\neq b$. Then
    $$
    \begin{aligned}
    
    -c>0 &\implies (-c)a\leqslant (-c)b \\
    &\implies -ca\leqslant -cb \\
    &\implies -ca<-cb\quad(\text{as }a\neq b\implies ca\neq cb\implies -ca\neq -cb) \\
    &\implies ca>cb
    
    \end{aligned}
    $$
