<div class="topSpace"></div>

Date Created: 16/10/24
References: #Ref/DiffGeo 
Tags: #Type/Definition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[metric tensor]], [[curve]], [[vector field]], [[fundamental theorem of pseudo-Riemannian geometry]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Geodesic Curvature).

Let $(\Sigma, g)$ be an [[orientation|oriented]] [[manifold#Riemannian manifolds|Riemannian $2$-manifold]], $\nabla$ be the [[fundamental theorem of pseudo-Riemannian geometry|Levi-Civita connection]], $\gamma: [0,b] \to \Sigma$ be a [[curve|smooth curve]] parametrized with unit speed $\| \dot{\gamma}(t) \|_g = 1$ and $N$ be a [[vector field]] normal to $\gamma$ such that $(\dot{\gamma}(t), N_t)$ is an oriented orthonormal basis of $T_{\gamma(t)}\Sigma$. Then the __geodesic curvature__ of $\gamma$ is defined by $$\kappa_N (t) := g(\nabla_\dt \dot{\gamma}(t), N_t).$$

```

``` ad-Proposition
title: Proposition (Existence of Normal Field).

Using the same setting as above, the normal [[vector field]] $N$ such that $(\dot{\gamma}(t), N_t)$ form an orthonormal basis of $T_{\gamma(t)}\Sigma$ always exists and is unique. Furthermore, the equation $$\nabla_\dt \dot{\gamma} = \kappa_\gamma \cdot N$$ holds. 

```

<i>Proof.</i>
TBD.
<span style="float:right;">$\blacksquare$</span>

**Remarks.**
1. $\gamma$ is a [[geodesic]] if and only if $\kappa_\gamma =0$. The geodesic curvature measures the deviation of $\gamma$ from being a [[geodesic]].
2. For $\dot{\gamma} = \gamma(b-t)$ we have $\dot{\hat{\gamma}} (t) = - \dot{\gamma}(b-t)$, $\hat{N}_t = -N_{b-t}$ and $\left( \nabla_\dt \dot{\hat{\gamma}}\right)_t = \left( \nabla_\dt \dot{\gamma}\right)_{b-t}$. Therefore, $\kappa_{\hat{\gamma}} (t) = - \kappa_\gamma (b-t)$.