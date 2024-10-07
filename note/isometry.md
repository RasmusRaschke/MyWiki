<div class="topSpace"></div>

Date Created: 06/10/24
References: #Ref/DiffGeo 
Tags: #Type/Definition #Topic/LinearAlgebra

Proved by: <i>Not Applicable</i>
References: [[manifold#Riemannian manifolds]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[diffeomorphism]]
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Isometry).

An __isometry__ between [[manifold#Riemannian manifolds|(pseudo-)Riemannian manifolds]] $(M,g)$ and $(N,h)$ is a [[diffeomorphism]] $$\phi: M \to N$$ such that $\phi^\ast h = g$ with $\phi^\ast h (v,w) := h(\phi_\ast(v), \phi_\ast (w))$. 
Isomorphisms between $(M,g)$ and itself form a [[group]] called __isometry group__ $\iso (M,g)$.

```

**Remark.**
Oftentimes, $\iso (M,g)$ consists only of the identity $\id: M \to M$. Interesting examples can have very big isometry groups, however.

**Examples.**
1. Let $\S^n \sub \R^{n+1}$ be the [[n-sphere|$n$-sphere]] with the of $g_\text{st}$ on $\R^{n+1}$ induced metric $g$ called __round metric__. Every linear isometry of $(\R^{n+1}, \langle .,. \rangle)$ preserves $\S^n$ and induces a isometry $\S^n \to \S^n$. Therefore, $\iso (\S^n) \cong \OO (n+1)$.
2. In $(\R^2, g_\text{st})$, every translation is a isometry. If $v,w \in \R^2$ are linearly independent vectors, they span a lattice $$\Lambda := \{nv + m w | n,m \in \Z} \cong \Z^2.$$ The [[quotient space]] $\R^2 \diagup \Z^2 \cong \T^2$ is a $2$ dimensional [[n-Torus|torus]]. The standard metric $g_\text{st}$ on $\R^2$ induces a on $\Lambda$ dependent metric $g$ on $\T^2$ because of the fact that translations are isometries. Every translation in $\R^2$ descends to an isometry for every single [[n-Torus|torus]]. The symmetry group of those [[n-Torus|tori]] is therefore still transitive on every [[n-Torus|torus]].
3. Embedding a [[n-Torus|torus]] as boundary of a doughnut in $\R^3$ gives a completely different metric.