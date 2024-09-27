<div class="topSpace"></div>

Date Created: 25/09/24
References: 
Tags: #Type/Proposition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition (Vector Fields and Derivations are isomorphic).

Let $M$ be a [[manifold|smooth manifold]]. The [[vector space|real vector space]] of [[vector field|vector fields]] $\Gamma(TM)$ on $M$ is naturally [[isomorphism|isomorphic]] to the [[vector space]] of [[derivation|derivations]] $\text{Der}(\cC^\infty(M))$.

```

<i>Proof.</i>
[[vector field|Vector fields]] are [[local form of vector fields|pointwise tangent vectors]] so for $X \in \Gamma(TM)$ and $f \in \cC^\infty (M)$ we define a function $$Xf: M \to \R$$ by $$(Xf)(p):= \underbrace{X_p}_{\in T_pM} f.$$ A quick calculation in [[local form of vector fields|local coordinates]] shows that this function is indeed smooth. For this one applies the local representation $X = \sum_i X_i \frac{\partial}{\partial x_i}$ to $f$ which yields a sum of [[smooth mapping|smooth functions]]. Furthermore, $$\cC^\infty (M) \to \cC^\infty (M)$$ $$f \mapsto Xf$$ is $\R$-linear and satisfies the [[derivation|leibniz rule]]. Henceforth, every $X \in \Gamma(TM)$ is mapped to a [[derivation]] $\cD_x \in \text{Der}(\cC^\infty(M))$ by $\cD_X(f) = Xf$. The mapping $\Gamma (TM) \to \text{Der}(\cC^\infty(M))$ is trivially [[linear map|linear]].
Let now $\cD \in \text{Der}(\cC^\infty (M))$. Evaluating at $p \in M$ gives rise to a tangent vector $X_\cD (p) \in \text{Der}_p \cong T_pM$. This mapping defines a [[sections|section]] given by $$M \to TM$$ $$ p \mapsto X_\cD (p)$$. Because $\cD f$ is smooth for all $f \in \cC^\infty (M)$, this holds in general for adapted local coordinate funtions $x_i$.
Therefore, $X_\cD$ has the local representation
$$
X_\cD |_U = \sum_{i=1}^n \cD(x_i) \frac{\partial}{\partial x_i}
$$
with smooth coefficients $\cD(x_i)$. This makes $X_\cD$ a [[vector field|smooth vector field]].
As these mappings are obviously inverse to each other, they define the proposed [[isomorphism]].
<span style="float:right;">$\blacksquare$</span>