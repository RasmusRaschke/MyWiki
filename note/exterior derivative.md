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
title: Definition (Exterior Derivative).

The __exterior derivative__ $d: \Omega^k(Q) \to \Omega^{k+1} (Q)$ is a mapping characterized by the following three properties:
1. Let $f \in \cC^\infty (Q, \R)$. Then the exterior derivative of $f$ is given by $df = f^\ast dt$ with the standard $1$-form $dt$ on $\R$. Therefore, we also have $df(X) = X(f)$ for a [[vector field]] $X$.
2. For all $\eta_1, \eta_2 \in \Omega^k(Q)$ the equation $$d(\eta_1 \wedge \eta_2) = (d\eta_1) \wedge \eta_2 + (-1)^{\deg \eta_1} \eta_1 \wedge d\eta_2$$ holds.
3. $$d^2 \eta = 0$ for all $\eta \in \Omega^k(Q)$.

```

**Remark.**
Let $\eta \in \Omega^1(M)$ and $X, Y \in \Gamma (TM)$. Then the identity $$d\eta (X,Y) = X(\eta(Y)) - Y(\eta(X)) - \eta([X,Y])$$ is satisfied.