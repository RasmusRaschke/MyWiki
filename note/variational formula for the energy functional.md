<div class="topSpace"></div>

Date Created: 14/10/24
References: #Ref/DiffGeo 
Tags: #Type/Proposition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[energy functional]], [[curve]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# First Variational Formula

``` ad-Proposition
title: Proposition (First Variational Formula).

Let $(M,g)$ be a [[manifold#Riemannian manifolds|Riemannian manifold]], $\gamma: [0,1] \to M$ a [[curve|smooth curve]] and $V \in \Gamma_\gamma (TM)$ be a [[vector field along a map|vector field]]. Then, the first variational formula of the [[energy functional]] holds:
$$dE_\gamma [V] = \int_0^1 g(V, \nabla_\dt \dot{\gamma}) \, dt + g(V_1, \dot{\gamma}(1)) - g(V_0, \dot{\gamma}(0)).$$
```

<i>Proof.</i>
Let $\Gamma: (-\epsilon, \epsilon) \times [0,1] \to M$ be a [[curve|variation]] with $\frac{\partial \Gamma}{\partial s}|_{s=0} = \Gamma_\ast (\partial_s)|_{s=0} = V$. Then we have
$$
\begin{align*}
dE_\gamma[V] &= \frac{d}{ds} E[\gamma_s]|_{s=0} = \frac{1}{2} \int_0^1 \frac{d}{ds} g(\Gamma_\ast (\partial_t), \Gamma_\ast (\partial_t))|_{s=0} \, dt = \int_0^1 g(\nabla_{\frac{d}{ds}} \Gamma_\ast (\partial_t), \Gamma_\ast (\partial_t))|_{s=0} \, dt \\
&= \int_0^1 g(\nabla_\frac{d}{dt} \Gamma_\ast (\partial_s), \Gamma_\ast (\partial_t))|_{s=0} \, dt = \int_0^1 \frac{d}{dt} g(\Gamma_\ast \partial_s, \Gamma_\ast \partial_t)|_{s=0} - g(\Gamma_\ast \partial_s, \nabla_\dt \Gamma_\ast \partial_t)|_{s=0} \, dt \\
&= g(V_1, \dot{\gamma}(1)) - g(V_0, \dot{\gamma}(0)) - \int_0^1 g(V, \nabla_\dt \dot{\gamma}) \, dt.
\end{align*}
$$
We used that $\nabla$ is [[fundamental theorem of pseudo-Riemannian geometry|torsion free]].
<span style="float:right;">$\blacksquare$</span>

**Remark.**
From this formula follows that $\gamma$ is a critial point of $E: \Omega_{p,q} \to \R$ iff $\gamma$ is a [[geodesic]].

# Second Variational Formula

``` ad-Proposition
title: Proposition (Second Variational Formula).

Let $(M,g)$ be a [[manifold#Riemannian manifolds|Riemannian manifold]], $\gamma: [0,1] \to M$ a [[geodesic]]. If $\Gamma: (-\epsilon, \epsilon) \times [0,1] \to M$ is a [[curve|variation]] of $\gamma$ with fixed end points in direction of the [[vector field]] $V$, the second variational formula holds:
$$\frac{d^2}{ds^2} E[\gamma_s]|_{s=0} = - \int_0^1 g(\nabla_\dt \nabla_\dt V + R(V, \dot{\gamma})\dot{\gamma}, V) \, dt .$$

```

<i>Proof.</i>
The first variational formula yields $$\frac{d}{ds} E[\gamma_s] = - \int_0^1 (\Gamma_\ast \partial_s, \nabla_\dt \Gamma_\ast \partial_t) \, dt .$$ Boundary terms vanish as we keep the end points of the variation fixed. Therefore, $$\frac{d^2}{ds^2} E[\gamma_s] = - \int_0^1 g(\nabla_\frac{d}{ds} \Gamma_\ast \partial_s, \nabla_\dt \Gamma_\ast \partial_t) \, dt - \int_0^1 g(\Gamma_\ast \partial_s, \nabla_\frac{d}{ds} \nabla_\frac{d}{dt} \Gamma_\ast \partial_t) \, dt.$$ Because $\gamma = \gamma_0$ is a [[geodesic]], the first term vanishes in $s=0$. From $$R(\Gamma_\ast \partial_s, \Gamma_\ast \partial_t)\Gamma_\ast \partial_t = \nabla_\frac{d}{ds} \nabla_\dt \Gamma_\ast \partial_t - \nabla_\dt \nabla_\frac{d}{ds} \Gamma_\ast \partial_t$$ follows $$\frac{d^2}{ds^2}E[\gamma_s]|_{s=0} = - \int_0^1 g(R(V, \dot{\gamma})\dot{\gamma}, V) + g(V, \nabla_\dt \nabla_\frac{d}{ds} \Gamma_\ast \partial_t) \, dt = -\int_0^1 g(\nabla_\dt \nabla_\dt V + R(V, \dot{\gamma})\dot{\gamma}, V) \, dt .$$
<span style="float:right;">$\blacksquare$</span>

**Remark.**
The proof also works for $\gamma(0) = \gamma(1)$, $\dot{\gamma}(0) = \dot{\gamma}(1)$ and $V_0 = V_1$, so a [[curve|variation]] of a closed [[geodesic]] in the [[curve|space of closed curves]] is also valid.