<div class="topSpace"></div>

Date Created: 14/04/25
References: #Ref/AlgTop 
Tags: #Type/Proposition #Topic/AlgebraicTopology 

Proved by: <i>Not Applicable</i>
References: [[homology#Singular Homology]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[homology]]
Examples: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition (Paths and Chain Complexes).

Let $\omega_1, \omega_2, \omega_3$ be paths in the path-connected [[topological space]] $X \neq \emptyset$.
(a) Constant paths are [[homology|null-homologous]].
(b) If $\omega_1(1) = \omega_2(0), then $\omega_1 \ast \omega_2 - \omega_1 - \omega_2$ is a boundary.
(c) If $\omega_1(0) = \omega_2(0)", $\omega_1(1)  =\omega_2(1)$ and if $\omega_1$ is homotopic relative to $\{0,1\}$, then $\omega_1$ and $\omega_2$ are [[homology|homologous]] as singular $1$-chains.
(d) Any $1$-chain of the form $\overline{\omega} \ast \omega$ is a boundary.

```

*Proof.*

(a) We consider the constant singular $2$-simplex $\alpha(t_0, t_1, t_2) = x$ and $c_x$, the constant path. Then:
$$\partial \alpha = c_x - c_x + c_x  = c_x.$$
(b) Define a singular $2$-simplex $\beta: \Delta^2 \to X$ as
![[simplexb.png]]
We define $\beta$ on the boundary components of $\Delta^2 as above and prolong it constantly along the inner lines. Then:
$$
\partial \beta = \beta d_0 - \beta d_1 + \beta d_2 = \omega_2 - \omega_1 \ast \omega_2 + \omega_1.
$$
(c) Let $H: [0,1] \times [0,1] \to X$ be a homotopy from $\omega_1$ to $\omega_2$. Since $H(0,t) = \omega_1(0) = \omega_2(0)$, we can factor through the quotient $[0,1] \times [0,1]/\{0\} \times [0,1] \cong \Delta^2$ with induced map $h: \Delta^2 \to X$. Then:
$$
\partial h = h d_0 - h d_1 + h d_2.
$$
The first summand has value $\omega_1(1) = \omega_2(1)$ and is therefore constant. The second one is $\omega_2$, the last one $\omega_1$. This makes $\omega_1 - \omega_2$ [[homology|null-homologous]].
(d) Follows directly by considering
![[simplexc.png]]
<span style="float:right;">$\blacksquare$</span>