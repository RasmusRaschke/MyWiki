<div class="topSpace"></div>

Date Created: 14/10/24
References: #Ref/DiffGeo 
Tags: #Type/Theorem #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[sectional curvature]], [[orientation]], [[connectedness]]
Justifications: [[variational formula for the energy functional]], [[Hopf and Rinows theorem]]

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Theorem
title: Theorem (Synge's Theorem).

Let $(M,g)$ be a [[manifold#Riemannian manifolds|Riemannian manifold]] with the following properties:
1. $M$ is closed (compact without boundary).
2. $\dim M$ is even.
3. All [[sectional curvature|sectional curvatures]] are positive.
4. $M$ is [[orientation|orientable]].

Then, $M$ is [[connectedness|simply connected]] and therefore, every map $\gamma: \S^1 \to M$ is null-homotopic.

```

<i>Proof.</i>
The proof is only outlined:
Propose thet in every (non-trivial) free homotopy class of [[curve|curves]] $\gamma: \S^1 \to M$ exists a shortest [[curve]] which is also a closed [[geodesic]].
Let $\gamma$ be such a [[geodesic]] and consider the [[parallel transport]] along it. Because $$P_{\gamma(0) \gamma(1)}: T_{\gamma(0)}M \to T_{\gamma(1)}M = T_{\gamma(0)}M$$ is an [[isometry]] we have $$P_{\gamma(0) \gamma(1)}(\dot{\gamma}(0)) = \dot{\gamma}(0).$$ Therefore, the [[parallel transport]] maps the [[linear subspace]] $\dot{\gamma}(0)^\perp \sub T_{\gamma(0)} M$ [[isometry|isometrically]] and [[orientation]]-preserving onto itself. Because $\dot{\gamma}^\perp$ has uneven dimension, there exists a vector $v \perp \dot{\gamma}(0)$, $v \neq 0$ such that $P_{\gamma(0) \gamma(1)}v = v$. Let $V \in \Gamma_\gamma (TM)$ be the [[parallelity|parallel]]  [[vector field along a map|vector field along $\gamma$]] with $V_0 = v$. Then the [[variational formula for the energy functional#Second Variational Formula|second variational formula]] yields $$\frac{d^2}{ds^2}E[\gamma_s]|_{s=0} = - \int_0^1 g(V, R(V, \dot{\gamma})\dot{\gamma}) \, dt - \int_0^1 g(V, \nabla_\dt \nabla_\dt V) \, dt = - \int_0^1 K(\span \{ V_t, \dot{\gamma}(t) \}) \, dt.$$ Thus, $\gamma$ is no local minimum of the [[energy functional]] in contradiction with our assumption. 
<span style="float:right;">$\blacksquare$</span>

**Remarks.**
1. The [[projective spaces|real projective space]] $\R P^2$ shows why [[orientation|orientability]] is crucial. $\R P^3$ shows that even dimension of $M$ is needed.
2. The Hopf conjecture is still unsolved: Exists a Riemannian metric with positive sectional curvature on $\S^2 \times \S^2$?