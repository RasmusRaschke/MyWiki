<div class="topSpace"></div>

Date Created: 02/10/24 
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[vector bundle]], [[vector field]], [[manifold]], [[section]], [[covariant derivative]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>


# Parallel sections 

``` ad-Definition
title: Definition (Parallelity).

Let $E \to B$ be a [[vector bundle]] and $\nabla$ a [[covariant derivative]] on $E$. A [[section]] $s: B \to E$ is called __parallel__ if $$\nabla_X s =0$$ for all [[vector field|vector fields]] $X \in \Gamma (TB)$.

```

**Remarks.**
1. In general, many [[covariant derivative|connections]] have no parallel [[section|sections]] at all.
2. The previously defined [[covariant derivative|connections]] have many parallel [[section|sections]], namely all linear combinations of global [[section|sections]] with coefficients $c_i \in \R$.


# Parallel vector fields

``` ad-Definition
title: Definition (Parallel Vector Fields).

Let $M$ be a [[manifold|smooth manifold]], $\gamma: [a.b] \to M$ be a smooth [[curve]] and $\nabla$ be a [[covariant derivative]] on $TM$. A [[vector field]] $Y \in \Gamma_\gamma (TM)$ is called __parallel__ if $$\nabla_{\frac{d}{dt}}Y = 0$$ is satisfied.
The local representation of this condition reads as
$$ \nabla_{\frac{d}{dt}} Y = \sum_{k=1}^n \left( \frac{da_k}{dt} + \sum_{i,j} a_j \frac{d(x_i \circ \gamma)}{dt} (\Gamma^k_{ij} \circ \gamma) \right) (\partial_{x_k} \circ \gamma)$$
for $Y|_{(t_0-s, t_0+s)} = \sum_{k=1}^n a_k (\partial_{x_k} \circ \gamma)$ and $a_k: (t_0 -s, t_0 +s) \to \R$.
```
<i>Proof (local representation).</i>
Let $t_0 \in [a,b]$. On a neighbourhood $U \sub M$ of $\gamma(t_0)$, local coordinates are given by $(x_1, \dots, x_n)$. For $Y \in \Gamma_\gamma (TM)$ we therefore obtain the local representation $$Y|_{t_0-s, t_0+s)} = \sum_{k=1}^n a_k (\partial_{x_k} \circ \gamma).$$ With this the [[covariant derivative]] is given by
$$\nabla_{\frac{d}{dt}} Y = \sum_{k=1}^n \left( \frac{da_k}{dt} \right) \cdot (\partial_{x_k} \circ \gamma) + \sum_{j=1}^n a_j \nabla_{\frac{d}{dt}} (\partial_{x_j} \circ \gamma).$$
With $\gamma_\ast \left( \frac{d}{dt} \right) = \sum_i \frac{d(x_i \circ \gamma)}{dt} \partial_{x_i}$ we obtain
$$\nabla_{\frac{d}{dt}} (\partial_{x_j} \circ \gamma) = \left( \nabla_{\gamma_\ast \left( \dt \right)} \partial_{x_j} \right) \circ \gamma = \sum_{i=1}^n \frac{d(x_i \circ \gamma)}{dt} \left( \nabla_{\partial_{x_j}} \partial_{x_j} \right) \circ \gamma = \sum_{i,k} \frac{d (x_i \circ \gamma)}{dt} \cdot \left( \Gamma^k_{ij} \circ \gamma \right) \left( \partial_{x_k} \circ \gamma \right).$$
Putting everything together we obtain
$$\nabla_{\frac{d}{dt}} Y = \sum_{k=1}^n \left( \frac{da_k}{dt} + \sum_{i,j} a_j \frac{d(x_i \circ \gamma)}{dt} (\Gamma^k_{ij} \circ \gamma) \right) (\partial_{x_k} \circ \gamma)$$ as proposed.
<span style="float:right;">$\blacksquare$</span>

