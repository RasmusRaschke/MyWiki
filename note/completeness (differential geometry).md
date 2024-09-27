<div class="topSpace"></div>

Date Created: 25/09/24
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[vector field]], [[integral curve]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Completeness (Differential Geometry)).

A [[vector field]] $X$ on a [[manifold|smooth manifold]] $M$ is called __complete__ if $$\sD_X = M \times \R.$$ This means that for every $p \in M$ a maximal [[integral curve]] through $p$ for all times $t \in \R$ is defined.

```

**Remarks.**
1. The local theory of [[ode|odes]] yields that every [[vector field]] on a [[compact]], [[borderless]] [[manifold]] is complete.
2. Every [[vector field]] with [[support|compact support]] is complete.

**Examples.**
1. On $M = \R^2$ we define $$X_{(x,y)} := x \frac{\partial}{\partial y} - y \frac{\partial}{\partial x}.$$ This [[vector field]] is complete with $$\Phi \left( \begin{pmatrix} x \\ y \end{pmatrix}, t\right) = \begin{pmatrix} \cos t & - \sin t \\ \sin t & \cos t \end{pmatrix} \begin{pmatrix} x \\ y \end{pmatrix}.$$ However, upon removing a subset $A \sub \R^2$, the restriction of $X$ on $\R^2 \times A$ is no longer complete.
2. Let $M \sub \S^2 \sub \R^3$ and choose one $v \in \S^2$. Define [[vector field|vector fields]] $X$ and $Y$ on $\S^2$ by $X_p := v \times p$ and $Y_p := X_p \times p = (v \times p) \times p$.