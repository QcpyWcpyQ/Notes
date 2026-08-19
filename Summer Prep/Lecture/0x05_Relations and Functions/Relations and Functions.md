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