<div class="topSpace"></div>

Date Created: 25/09/24
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[vector bundle]], [[section]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Vector Fields).

A __smooth vector field__ on a [[manifold|smooth manifold]] $M$ is a [[sections|smooth section]] in the [[tangent bundle]] $\pi: TM \to M$ of $M$.
```
**Remarks.**
1. Let $p: E \to B$ be a [[vector bundle]] and $S \sub B$ be a [[submanifold]]. Then $$p|_{p^{-1}(S)} : p^{-1}(S) (=:E|_S) \to S$$ is another smooth [[vector bundle]].
2. Let $M$ be a [[manifold|smooth manifold]] and $\phi: U \to V \sub \R^n$ be a [[chart|local chart]] with coordinates $(x_1, \dots, x_n)$. The mapping $$\frac{\partial}{\partial x_i}: U \to TM|_U = TU$$ $$p \mapsto \left. \frac{\partial}{\partial x_i}\right|_p$$ defines a smooth local vector field for all $i \in \{1, \dots, n\}$. In the by the [[chart]] $\phi: U \to V$ defined [[vector bundle|local trivialization]] $\psi: TM|_U \to TV = V \times \R^n$ the vector field $\frac{\partial}{\partial x_i}$ is the constant vector field $$p \mapsto (\phi(p), (0, \dots, 0, 1, 0, \dots, 0)).$$ In every $p \in U$ the vectors $\left\{ \left.\frac{\partial}{\partial x_i}\right|_p\right\}_{i \leq n}$ are a [[basis]] of $T_pM$. Therefore, every on $U$ defined vector field is given by a linear combination of $\left\{ \left.\frac{\partial}{\partial x_i}\right|_p\right\}_{i \leq n}$ with coefficients in $\cC^\infty(U, \R)$.

**Example.**
Let $U \sub M$ be an open subset. Then, $TM|_U = TU$. However, if $S \sub M$ has positive codimension ($\dim S < \dim M$), $TM|_S$ and $TS$ are different because of their different rank.