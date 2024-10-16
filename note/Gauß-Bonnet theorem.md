<div class="topSpace"></div>

Date Created: 15/10/24
References: #Ref/DiffGeo 
Tags: #Type/Theorem #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[volume form]], [[submanifold]], [[metric tensor]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Theorem
title: Theorem (of Gauß-Bonnet).

Let $\Sigma$ be a closed, [[orientation|oriented]] $2$-[[manifold]] and $g$ be a [[metric tensor|Riemannian metric]]. In addition, let $\mu_g \in \Omega^2 (\Sigma)$ be the [[volume form]] and $\tilde{K}: \Sigma \to \R$ be the [[gaussian curvature]]. Then, $$\int_\Sigma K \mu_g = 2 \pi \chi(\Sigma),$$ where $\chi(\Sigma)$ is the [[Euler characteristic]] of $\Sigma$.

```

<i>Proof.</i>
The proof is quite simple using the [[Gauß-Bonnet formula]]. Let $D \sub \Sigma$ be the image of a smoothly [[submersion, immersion and embedding|embedded]] $n$-gon with interior angles $\beta_i$. The equation can be shown by direct calculation:
$$
\int_\Sigma K \mu_g = \sum_{D_i \in T} \int_{D_i} K \mu_g = \sum_i \left( \sum_{j=1}^3 \beta_{ij} - \pi \right) - \cancel{\sum_i \int_{\partial D_i} \kappa_{\partial D}} = 2\pi V(T) - F(T) - \pi = 2 \pi (V(T)- \underbrace{\frac{3}{2} F(T)}_{E(T)} + F(T)) = 2 \pi \chi(\Sigma).
$$
The integral $\sum_i \int_{\partial D_i} \kappa_{\partial D}$ vanishes as every chart is contained in exactly two triangles with opposing borders.
<span style="float:right;">$\blacksquare$</span>