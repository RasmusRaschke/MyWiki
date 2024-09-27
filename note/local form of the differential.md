<div class="topSpace"></div>

Date Created: 20/09/24
References: 
Tags: #Type/Proposition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[differential]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition (Local Form of the Differential).

Let $M, N$ be [[manifold|smooth manifolds]], $\phi: U \sub M \to \R^n$ be a [[chart]] of $M$ and $\psi: W \sub N \to \R^m$ be a [[chart]] of $N$. Let $\left( \left. \frac{\partial}{\partial x_1}\right|_p, \dots, \left. \frac{\partial}{\partial x_n}\right|_p\right)$ be a base of $T_pM$ and $\left( \left. \frac{\partial}{\partial x_1}\right|_{F(p)}, \dots, \left. \frac{\partial}{\partial x_m}\right|_{F(p)}\right)$ be a base of $T_pN$. Then the local coordinate form of $F_{\ast, p}: T_pM \to T_{F(p)}N$ is given by $$\left\{ \frac{\partial (\psi \circ F \circ \phi^{-1} )}{\partial x_i}\right\}_{i \leq n, \ j \leq m}.$$
```

<i>Proof.</i>
Let $F: M \to N$ be a [[smooth mapping]] and $p \in M$. Let $\phi: U \to \R^n$ be a chart around $p$ with coordinates $(x_1, \dots, x_n)$ and $\psi: W \to \R^m$ be a [[chart]] around $F(p)$ with coordinates $(y_1, \dots, y_m)$. For $w \in T_{F(p)}N$ and $f \in \cC^\infty (N)$ we have $$w(f) = \sum_{j=1}^m w(y_j) \left. \frac{\partial}{\partial y_j}\right|_{F(p)} f.$$ For $v \in T_pM$ this leads to $$F_{\ast, p}(v)(f) = \sum_{j=1}^m F_{\ast, p} (v) (y_j)  \left. \frac{\partial}{\partial y_j}\right|_{F(p)} f = \sum_{j=1}^m v(y_j \circ F)  \left. \frac{\partial}{\partial y_j}\right|_{F(p)} f.$$
With $v  = \sum_{i=1}^n v_i  \left. \frac{\partial}{\partial x_i}\right|_{p}$ the proposition follows as:
$$
F_{\ast, p} (v) (f) = \sum_{i = 1}^n \sum_{j=1}^m \frac{\partial (y_i \circ F \circ \phi^{-1})}{\partial x_i} (\phi (p)) \cdot v_i \cdot \left.\frac{\partial}{\partial y_j}\right|_{F(p)} f.
$$
**Example.**
Let $c: (a,b) \to M$ be a smooth curve in $M$. For $t_0 \in (a,b)$ we denote the standard base vector of $T_{t_0}\R \cong \R$ as $\left. \frac{\partial}{\partial t}\right|_{t_0}$ . The tangent vector in $c$ at $c(t_0)$ is given by $$c'(t_0) = \dot{c}(t_0) := c_{\ast, t_0} \left( \left. \frac{\partial}{\partial t} \right|_{t_0} \right) \in T_{c(t_0)}M.$$ For a [[smooth mapping]] $F: M \to N$ $$F_{\ast, c(t_0)} (c'(t_0)) = (F \circ c)'(t_0) \cdot \left. \frac{\partial}{\partial t}\right|_{F \circ c(t_0)}$$ holds.