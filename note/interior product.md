<div class="topSpace"></div>

Date Created: 30/09/24
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[tangent bundle]], [[cotangent bundle]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Interior Product).

Let $M$ be a [[manifold|smooth manifold]] and $X \in \Gamma (TM)$ be a [[vector field|smooth vector field]]. Define the __interior product__ or __contraction__ as [[linear map]] $$\iprod:  \Omega^k (M) \to \Omega^{k-1} (M)$$ $$\omega \mapsto X \iprod \omega (X_1, \dots, X_{k-1}) = \omega(X, X_1, \dots, X_{k-1}).$$
Sometimes, $i_X \omega$ is written instead of $X \iprod \omega$.
```

**Remark.**
Let $X \in \Gamma(TM)$ be a [[vector field|smooth vector field]], $\omega_1 \in \Omega^k(M)$ and $\omega_2 \in \Omega^l(M)$. Then the identity $$X \iprod (\omega_1 \wedge \omega_2) = (X \iprod \omega_1) \wedge \omega_2 + (-1)^k \omega_1 \wedge (X \iprod \omega_2)$$ holds.