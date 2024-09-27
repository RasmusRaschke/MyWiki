<div class="topSpace"></div>

Date Created: 25/09/24
References: 
Tags: #Type/Proposition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[vector field]], [[derivation]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition (Local Form of Vector Fields).

Let $\phi: U \to V \sub \R^n$ be a [[chart]] of the [[manifold|smooth manifold]] $M$ with local coordinates $(x_1, \dots, x_n)$. Then every locally defined, smooth [[vector field]] $X \in \Gamma(TM|_U)$ admits the representation $$X(p) = \sum_{i=1}^n X(x_i) \cdot \left. \frac{\partial}{\partial x_i}\right|_p$$ where $X_p(x_i) =: X(x_i)(p)$ is a [[derivation]] in $p$.
Adversely, for any function $f_1, \dots, f_n \in \cC^\infty (U, \R)$, a smooth, local [[vector field]] is defined by $$fX := \sum_{i=1}^n f_i \frac{\partial}{\partial x_i}.$$
```

<i>Proof.</i>
The first pointwise formula was already proven while [[derivations describe tangent space|describing tangent vectors as derivations]]. The functions $X(x_i)$ are smooth because they describe $X$ in the [[vector bundle|local trivialization]] by $\left( \frac{\partial}{\partial x_1}, \dots, \frac{\partial}{\partial x_n}\right)$. The last statement is trivial.
<span style="float:right;">$\blacksquare$</span>