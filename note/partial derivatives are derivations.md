<div class="topSpace"></div>

Date Created: 20/09/24 
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[partial derivative]], [[manifold]], [[derivation]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition (Partial Derivatives are Derivations).

The [[partial derivative]] as defined for [[manifold|manifolds]] is a [[derivation]] at $p \in M$.
```

<i>Proof.</i>
Linearity is trivial, the Leibniz rule follows from general derivative rules in $\R^k$:
$$
\begin{align*}
\left.\frac{\partial}{\partial x_i}\right|_p (f \cdot g) &= \frac{\partial (fg) \circ \phi^{-1}}{\partial x_i}(\phi(p))\\
&=\frac{\partial (f \circ \phi^{-1})(g \circ \phi^{-1}) \circ \phi^{-1}}{\partial x_i}(\phi(p))\\
&= \frac{\partial (f \circ \phi^{-1})}{\partial x_i}(\phi(p)) \cdot \left( g \circ \phi^{-1} \right)(\phi(p)) + \left( f \circ \phi^{-1} \right)(\phi(p)) \cdot \frac{\partial (g \circ \phi^{-1})}{\partial x_i}(\phi(p))\\
&= \left.\frac{\partial}{\partial x_i}\right|_p [f] \circ g(p) + f(p) \circ  \left.\frac{\partial}{\partial x_i}\right|_p [g]
\end{align*}
$$
<span style="float:right;">$\blacksquare$</span>