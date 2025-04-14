<div class="topSpace"></div>

Date Created: 14/04/25
References: #Ref/AlgTop 
Tags: #Type/Definition #Topic/AlgebraicTopology 

Proved by: [[first homology group]]
References: [[homology#Singular Homology]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Hurewicz Homomorphism).
The map $h: \pi_1 (X,x) \to H_1(X)$$ that sends homotopy classes $[\omega]_{\pi_1}$ of closed paths $\omega$ to homology classes $[\omega]= [\omega]_{H_1}$ is called <ins>Hurewicz homomorphism</ins>.

```

The well-definedness of this map is given by our considerations of paths and homology in [[first homology group]]. This also yields
$$
h([\omega_1][\omega_2])=h([\omega_1 \ast \omega_2]) = [\omega_1] + [\omega_2] = h([\omega_1]) + h([\omega_2]).
$$
For closed paths, $[\overline{\omega}] = -[\omega]$ holds in $H_1(X)$.

