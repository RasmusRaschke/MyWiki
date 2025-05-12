<div class="topSpace"></div>

Date Created: [[11/05/2025]]
References: #Ref/AlgTop 
Tags: #Type/Theorem 

Proved by: [[mapping degree]]
References: [[sphere]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# In Dimension $2n$

``` ad-Theorem
title: Theorem (Hairy Ball Theorem).
Any tangential [[vector field]] on $\S^{2n}$ is trivial in at least one point.

```
*Proof.*
We represent the tangent space of $\S^{2n}$ by 
$$
T_x\S^{2n} = \{y \in \R^{2n+1} \mid \langle x,y \rangle=0\}.
$$
Now assume that there is a [[vector field|tangent vector field]] $V: \S^{2n} \to T\S^{2n}$ with $V(x)\in T_x\S^{2n}$ and $V(x)\neq 0$ for all $x$. This justifies the definition of an auxiliary function 
$$
\begin{align}
f: \S^{2n} &\to \S^{2n}\\
x &\mapsto f(x):=\frac{V(x)}{\|V(x)\|}.
\end{align}
$$
By [[antipodal map#Non-agreeing and Antipodal Maps|the second corollary]] we know that $f(x)=x$ or $f(x)=-x$ for some $x \in \S^{2n}$. In both cases, we obtain $V(x)=\pm x\|V(x)\|$ which implies that $V(x)$ points outward or inward of $\S^{2n}$ and is not tangential, a contradiction. <span style="float:right;">$\blacksquare$</span>

**Remark.**
Note that it is easy to construct such a vector field in uneven dimension: For $\S^{2n+1}\sub \C^n$ one can simply choose $$
(z_1, \dots, z_n) \mapsto (iz_1, \dots, iz_n).
$$