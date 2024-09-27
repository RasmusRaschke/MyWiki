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
title: Proposition (Taylor Expansion (Differential Geometry)).

Let $f \in \cC^\infty (M, \R)$ be a mapping and $\phi: U \to V \in \R^n$ be a [[chart]] around $p \in M$ with coordinates $(x_1, \dots, x_n)$. There exists an open neighbourhood $W \in U$ of $p$ and functions $f_i: W \to \R$, $i \in \{1, \dots, n\}$ such that $$f|_W(q) = f(p) + \sum_{i=1}^n (x_i(q) - x_i (p)) \cdot f_i(q).$$

```

<i>Proof.</i>
Let $W' \sub V = \phi(U)$ be a [[convex]] neighbourhood of $\phi(p)$ and set $x_0 :=  \phi(p)$. For $x \in W'$ we find:
$$
\begin{align*}
(f \circ \phi^{-1})(x) - (f \circ \phi^{-1})(x_0) &= \int_0^1 \frac{d}{dt} (f \circ \phi^{-1})(x_0 + t(x-x_0)) \ dt \\
&= \sum_{i=1}^n (x_i - x_i(p)) \underbrace{\int_0^1 \frac{\partial (f \circ \phi^{-1})}{\partial x_i} (x_0 + t(x-x_0)) \ dt.}_{=: \tilde{f}_i(x)}
\end{align*}
$$
With $W := \phi^{-1} (W')$,  $q = \phi^{-1} (x)$ and $f_i: W \to \R$, defined as $\tilde{f}_i \circ \phi$, the proposition follows.
