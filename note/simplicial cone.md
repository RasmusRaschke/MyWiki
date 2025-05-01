<div class="topSpace"></div>

Date Created: [[30/04/2025]]
References: #Ref/AlgTop 
Tags: #Type/Definition #Topic/AlgebraicTopology 

Proved by: <i>Not Applicable</i>
References: [[singular simplex]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Cones of Singular $n$-Simplices

``` ad-Definition
title: Definition (Cone).
Let $v \in \Delta^p$ and let $\alpha: \Delta^n \to \Delta^p$ be a [[singular simplex|singular $n$-simplex]] in $\Delta^p$.
The <ins>cone</ins> of $\alpha$ with respect to $v$ is a map
$$
\begin{split}
K_v(\alpha): \Delta^{n+1} &\to \Delta^p\\
(t_0, \dots, t_{n+1}) &\mapsto
\begin{cases}
(1-t_{n+1}) \alpha\left( \frac{t_0}{1-t_{n+1}}, \dots, \frac{t_n}{1-t_{n+1}} \right) \ &\text{for } t_{n+1} \leq 1,\\
v, \ &t_{n+1}=1.
\end{cases}
\end{split}
$$

```
This map is well-defined and continuous. On the standard basis, we obtain $K_v(e_i)=\alpha(e_i)$ for $0 \leq i \leq n$ and $K_v(e_{n+1})=v$. The linear extension of $K_v$ yields a map
$$
K_v: S_n(\Delta^p) \to S_{n+1}(\Delta^p).
$$

## Identities

``` ad-Proposition
title: Proposition (Cone Map Properties).

The extended map $K_v$ satisfies:
1. $\partial K_v(c)=\epsilon(c).\kappa_v -c$ for $c \in S_0(\Delta^p)$, $\kappa_v(e_0)=v$ and the [[zeroth homology group|augmentation map]] $\epsilon$.
2. For $n>0$ we have $\partial K_v -K_v \delta = (-1)^{n+1}\id.$
```
*Proof.*
Let $\alpha: \Delta^0 \to \Delta^p$ be a [[singular simplex|singular $0$-simplex]]. We know that $\epsilon(\alpha)=1$ and can calculate:
$$
\partial K_v(\alpha)(e_0) = (K_v(\alpha)d_0)(e_0) - (K_v(\alpha)d_1)(e_0)=K_v(\alpha)(e_1)-K_v(\alpha)(e_0) = v-\alpha(e_0).
$$
For $n>0$, we start by calculating $\partial_{n+1}K_v(\alpha)$ for some standard basis vector $e_j \in \Delta^n$:
$$
\partial_{n+1}K_v(\alpha)(e_j) = K_v(\alpha)d_{n+1}^n(e_j)=K_v(\alpha)(\dots, 0) = \alpha(e_j)
$$
since $d_{n+1}^{n}$ always inserts a $0$ at position $n+1$ so $\partial_{n+1}K_v(\alpha)=\alpha.$ Now we consider $\partial_i K_v(\alpha)$ for $i < n+1$ evaluated on $e_j \in \Delta^n:$
$$
\begin{align}
\partial_iK_v(\alpha)(e_j) &= K_v(\alpha)d_i^n(e_j)=
\begin{cases}
(1-\{d_i^ne_i\}_{n+1}) \alpha\left( \frac{\{d_i^ne_i\}_0}{1-\{d_i^ne_i\}_{n+1}}, \dots, \frac{\{d_i^ne_i\}_n}{1-\{d_i^ne_i\}_{n+1}} \right) \ &\text{for } j\neq n,\\
v, \ &j=n.
\end{cases}\\
&= K_v(\partial_i \alpha)(e_j)
\end{align}
$$
and obtain $\partial_iK_v(\alpha)=K_v(\partial_i\alpha).$ We used the fact that $e_j$ has $1$ as $n$-th coordinate only if $j=n.$ Since $d_i^n$ only shifts indices in front of $n,$ this yields a $1$ at position $n+1$ if and only if position $n$ has coordinate $1$. With this, the proposition follows as:
$$
\begin{align}
(\partial K_v - K_v\partial)(\alpha) &= \sum_{i=0}^{n+1} (-1)^i\partial_iK_v(\alpha)-K_v\sum_{i=0}^{n}(-1)^i\partial_i(\alpha)  \\
&= (-1)^{n+1}\alpha + \sum_{i=0}^n (-1)^i [(K_v(\partial_i \alpha))- K_v(\partial_i\alpha)] = (-1)^{n+1} \alpha.
\end{align}
$$
<span style="float:right;">$\blacksquare$</span>