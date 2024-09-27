<div class="topSpace"></div>

Date Created: 20/09/24
References: 
Tags: #Type/Proposition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition (Chain Rule for Manifolds).

Let $M_1, M_2$ and $M_3$ be [[manifold|smooth manifolds]] and $F: M_1 \to M_2$ as well as $G: M_2 \to M_3$ be [[smooth mapping|smooth mappings]]. Then the chain rule
$$ (G \circ F)_{\ast, p} = G_{\ast, F(p)} \circ F_{\ast, p}$$
is satisfied.
```

<i>Proof.</i>
Consider an arbitrary $f \in \cC^\infty (M_3, \R)$. The established rules for the [[differential]] lead to:
$$
G_{\ast, F(p)} \circ F_{\ast, p}(v)(f) = F_{\ast, p} (v)(f \circ G)= v(f \circ (G \circ F)) = (G \circ F)_{\ast, p} (v)(f).
$$