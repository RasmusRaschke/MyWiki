<div class="topSpace"></div>

Date Created: 06/10/24
References: #Ref/DiffGeo 
Tags: #Type/Definition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[fundamental theorem of pseudo-Riemannian geometry]], [[manifold#Riemannian manifolds]], [[covariant derivative]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Geodesic).

Let $(M,g)$ be a [[manifold#Riemannian manifolds|pseudo-Riemannian manifold]] and $\nabla$ be the [[fundamental theorem of pseudo-Riemannian geometry|Levi-Civita connection]] of $g$. A [[curve]] $\gamma: [a,b] \to M$ is called __geodesic__ if $$\nabla_\dt \dot{\gamma} = 0.$$

```

**Example.**
In $(\R^n, g_\text{st})$ $\nabla_\dt \dot{\gamma} = \ddot{\gamma}$ holds. Therefore, geodesics are of the form $$\gamma(t) = p + tv$$ for $p, v \in \R^n$.

**Remark.**
An [[isometry]] $\phi$ between $(M,g)$ and $(N,h)$ maps geodesics to geodesics. If $F \sub M$ is the set of fixed points of $\phi: (M,g) \to (M.g)$ and if $\gamma: (a.b) \to M$ is a geodesic which is tangential to $F$ at one point $p = \gamma(t_0)$ ($\dot{\gamma}(t_0) \in T_pF \sub T_p M$), the image of $\gamma$ is completely contained in $F$.

<i>.</i><span style="float:right;">$\blacksquare$</span>