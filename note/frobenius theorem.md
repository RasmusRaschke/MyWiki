<div class="topSpace"></div>

Date Created: 30/09/24
References: 
Tags: #Type/Theorem #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[geometric distribution]], [[manifold]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Theorem
title: Theorem (Frobenius' Theorem).

Let $M$ be a [[manifold|smooth manifold]] and $\Delta \sub TM$ be a smooth [[geometric distribution|distribution]] of rank $k$. Then the following statements are equivalent:
1. $\Delta$ is integrable: For every $p \in M$ exists an integral manifold of dimension $k$ for $\Delta$.
2. $\Delta$ is involutive: For any $X,Y \in \Gamma (\Delta)$ we have $[X,Y] \in \Gamma (\Delta)$.
3. Let $U \sub M$ be an open subset and $\Delta = \ker \alpha_1 \cap \cdots \cap \ker \alpha_{n-k}$ for pointwise linearly independent [[smooth k-form|$1$-forms]] $\alpha_1, \dots, \alpha_{n-k} \in \Omega^1(U)$. Then for every $1 \leq j \leq n-k$ $$(d \alpha_j) \wedge \alpha_1 \wedge \cdots \wedge \alpha_{n-k} = 0$$ holds.
4. Let $U$ and $\alpha_i$ be like above. Then there exist [[smooth k-form|$1$-forms]] $\theta_{ij} in \Omega^1(U)$ with $1 \leq i$ and $j \leq n-k$ such that $$d\alpha_j = \sum_{i_1}^{n-k} \theta_{ij} \wedge \alpha_i$$ for all $1 \leq j \leq n-k$$.

```

<i>Proof.</i>
Somewhat simple is $2 \iff 3 \iff 4$ and $1 \implies 3$- Difficult to prove is $3 \implies 1$-
$(4 \implies 3)$: Trivial as $\alpha \wedge \alpha = 0$.
$(3 \implies 4)$: We complete $\alpha_1, \dots, \alpha_{n-k}$ with suited forms $\beta_1, \dots, \beta_n$ to a local [[frame]] of $T^\ast M|_U$. The [[exterior derivative]] is given by 
$$ d\alpha_j = \sum_{r<s} A_{rs} \alpha_r \wedge \alpha_s + \sum_{r,l} B_{rl} \alpha_r \wedge \beta_l + \sum_{l < m} C_{lm} \beta_l \wedge \beta_m.$$
Statement 3 is equivalent to $\sum_{l<m} C_{lm}(\beta_l \wedge \beta_m) \wedge \alpha_1 \wedge \cdots \wedge \alpha_{n-k}=0$ which implies $C_{lm} = 0$ for all $l < m$.Excluding $\alpha_r$ from the first two terms yields $$d\alpha_j = \sum_{r=i}^{n-k} \theta_{jr} \wedge \alpha_r.$$
$(2 \iff 3)$: Let $\eta_j := (d \alpha_j) \wedge \alpha_1 \wedge \cdots \wedge \alpha_{n-k}$ be a $n-k+2$-form. Contracting it with $n-k+2$ [[vector field|vector fields]] we can assume that at least two of them are tangential to $\Delta$.  Call these fields $V$ and $W$. For the only non-vanishing terms $V$ and $W$ have to be contracted with $d\alpha_j$. However,
$$d \alpha_j (V,W) = \cancel{V(\alpha_j(W)) - W(\alpha_j(V))} - \alpha_j([V,W])$$ by this [[exterior derivative|remark]].
<span style="float:right;">$\blacksquare$</span>

**Corollary.**
For $k=1$ the form $(d \alpha_j) \wedge \alpha_1 \wedge \cdots \wedge \alpha_{n-1}$ is a $n+1$-form on $M$ and therefore trivially $0$. For $k=n-1$ is the third statement given by $d \alpha \wedge \alpha = 0$.