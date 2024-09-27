<div class="topSpace"></div>

Date Created: 16/12/2023 18:21:37
References: 
Tags: #Type/Proposition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[submanifold]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition (Chart lemma).

Let $M\sub \R^n$ be a $k$ dimensional submanifold and $p \in M$. Then there exists a neighbourhood $U \sub \R^n$ of $p$, an open subset $W \sub \R^k$ and a smooth mapping $\phi: W \to U$ with the following properties:
1. For all $y \in W$ has $\mathcal{D}\phi_y: \R^k \to \R^k$ maximal rank.
2. $\phi$ is *injective* with $\phi(W) = U \cap M$.

```

<i>Proof.</i> For a local diffeomorphism $h$ like in the definition of [[submanifold]], we choose $W := \R^k \times \{ 0\}^{n-k}$ and $\phi: h^{-1}|_{W}:W \to U \cap M$  .<span style="float:right;">$\blacksquare$</span>

**Remark.** $\phi: W \to U \cap M$ is actually a [[homeomorphism]].