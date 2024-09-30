<div class="topSpace"></div>

Date Created: 30/09/24
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[atlas]], [[chart]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Orientation).

Let $M$ be a [[manifold|smooth manifold]]. $M$ is called __orientable__ if there exists an [[atlas]] $\fA = \{(U_\alpha, \phi_\alpha\}_{\alpha \in I}$ such that all chart transitions $\phi_{\alpha \beta}$ are orientation preserving [[diffeomorphism|diffeomorphisms]] of open subsets of $\R^n$. This means that the [[differential]] $\cD \phi_{\alpha \beta}$ has positive [[determinant]] everywhere.
An __orientation__ on $M$ is a selection of such an [[atlas]] with this property.

```

**Remarks.**
1. If $M$ is [[connectedness|connected]] and orientable there exist exactly two possible orientations on $M$.
2. $M$ is orientable iff there exists a global volume form $\omega \in \Omega^{\dim M}(M)$ with $\omega_q \neq 0$ for all $q \in M$. Any such volume form defines a [[vector bundle|trivialization]] $\Lambda^{\dim M}T^\ast M \cong \underline{R} = M \times \R$ and the other way around. 