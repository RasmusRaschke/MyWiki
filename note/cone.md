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
For $n>0$, we calculate $\partial_i K_v(\alpha)$ and see that $\partial_{n+1}K_v(\alpha)= \alpha$ and $\partial_i (K_v(\alpha))=K_v(\partial_i \alpha)$ for all $i < n+1$.