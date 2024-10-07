<div class="topSpace"></div>

Date Created: 06/10/24
References: #Ref/DiffGeo
Tags: #Type/Definition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[vector field along a map]], [[parallelity]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Parallel Transport).

Let $\gamma: [a,b] \to M$ be a smooth [[curve]] on a [[manifold|smooth manifold]] $M$ with $t_0, t_1 \in [a,b]$. Let $v \in T_{\gamma(t_0)} M$ be a [[tangent space|tangent]] vector and $V \in \Gamma_\gamma (TM)$ be a [[parallelity|parallel]] [[vector field]] with $V(t_0) = v$. The __parallel transport__ is an [[isomorphism]]
$$P^\gamma_{t_0t_1}: T_{\gamma(t_0)}M \to T_{\gamma (t_1)}M$$
$$v \mapsto V(t_1).$$

```
**Remark.**
$$P^\gamma_{t_0t_1}  = (P^\gamma_{t_1t_0})^{-1}$$

# A different view of the parallel transport

The parallel transport along $\gamma: [a,b] \to M$ gives a curve $Y: [a,b] \to TM$ with $Y(a) =v$ and $\pi_M \circ Y = \gamma$ for every initial value $v \in T_{\gamma(a)}M$. For every tangent vector $w \in T_pM$ we obtain a $Y$ with inital value $v \in TM$ and a [[linear map]] $$T_pM \to T_v(TM)$$ $$w \mapsto \dot{Y}_w (0).$$ The image is given as $n$-dimensional subspace $H_v \sub T_v(TM)$ such that $\pi_{\ast, M}$ maps $H_v$ [[isomorphism|isomorphically]] on $T_pM$. The family $\{ H_v \sub T_v(TM)\}_{v \in TM}$ containes all information about $\nabla$.
Now consider $Y \in \Gamma (TM)$ as map $Y: M \to TM$ with $Y_\ast (X)_x \in T_{Y_x} TM$. Furthermore, cosider the decomposition $T_v(TM) = V_v \oplus H_v$ with $V_v \cong T_pM$.
Then, this yields the preposition that $$(\nabla_X Y)_X = pr_V (Y_{\ast, X} (X))$$ which is indeed true. Therefore, the [[covariant derivative]] defines a projection of the normal derivative onto fibers. 