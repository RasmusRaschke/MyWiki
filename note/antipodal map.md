<div class="topSpace"></div>

Date Created: [[11/05/2025]]
References: #Ref/AlgTop 
Tags: #Type/Definition #Type/Proposition #Topic/Topology  

Proved by: <i>Not Applicable</i>
References: [[mapping degree]]
Justifications: [[sphere]]

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Definition

``` ad-Definition
title: Definition (Antipodal map).
The <ins>antipodal map</ins> on $\S^n$ is defined as
$$
\begin{align}
A: \S^n &\to \S^n\\
x &\mapsto A(x)=-x.
\end{align}
$$

```

# Mapping Degree

First, we observe that the map $f^{(n)}: \S^n \to \S^n$ which maps $(x_0,x_1, \dots, x_n)$ to $(-x_0, x_1, \dots, x_n)$ has degree $-1$. For $n=0$, the [[sphere#Fundamental Class|fundamental class]] is given by $[1]-[-1]$ and we obtain
$$
f^{(0)} ([1]-[-1]) = [-1]-[1]=-\mu_0.
$$
Now assume this holds for $n-1$. By naturality of $D$, we can conclude
$$
H_n(f^{(n)}) \mu_n= H_n(f^{(n)}) D^{-1}\mu_{n-1}=D^{-1}H_{n-1}(f^{(n-1)})\mu_{n-1}=D^{-1}(-\mu_{n-1})=- \mu_n.
$$
With this, we obtain the desired result:
``` ad-Proposition
title: Proposition (Mapping Degree of the Antipodal Map).
The antipodal map $A: \S^n \to \S^n$ has degree $(-1)^{n+1}$.
```
*Proof.*
Define $f_i^n: \S^n \to \S^n$ as the map which flips the sign of the $i$-th coordinate. The statement above shows that $f_i^n$ is of degree $-1$.  Splitting $A$ into $f_n^n f_{n-1}^n \cdots f_0^n$, the claim follows.
<span style="float:right;">$\blacksquare$</span>

**Remark.**
This implies that the antipodal map can not be homotopic to the identity for even $n$.

## Non-agreeing and Antipodal Maps

``` ad-Proposition
title: Proposition (Homotopy of non-agreeing Maps).
Let $f,g: \S^n \to \S^n$ be continuous maps with $f(x)\neq g(x)$ for all $x \in \S^n$. Then $f \simeq Ag$ and 
$$
\deg(f) = (-1)^{n+1} \deg(g).
$$
```
*Proof.*
The line segment $t \mapsto (1-t)f(x)-tg(x)$ does not pass through the origin for $t \in [0,1]$ by assumption. Therefore, we can consider the homotopy
$$
H(x,t):=\frac{(1-t)f(x)-tg(x)}{\|(1-t)f(x)-tg(x) \|}
$$
with 
$$
H(x,0)=\frac{f(x)}{\|f(x)\|}=f
$$
and
$$
H(x,1) = \frac{-g(x)}{\|-g(x)\|} = Ag,
$$
yielding $f \simeq Ag$.  <span style="float:right;">$\blacksquare$</span>

``` ad-Proposition
title: Corollary (From Homotopy of non-agreeing Maps).
Let $f: \S^n \to \S^n$ be a continuous map.
1. If $\deg(f)=0$ there are $x_+,x_- \in \S^n$ such that $f(x_+)=x_+$ and $f(x_-)=-x_-$.
2. If $n$ is even, there is an $x \in S^n$ with $f(x)=x$ or $f(x)=-x$.
```
*Proof.*
1. Suppose $f(x)\neq x$ for all $x$. This means $f(x)\neq \id(x)$ for all $x$ and we obtain a homotopy $f \simeq A$ by the proposition above. But this implies $0=\deg(f)=\deg(A)\neq 0$, a contradiction. Similarly, $f(x)\neq -x$ implies $f(x) \simeq -A$ and $0 = \deg(f)=(-1)^{n+1}A \neq 0$.
2. Suppose $n$ is even but $f(x)\neq \pm x$ for all $x$. Again, we obtain $f \simeq A$ and $f \simeq -A$, implying $A \simeq -A$ and therefore $\deg(A)=\deg(-A)=- \deg(A)$ since $n$ is even. This is a contradiction.
<span style="float:right;">$\blacksquare$</span>