<div class="topSpace"></div>

Date Created: [[21/04/2025]]
References: #Ref/LeeSmooth 
Tags: #Type/Definition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Definition

``` ad-Definition
title: Definition (Unit Sphere).

For some $n \geq 0$, define the <ins>$n$-dimensional unit sphere</ins>
$$
\S^n := \{x \in \R^{n+1} \mid \|x\|=1\} \sub \R^{n+1}.
$$

```

# Manifold

``` ad-Proposition
title: Proposition (Spheres are Manifolds).
The unit sphere $\S^n$ is for all $n\geq 0$ a $n$-dimensional [[manifold#Topological Manifold|manifold]].

```
*Proof.*
As a subspace of $\R^{n+1}$, all unit spheres are Hausdorff and second countable. For each $0 \leq i \leq n+1$, define
$$
U_i^{\pm} := \{(x^1, \dots, x^{n+1}) \mid x^i \gtrless 0\} \sub \R^{n+1}
$$
and consider the continuous function $f(u)= \sqrt{1- |u|^2}$.