<div class="topSpace"></div>

Date Created: 20/09/24
References: 
Tags: #Type/Proposition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[tangent space]], [[derivation]], [[manifold]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition ($\text{Der}_p$ describes Tangent Space).

Let $U \sub M$ and $V \sub \R^n$ be open subsets and $M$ be a [[manifold|smooth manifold]] with $p \in M$ and coordinate functions $(x_1, \dots, x_n)$. The mapping
$$ T_pM \to \text{Der}_p$$
$$ [\phi, v] \mapsto \cD_{[\phi, v]},$$
with the [[directional derivative]] $$f \circ \phi^{-1}: V \to \R$$ in direction of $v \in T_{\phi(p)}M,$ is given by $$\cD_{[\phi, v]}(f) = v(f \circ \phi^{-1}).$$ It is an [[isomorphism]] of $\R$-[[vector space|vector spaces]].
```

<i>Proof.</i>
The mapping is well defined by means of the [[chain rule]]. The tangential vector $[\phi, (\phi|_p, e_i)]$ is mapped to $\frac{\partial}{\partial x_i}|_p$. For locally defined coordinate functions $x_j: U \to \R$ the identity $\frac{\partial x_j}{\partial x_i} = \delta_{ij}$ holds. This makes the above mapping [[real function|injective]]. Surjectivity follows from the fact that $\text{Der}_p$ is spanned by the partial derivatives:
$$ \text{Der}_p = \left\langle \left.\frac{\partial}{\partial x_1} \right|_p, \dots, \left. \frac{\partial}{\partial x_n}\right|_p \right\rangle.$$
This follows from the [[taylor expansion]]:
$$
\left. \frac{\partial}{\partial x_i} \right|_p (f) = \sum_{j=1}^n \left. \frac{\partial}{\partial x_i} \right|_p (x_j - x_j(p)) \cdot f_j = \sum_{j=1}^n \delta_{ij} \cdot f_j (p) + \cancel{(x_j(p) -x_j(p))} \cdot \left. \frac{\partial}{\partial x_i} \right|_p f_j = f_i(p).
$$
For any [[derivation]] $\cD \in \text{Der}_p$ we see
$$
\cD f = \sum_{i=1}^n \cD (x_i - x_i (p)) \cdot f_i = \sum_{i=1}^n \cD (x_i) f_i(p) + \cancel{(x_i (p) - x_i (p))} \cdot \cD (f_i) = \left( \sum_{i=1}^n \cD (x_i) \left. \frac{\partial}{\partial x_i} \right|_p \right) f.
$$
Therefore, any $\cD \in \text{Der}_p$ can be expressed as [[linear combination]] of $\left\{ \frac{\partial}{\partial x_i}|_p \right\}_i$.
<span style="float:right;">$\blacksquare$</span>