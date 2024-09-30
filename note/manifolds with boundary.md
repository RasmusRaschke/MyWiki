<div class="topSpace"></div>

Date Created: 30/09/24
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[manifold]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[manifold]]

``` ad-Definition
title: Definition (Manifold with Boundary).

Let $X$ be a [[Hausdorff property|Hausdorff space]] with a countable [[basis]]. If every point $p \in X$ has a neighbourhood [[homeomorphism|homeomorphic]] to an open subset of $$\R^n_- := \{x = (x_1, \dots, x_n) \in \R^n | x_1 \leq 0\}$$, $X$ is called __topological manifold with boundary__.
A __boundary point__ of $X$ is a point which is homeomorphic to $\{0\} \times \R^{n-1}$. $\partial X$ is called __boundary__ of $X$ and consists of all __boundary points__.

```

**Remarks.**
Certain definitions carry over:
1. Let $U, V \sub \R^n_-$ be open subsets. A mapping $f: U \to V$ is called __smooth__ if there exist open subsets $\tilde{U}, \tilde{V} \sub \R^n$ and a [[smooth mapping]] $\tilde{f}: \tilde{U} \to \tilde{V}$ such that $\tilde{f}|_U = f$.
2. A manifold with boundary $X$ is called __smooth__ if there exists an [[atlas]] such that all chart transitions are [[diffeomorphism|diffeomorphisms]] of open subsets of $\R^n_-$.

**Remark.**
Let $p \in \partial X$. Then $T_p \partial X \sub T_p X$ is a subspace of codimension $1$. A outward oriented vector in $T_pX$ is a $v \in T_pX$ which gets mapped to a vector with positive component in $\frac{\partial}{\partial x_1}$-direction by the [[differential]] of the [[chart]] $\phi: U \to \R^n_-$.
If $X$ is oriented, this induces an [[orientation]] on $\partial X$ in the following way.  $(v_2, \dots, v_n) \in T_p \partial X$ is [[orientation|oriented]] positively iff for an outward directed vector $v \in T_pX$ a positively oriented [[basis]] is given by $(v, v_2, \dots, v_n)$.