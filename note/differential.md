<div class="topSpace"></div>

Date Created: 20/09/24 
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[tangent space]], [[smooth mapping]], [[chain rule]]
Justifications: <i>Not Applicable</i>

Specializations: [[differential in Rn]]
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Differential).

Let $M, N$ be [[manifold|smooth manifolds]] and $F: M \to N$ be a [[smooth mapping]] between them. The __differential__ or __pushforward__ of $F$ in $p \in M$ is the [[linear map]] 
$$F_{\ast, p}: T_pM \to T_{F(p)}N$$
$$v \mapsto F_{\ast, p} (v),$$
given by $F_{\ast, p}(v)(f) = v(f \circ F)$ for all $f \in \cC^\infty (N, \R)$.
```
