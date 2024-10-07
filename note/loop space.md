<div class="topSpace"></div>

Date Created: 06/10/24
References: #Ref/DiffGeo 
Tags: #Type/Definition #Topic/DifferentialGeometry #Topic/Topology 

Proved by: <i>Not Applicable</i>
References: [[parallel transport]], [[manifold]], [[covariant derivative]]
Justifications: [[parallel transport and curvature]]

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Smooth Loop Space).

Let $M$ be a [[manifold#Smooth Manifolds|smooth manifold]] with $p \in M$ and $\nabla$ be a [[covariant derivative]] on $TM$. The space 
$$\Omega_p M := \{\gamma: [0,1] \to M | \gamma \in \cC^\infty, \, \gamma(0) = \gamma(1) = p\} $$
is called __(smooth) loop space__ in $p$. The operation
$$\ast: \Omega_p M \times \Omega_p M \to \Omega_p M$$
$$(\gamma_1 \ast \gamma_2)(t) = \begin{cases} \gamma_1(2t), \ t \leq \frac{1}{2} \\ \gamma_2(2t-1), \ t > \frac{1}{2}\end{cases}$$
makes $\Omega_p M$ a [[monoid]].

```
**Remark.**
The [[parallel transport]] is therefore a mapping $$\Omega_p M \to \text{Gl}(T_pM)$$ $$\gamma \mapsto P^\gamma.$$

``` ad-Definition
title: Definition (Holonomy Group).

The image of the [[parallel transport]] as given above is a subgroup called __holonomy group__ $\text{Hol}_p (M, \nabla)$ of $\nabla$ in $p$. For [[connectedness|connected]] $M$ the holonomy groups $\text{Hol}_p$ and $\text{Hol}_q$ are conjugated (defining $\text{Gl}(T_pM) \cong \text{Gl}(n, \R) \cong \text{Gl}(T_qM)$ ).
The subset $\Omega_p^0M \sub \Omega_p M$ containes all contractable loops. With the same construction we obtain the __reduced holonomy group__ $\text{Hol}^0_p(M, \nabla) \sub \text{Hol}_p (M, \nabla)$. We have
$$\text{Hol}_p^0(M) = \{\id\} \iff R \equiv 0.$$ In that case the [[parallel transport]] descents to a [[homomorphism|group homomorphism]] $$\pi_1(M, p) \to \text{Gl} (T_pM).$$
```

**Remark.**
If there exists a parallel [[tensor field]] $B$ with respect to a [[covariant derivative]] $\nabla$ on $M$, the holonomy group $\text{Hol}_p$ is a subgroup of the automorphism group $\text{Aut}(B_p)$.