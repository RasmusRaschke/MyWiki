<div class="topSpace"></div>

Date Created: 25/09/24
References: 
Tags: #Type/Proposition #Topic/Algebra #Topic/DifferentialGeometry

Proved by: [[derivation]]
References: [[derivation]], [[commutator]], [[Lie group]], [[Lie algebra]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition (Commutator as Lie bracket).

Let $V$ be a $\R$-[[algebra]]. Then $\text{Der}(V)$ is, together with the [[commutator]] $$[.,.]: \text{Der}(V) \times \text{Der}(V) \to \text{Der}(V),$$ a [[Lie algebra]]. In this case, the commutator is called __Lie bracket__. The following axioms are satisfied:
1. $[.,.]$ is $\R$-bilinear.
2. $[.,.]$ is skew symmetric: $[\cD_1, \cD_2] = - [\cD_2, \cD_1]
3. The __Jacobi identitiy__ holds: $[\cD_1, [\cD_2, \cD_3]] + [\cD_2, [\cD_3, \cD_1]] + [\cD_3, [\cD_1, \cD_2]]$

```

<i>Proof.</i>
The proof only contains trivial calculations.
<span style="float:right;">$\blacksquare$</span>

**Corollary.**
On every [[manifold|smooth manifold]] $M$ a Lie algebra is given by the [[vector field|smooth vector fields]] $\Gamma(TM)$ together with the commutator.

<i>Proof.</i>
For local coordinate [[vector field|vector fields]] $\frac{\partial}{\partial x_i}$ and $\frac{\partial}{\partial x_j}$ the identity $$\left[\frac{\partial}{\partial x_i}, \frac{\partial}{\partial x_j} \right] = 0$$ holds.
<span style="float:right;">$\blacksquare$</span>