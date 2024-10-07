<div class="topSpace"></div>

Date Created: 
References: 
Tags: #Type/Definition

Proved by: [[atlas]], [[partition of unity]]
References: [[manifold#Riemannian manifolds]], [[metric tensor]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition (Existence of Riemannian Metrics).

On every [[manifold#Smooth Manifolds|smooth manifold]] exist [[metric tensor|Riemannian metrics]].

```

<i>Proof.</i>
The set of positive definite [[scalar product|scalar products]] on a [[vector space]] is convex. Let $\fA = \{(\phi_\alpha, U_\alpha\}_{\alpha \in I}$ be an [[atlas]] and $\{\rho_\alpha\}_{\alpha \in I}$ be a [[partition of unity]] subordinate to $\{U_\alpha \}_{\alpha \in I}$. Locally we obtain a metric by setting $g_\alpha = \phi_\alpha^\ast g_\text{st}$. Therefore, a [[metric tensor|Riemannian metric]] on $M$ is given by $$g := \sum_{\alpha \in I} \rho_\alpha g_\alpha.$$
<span style="float:right;">$\blacksquare$</span>

**Remark.**
For different [[bilinear map|signatures]], this construction failes because the set of [[scalar product|scalar products]] not being convex. The proposition is false in that case. For example, on the [[n-sphere]] $\S^n$ exist [[metric tensor|Lorentzian metrics]] only for uneven $n \geq 3$.