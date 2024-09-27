<div class="topSpace"></div>

Date Created: 25/09/24
References: 
Tags: #Type/Proposition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[vector field]], [[integral curve]], [[manifold]], [[ode]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition (Maximal Solutions of Integral Curves).

Let $M$ be a [[manifold|smooth manifold]] and $X \in \Gamma(TM)$ be a [[vector field]]. Then the following statements are true:
1. $\sD_X$ \sub M \times \R$ is an open subset.
2. Let $c_p: I_p \to M$ be the maximal [[integral curve]] through $p$. Then $\Phi: \sD_X \to M$, $(p,t) \mapsto c_p(t)$ is [[smooth mapping|smooth]].
3. For $p \in M$ and $q = \Phi(p,t)$ we have $I_q = I_p - t$ and $\Phi(p, s+t) = \Phi(\Phi(p,t), s) = \Phi(q,s)$ as long as one of those terms is defined.
```

<i>Proof.</i>
1. Corollary of [[Picard-Lindelöf theorem]].
2. Corollary of a proposition about [[ode]].
3. Uniqueness statement.
<span style="float:right;">$\blacksquare$</span>