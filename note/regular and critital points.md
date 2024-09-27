<div class="topSpace"></div>

Date Created: 22/09/24
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[preimage theorem]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Regular and Critical Points).

Let $M$ and $N$ be [[manifold|smooth manifolds]] and $F: M \to N$ be a [[smooth mapping]]. 
A point $p \in M$ is called __regular__ for $F$ if $F_{\ast, p}: T_pM \to T_{F(p)}N$ is surjective. If this is not the case, $p$ is called __critical__ for $F$.
A point $q \in N$ is called __regular value__ of $F$ if $F^{-1}(q)$ contains only regular points. If $F^{-1}(q)$ contains at least one critical point, $q$ is called __critical value__.

```

**Example.**
Let $f: \R \to \R$, $x \mapsto x^3$ be a [[smooth mapping]]. Because $f'(0)=3 \cdot 0^2 = 0$, $p=0$ is a critical value of $f$.