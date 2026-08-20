## Relations and Functions  
- **Definition 1**   
  Let $X$ be a set. A **relation** $\sim$ on $X$ is a rule that determines for every $x,y\in X$ whether the statement   
  $$
  x\sim y   
  $$
  is true or false. If it is true, we say that $x$ is related to $y$. If it is false, we write $x\not\sim y$.    
  - **Example 1.1**     
    Let $X=\left\{1,2,3,4\right\}$, the following are examples of relations on $X$.     
    1. The relation $\sim$ given by $1\sim 2,2\sim 3,3\sim 1,4\sim 4$.     
    2. The relation $\sim$ given by $1\sim 1,2\sim 2,2\sim 4$.     
    3. The relation $\sim$ given by $1\sim 1,2\sim 2,3\sim 3,4\sim 4$.  
  
- **Definition 2**   
  Let $X$ be a set and $\sim$ a relation on $X$.    
  1. The relation is **reflexive** if $x\sim x$ for every $x\in X$.    
  2. The relation is **symmetric** if for every $x,y\in X$      
     $$
     x\sim y\implies y\sim x.
     $$
  3. The relation is **antisymmetric** if for every $x,y\in X$      
     $$
     x\sim y\land y\sim x\implies x=y.
     $$
  4. The relation is **transitive** if for every $x,y,z\in X$      
     $$
     x\sim y\land y\sim z\implies x\sim z.
     $$
  - **Example 2.1**     
    On the set $\mathbb Z$ consider the relation     
    $$
    x\sim y\iff x\leqslant y.
    $$
    Note that      
    1. $\sim$ is reflexive since $x\leqslant x$ for every $x\in\mathbb Z$.     
    2. $\sim$ is not symmetric since $1\leqslant 2$ but $2\not\leqslant 1$.     
    3. $\sim$ is antisymmetric because if $x\leqslant y$ and $y\leqslant x$ then $x=y$.      
    4. $\sim$ is transitive since $x\leqslant y$ and $y\leqslant z$ implies that $x\leqslant z$.  
  
- **Definition 3**   
  Let $X$ be a set. An **equivalence relation** on $X$ is a relation $\sim$ that satisfies the following properties.    
  1. $\sim$ is reflexive.   
  2. $\sim$ is symmetric.   
  3. $\sim$ is transitive.    
  - **Example 3.1**     
    Let $X=\left\{1,2,3,4\right\}$. The following are examples of equivalence relations on $X$.     
    1. The relation $\sim$ given by $1\sim1,2\sim2,3\sim3,4\sim4$.     
    2. The relation $\sim$ given by $1\sim1,2\sim2,3\sim3,4\sim4,2\sim3,3\sim2,1\sim4,4\sim1$.  
  
- **Definition 4**   
  Let $X$ be a set. An **order relation** on $X$ is a relation $\sim$ that satisfies the following properties.    
  1. $\sim$ is reflexive.   
  2. $\sim$ is antisymmetric.   
  3. $\sim$ is transitive.    
  - **Example 4.1**     
    Let $X=\left\{1,2,3,4\right\}$. The following are examples of order relations on $X$.     
    1. The relation $\sim$ given by $1\sim1,2\sim2,3\sim3,4\sim4$.     
    2. The relation $\sim$ given by $1\sim1,2\sim2,3\sim3,4\sim4,1\sim2,1\sim3,1\sim4,2\sim3,2\sim4,3\sim4$.  
  
- **Definition 5**   
  A **function** $f\colon X\to Y$ is a correspondence of elements of $X$ with elements of $Y$ such that forall $x\in X$ there exists a unique $y\in Y$ such that $y=f(x)$.   
  $$
  \begin{aligned}      
     f\colon X\to \ &Y \\   
  x\mapsto \ &y=f(x)      
     \end{aligned}   
  $$
  The element $y=f(x)$ is called the **image** of $x$ under $f$ and the element $x$ is called the **preimage** of $y$ under $f$.  
  
- **Definition 6**   
  If $f\colon X\to Y$ is a function, the **domain** of $f$ denote $\text{Dom}(f)$ is $X$ and the **codomain** of $\text{CoDom}(f)$ is $Y$. The **range** of $f$, denoted $\text{Ran}(f)$, is the set   
  $$
  \text{Ran}(f)=\left\{y\in Y: y=f(x)\text{ for some }x\in X\right\}   
  $$
  Note that $\text{Ran}(f)\subseteq Y$.    
  - **Example 6.1**      
    1. The function $f\colon\mathbb R\to\mathbb R$, $f(x)=x^2$.     
    2. The function $g\colon\mathbb R\to\mathbb R$, $g(x)=\sin(x)$.     
    3. The function $h\colon \left[0,\infty\right)\to\mathbb R$, $h(x)=\sqrt{x}$.    
  - **Example 6.2**     
    Let $X=\left\{1,2,3\right\}$ and $Y=\left\{a,b,c\right\}$ the following examples of functions from $X$ to $Y$.      
    1. The function $f\colon X\to Y$ defined by        
       $$
       f(1)=a\quad f(2)=b\quad f(3)=c.
       $$
    2. The function $g\colon X\to Y$ defined by        
       $$
       g(1)=a\quad g(2)=a\quad g(3)=a.
       $$
    3. The function $h\colon X\to Y$ defined by        
       $$
       h(1)=a\quad h(2)=b\quad h(3)=a.
       $$
  
- **Definition 7**   
  Two functions $f\colon X\to Y$ and $g\colon Z\to W$ are **equal** if $X=Z,Y=W$ and $f(x)=g(x)$ for all $x\in X$.    
  
  - **Example 7.1**     
    1. Let $X$ be a set. The **identity function** on $X$ is the function $\mathrm{id}_x\colon X\to X$ given by $\mathrm{id}_x(x)=x$.     
    2. Let $X$ and $Y$ be sets and $c\in Y$. The **constant function** with value $c$ is the function $\mathrm K_c\colon X\to Y$ given by $\mathrm K_c(x)=c$.     
    3. Let $X$ be a set and $A\subseteq X$. The **inclusion function** of $A$ in $X$ is the function $\iota\colon A\to X$ (or $\iota\colon A\hookrightarrow X$) given by $\forall x\in A,\iota(x)=x$.     
    4. If $f\colon X\to Y$ is a function and $A\subseteq X$, the **restriction** of $f$ to $A$ is the function $f \big|_A\colon A\to Y$ given by $f\big|_A(x)=f(x)$ for all $x\in A$.
  
- **Definition 8**
  If $f\colon X\to Y$ and $g\colon Z\to W$ are functions, the **composition** of $g$ with $f$, denoted $g\circ f$, is the function $g\circ f\colon X\to Z$ defined by $\left(g\circ f\right)=g\left(f\left(x\right)\right)$ for all $x\in X$.
  
  - **Example 8.1**
    Note that if $f\colon X\to Y$, $f$ is a function and $A\subseteq X$, we have that $f \big|_A=f\circ \iota_A$ where $\iota\colon A\to x$.
    $$
    A\xrightarrow{\iota}X\xrightarrow{f}Y.
    $$
  
- **Remark 8**
  Note that even in the case both $g\circ f$ and $f\circ g$ are defined, the composition of two functions is not commutative, that is, in general $g\circ f\neq f\circ g$.
  
  - **Example 8.2**
    Consider the functions
    $$
    \begin{aligned}
    
    f\colon &\mathbb R\to \mathbb R,\quad g\colon \mathbb R\to \mathbb R. \\
    &x\mapsto x^2,\quad x\mapsto x+1.
    &
    \end{aligned}
    $$
    Note thet $g\circ f\colon \mathbb R\to \mathbb R$ and $f\circ g\colon \mathbb R\to \mathbb R$ with
    $$
    \begin{aligned}
    
    g\circ f&=g\left(f\left(x\right)\right) \\
    &=g\left(x^2\right) \\
    &=x^2+1
    
    \end{aligned}
    \quad
    \begin{aligned}
    
    f\circ g&=f\left(g\left(x\right)\right) \\
    &=f\left(x+1\right) \\
    &=\left(x+1\right)^2.
    
    \end{aligned}
    $$
    In particular if $x=2$ we have that $(g\circ f)(2)=5$ and $(f\circ g)=9$. Therefore $g\circ f\neq f\circ g$.
    
  - **Proposition 8.3**
    Let $f\colon X\to Y,g\colon Y\to Z$ and $h\colon Z\to W$ be functions, the $(h\circ g)\circ f=h\circ(g\circ f)$. In other words, the composition is associative.
    
    - **Proof 8.3.1**
      Let $x\in X$ then
      $$
      \begin{aligned}
      
      [(h\circ g)\circ f](x)&=(h\circ g)(f(x)) \\
      &=h(g(f(x))) \\
      &=h((g\circ f)(x)) \\
      &=[h\circ(g\circ f)](x).
      
      \end{aligned}
      $$
      Now, as $[(h\circ g)\circ f](x)=[h\circ(g\circ f)](x)$ for all $x\in X$ we have that $(h\circ g)\circ f=h\circ(g\circ f)$.
    
  - **Example 8.4**
    Let $s,t\colon \mathbb Z\to \mathbb Z$ be functions defined by $s(x)=x+1$ and $t(x)=2x$. Prove that $t\circ s\neq s\circ t$.
    
    - **Proof 8.4.1**
      Let $x\in\mathbb Z$ then
      $$
      \begin{aligned}
      
      t\circ s&=t\left(s\left(x\right)\right) \\
      &=t\left(x+1\right) \\
      &=2x+2
      
      \end{aligned}
      \quad
      \begin{aligned}
      
      s\circ t&=s\left(t\left(x\right)\right) \\
      &=s\left(2x\right) \\
      &=2x+1.
      
      \end{aligned}
      $$
      In particular if $x=2$ we have that $(t\circ s)(2)=6$ and $(s\circ t)(2)=5$. Therefore $t\circ s\neq s\circ t$.
    
  - **Example 8.5**
    Let $X=\left\{1,2,3,4,5\right\}$ and let $f\colon X\to X$ be the function defined by 
    $$
    f(1)=2,\quad f(2)=2, \quad f(3)=4,\quad f(4)=4,\quad f(5)=4.
    $$
    Show that $f\circ f=f$. Find a function $g$ such that $g\circ f=f$ and $f\circ g=f$.
    
    - **Solution 8.5.1**
      $$
      g\colon X\to X \\
      g(1)=1,\quad g(2)=2, \quad g(3)=5,\quad g(4)=4,\quad g(5)=3.
      $$
      Then
      $$
      (g\circ f)(1)=g(f(1))=g(2)=2=f(1), \\
      (g\circ f)(2)=g(f(2))=g(2)=2=f(2), \\
      (g\circ f)(3)=g(f(3))=g(4)=4=f(3), \\
      (g\circ f)(4)=g(f(4))=g(4)=4=f(4), \\
      (g\circ f)(5)=g(f(5))=g(4)=4=f(5).
      $$
      Therefore $g\circ f=f$. Similarly, we can prove $f\circ g=f$ and $f\circ f=f$.
  
- **Definition 9**
  Let $f\colon X\to Y$ be a function.
  We say that $f$ is **injective** if given $x_1,x_2\in X$, such that $f\left(x_1\right)=f\left(x_2\right)$ implies $x_1=x_2$.
  Equivalently, if given $x_1,x_2\in X$ such that $x_1\neq x_2$ implies $f\left(x_1\right)\neq f\left(x_2\right)$.
  
  We say that $f$ is **surjective** if for every $y\in Y$ there exists $x\in X$ such that $y=f(x)$.
  
  We say that $f$ is **bijective** if it is both injective and surjective.
  
- **Remark 9**
  If there exists a bijective function $f\colon X\to Y$. We say that $X$ and $Y$ are **one-to-one correspondence**.
  
  - **Example 9.1**
    The identity function $\text{id}_x\colon X\to X$ is injective since if $\text{id}_x(x)=\text{id}_x(y)$ then $x=y$.
    It is also surjective since for all $x\in X$ we have that $x=\text{id}_x(x)$.
    Therefore, $\text{id}_x$ is bijective.
    
  - **Example 9.2**
    Consider the constant function $\text{K}_c\colon X\to Y$.
    Note that if $X$ has more than one element the function is not injective and if $Y$ has more than one element the function is not surjective.
    
  - **Example 9.3**
    The inclusion function $\iota\colon A\to X$ is injective since $\iota_A(x)=\iota_A(y)$ implies $x=y$. Note that, if $A=X$ then $\iota_x=\text{id}_x$. Therefore $\iota_A$ is surjective. If $A\neq X$ and is not surjective if $A\subset X$.
    
  - **Example 9.4**
    Composition and Injectivity/Surjectivity
    Suppose that $f \colon A \rightarrow B$ and $g \colon B \rightarrow C$ are functions. Prove that if $g \circ f$ is injective then $f$ is injective, and if $g \circ f$ is surjective then $g$ is surjective.
    
    - **Solution 9.4.1**
      **Proof:**
      
      * **First Part (If $g \circ f$ is injective, then $f$ is injective):**
        Let $x_1, x_2 \in A$ be arbitrary elements in the domain of $f$ such that:
        $$
        f(x_1) = f(x_2)
        $$
        Since $g$ is a function, applying $g$ to both sides yields identical outputs:
        $$
        g(f(x_1)) = g(f(x_2))
        $$
        By definition of function composition, this is equivalent to:
        $$
        (g \circ f)(x_1) = (g \circ f)(x_2)
        $$
        We are given the hypothesis that $g \circ f$ is injective. By definition of an injective function, $(g \circ f)(x_1) = (g \circ f)(x_2) \implies x_1 = x_2$.
        Thus, $f(x_1) = f(x_2) \implies x_1 = x_2$, proving that $f$ is injective.
      
      * **Second Part (If $g \circ f$ is surjective, then $g$ is surjective):**
        Let $z \in C$ be an arbitrary element in the codomain of $g$.
        We are given the hypothesis that $g \circ f \colon A \rightarrow C$ is surjective. By definition of a surjective function, there exists some element $x \in A$ such that:
        $$
        (g \circ f)(x) = z
        $$
        By definition of function composition, this means:
        $$
        g(f(x)) = z
        $$
        Let $y = f(x)$. Since $x \in A$ and $f \colon A \rightarrow B$, it follows that $y \in B$.
        Substituting $y$ back into the equation gives $g(y) = z$.
        Thus, for any arbitrary $z \in C$, there exists an element $y \in B$ such that $g(y) = z$, proving that $g$ is surjective.