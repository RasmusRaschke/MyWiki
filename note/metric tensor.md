<div class="topSpace"></div>

Date Created: 06/10/24
References: #Ref/DiffGeo 
Tags: #Type/Definition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[manifold]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[tensor field]], [[bilinear map]]
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Pseudo-Riemannian Metric Tensor).
Let $M$ be a [[manifold#Smooth Manifolds|smooth manifold]]. A __pseudo-Riemannian metric__ on $M$ is a [[tensor field|smooth $(2,0)$-tensor field]] $g$ which is pointwise symmetric and non-degenerate. Furthermore, the [[bilinear map|signature]] is independent of $p \in M$.
If $g$ is [[positive definite]], it is called __Riemannian metric__.
If $g$ has [[bilinear map|signature]] $(1, n-1)$ or $(n-1,1)$, it is called __Lorentzian metric__.

```
**Examples.**
1. Let $(V, \langle ., . \rangle)$ be a [[vector space|real vector space]] with [[scalar product]]. The identification $T_vV \cong V$ allows the construction of a [[tensor field|$(2,0)$-tensor field]] $g$ such that $(V,g)$ is a pseudo-Riemannian [[manifold]].
2. Let $M \sub \R^n$ be a [[submanifold]]. The [[tangent space]] $T_pM \sub T_p \R^n$ is a linear subspace at all $p \in M$. Restricting the standard metric of $\R^n$ gives a Riemannian metric on $M$ depending on the [[submersion, immersion and embedding|embedding]] $M \hookrightarrow \R^n$. This only works for positive definite metrics.
3. Let $(M,g)$ be a [[manifold#Riemannian manifolds|Riemannian manifold]] and $\iota: N \hookrightarrow M$ be a [[submersion, immersion and embedding|immersion]]. The __pullback metric__ or __induced metric__ is given by $$h := \iota^\ast g(v,w) := g(\iota^\ast v, \iota^\ast w).$$ It defines a Riemannian metric on $N$.

**Remark.**
Let $(M,g)$ be a [[manifold#Riemannian manifolds|Riemannian manifold]]. On every [[tangent space]] $T_pM$ with $p \in M$ a [[norm]] is defined by $$\| v \|_g := \sqrt{g_p(v,v)}.$$

``` ad-Proposition
title: Proposition (Local Representation of the Metric Tensor).
Let $M$ be a [[manifold#Smooth Manifolds|smooth manifold]] and let $(x_1, \dots, x_n)$ be local coordinates on $U \sub M$. The metric tensor $g$ is uniquely determined by the component functions $$g_{ij}(p) = g(\partial_{x_i}|_p, \partial_{x_j}|_p).$$ Smoothness of a metric is equivalent to smoothness of the component functions.
```
