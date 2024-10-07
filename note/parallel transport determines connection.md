<div class="topSpace"></div>

Date Created: 06/10/24
References: #Ref/DiffGeo 
Tags: #Type/Proposition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[parallelity]], [[parallel transport]], [[vector field]], [[covariant derivative]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition (Parallel Transport determines Connection).

Let $M$ be a [[manifold#Smooth Manifolds|smooth manifold]]$, $\nabla$ be a [[covariant derivative|connection]] and $\gamma: [a,b] \to M$ be a [[curve|smooth curve]] with $t_0 \in [a,b]$. For $X \in \Gamma_\gamma (TM)$
$$\left( \nabla_\dt X\right)_{t_0} = \lim_{t \to t_0} \frac{(P_{t_0 t}^\gamma)^{-1} X_t - X_{t_0}}{t - t_0}$$
is satisfied.

```

<i>Proof.</i>
Let $Z_1, \dots, Z_n$ be a [[frame]] of [[parallelity#Parallel vector fields|parallel]] [[vector field along a map|vector fields]] along $\gamma$. We can write $X = \sum_{k=1}^n a_k Z_k$ and $\nabla_\dt X = \sum_{k=1}^n \frac{da_k}{dt}Z_k + \cancel{a_k \nabla_\dt Z_k}$. However, $(P_{t_0t}^\gamma)^{-1} X_t = \sum_{k=1}^n a_k(t)(Z_k)_{t_0}$. This leads to
$$ 
\lim_{t \to t_0} \frac{(P_{t_0 t}^\gamma)^{-1} X_t - X_{t_0}}{t - t_0} = \lim_{t \to t_0} \sum_{k=1}^n \left( \frac{a_k(t)-a_k(t_0)}{t-t_0}\right)(Z_k)_{t_0} = \left( \sum_k \frac{ da_k}{dt} Z_k\right)_{t_0} = \left( \nabla_\dt X\right)_{t_0}.
$$
<span style="float:right;">$\blacksquare$</span>