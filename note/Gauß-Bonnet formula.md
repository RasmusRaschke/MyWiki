<div class="topSpace"></div>

Date Created: 
References: 
Tags: #Type/Definition

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[Euler characteristic|Triangulation]], [[Gaußian curvature]], [[geodesic curvature]], [[volume form]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Theorem
title: Theorem (Gauß-Bonnet Formula).

Let $(\Sigma, g)$ be an [[orientation|oriented]] Riemannian $2$-[[manifold#Riemannian manifolds|manifold]] and $D \sub \Sigma$ be the image of a smoothly [[submersion, immersion and embedding|embedded]] $n$-gon with interior angles $\beta_i$. Then
$$ \int_D K \mu_g + \int_{\partial_D} \kappa_{\partial D} \, dt = 2 \pi - \sum_{i=1}^n (\pi - \beta_i) = (2-n)\pi + \sum_{i=1}^n \beta_i$$
with the [[gaussian curvature]] $\tilde{K}$, the [[volume form]] $\mu_g$ and the [[geodesic curvature]] $\kappa$.
```

<i>Proof.</i>
Let $D \sub \Sigma$ be an $n$-gon like above. For $\epsilon > 0$ we shift every edge by $\epsilon$ orthogonally outwards and obtain the bigger domain $U_\epsilon \supseteq D$. Denote edge [[curve|curves]] by $\gamma_i$ and $\gamma_{i, \epsilon}$, respectively. Connect the vertices by circle segments. The rounded vertices are denoted $\delta_{i, \epsilon}$. The proposition yields $$\int_{U_\epsilon} K \mu_g + \int_{\partial U_\epsilon} \kappa_{\partial U_\epsilon} = 2\pi.$$ Now, we consider our extended domain: $$\int_D K \mu_g + \lim_{\epsilon \to 0} \sum_i \int_{\gamma_{i, \epsilon}} dt + \lim_{\epsilon \to 0} \sum_i \int_{\delta_{i, \epsilon}} \kappa_{\delta_{i, \epsilon}} \, dt = 2 \pi.$$ With $$\lim_{\epsilon \to 0} \sum_i \int_{\gamma_{i, \epsilon}} dt = \int_{\partial D} \kappa_{\partial D} dt$$ and $(\ast)$ from the [[total curvature theorem]], the theorem follows as $$\int_{\delta_{i, \epsilon}} \kappa_{\delta_{i, \epsilon}} \, dt = - \int_{\delta_{i, \epsilon}} \dot{\phi}(t) \, dt - \cancel{ \lim_{\epsilon \to 0} \int_{\delta_{i, \epsilon}} \omega} = \pi - \beta_i.$$
<span style="float:right;">$\blacksquare$</span>
