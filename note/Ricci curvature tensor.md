<div class="topSpace"></div>

Date Created: 15/10/24
References: #Ref/DiffGeo 
Tags: #Type/Definition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[torsion and curvature]], [[tensor field]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Ricci Curvature Tensor).

Let $(M,g)$ be a [[manifold#Riemannian manifolds|(pseudo-)Riemannian manifold]]. The __Ricci curvature tensor__ is a $(0,2)$-[[tensor field]] $$\text{Ric}_p: T_pM \times T_pM \to \R$$ $$\text{Ric}_p(Y,Z) = \tr[X \mapsto R_p(X,Y)Z] = g^{km}R_{kijm}.$$
The normalized quadratic form $$\text{ric}_p(v) := \frac{1}{(n-1) \|v\|_g^2} \text{Ric}_p (v,v)$$ is a mean of [[sectional curvature|sectional curvatures]] of planes containing $v$.

```

**Remarks.**
1. If $\{e_1, \dots, e_n\}$ is an orthonormal basis of $T_pM$ with respect to $g$, the Ricci tensor can be represented as $$\text{Ric}_p (u,v) = \sum_{i=1}^n g(R(e_i, u)v, e_i)$$ for $u,v \in T_p M$.
2. $\text{Ric}_p$ is a symmetric [[bilinear map]].

