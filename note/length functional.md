<div class="topSpace"></div>

Date Created: 09/10/24
References: #Ref/DiffGeo 
Tags: #Type/Definition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[curve]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Length and Length Functional).

Let $\gamma: [a,b] \to M$ be a [[curve]] on a [[manifold#Riemannian manifolds|Riemannian manifold]] $(M,g)$. The __length__ of $\gamma$ is defined by the __length functional__ $$L [\gamma] := \int_a^b \| \dot{\gamma}(t) \|_g \, dt.$$
```
**Remark.**
If $\gamma$ is only piecewise of class $\cC^1$, subdivide the interval $a  = t_0 < t_1 < \cdots < t_r =b$ such that $\gamma$ is $\cC^1$ on every subinterval $[t_i, t_{i+1}]$. Then the length is given by 
$$ L[\gamma] = \sum_{t_i \sub [a,b]} \int_{t_i}^{t_{i+1}} \| \dot{\gamma}(t) \|_g \, dt.$$

``` ad-Proposition
title: Proposition (Elementary Properties of the Length).

Let $(M,g)$ be a [[manifold#Riemannian manifolds|Riemannian manifold]]. Then the following statements are true:
1. For every (piecewise) [[curve|smooth curve]] $\gamma: [a,b] \to M$ the length satisfies $L[\gamma] \geq 0$ with equality iff $\gamma$ is constant.
2. For (piecewise) [[curve|smooth curves]] $\gamma_1: [a,b] \to M$ and $\gamma_2: [b,c] \to M$ with $\gamma_1(b) = \gamma_2(b)$ the length of $\gamma_1 \ast \gamma_2: [a,c] \to M$ is given by $$L[\gamma_1 \ast \gamma_2] = L[\gamma_1] + L[\gamma_2].$$
3. For any [[diffeomorphism]] $\phi: [a', b'] \to [a,b]$, the length of $\gamma: [a,b] \to M$ is invariant under $\phi$: $$L [\phi \circ \gamma] = L[\gamma].$$
```

**Remark.**
$\phi$ being monotonous, smooth and surjective is sufficient for the third property.