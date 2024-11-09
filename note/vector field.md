<div class="topSpace"></div>

Date Created: 25/09/24
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[vector bundle]], [[section]]
Justifications: <i>Not Applicable</i>

Specializations: [[vector field along a map]]
Generalizations: <i>Not Applicable</i>

# Vector Fields

``` ad-Definition
title: Definition (Vector Fields).

A __smooth vector field__ on a [[manifold|smooth manifold]] $M$ is a [[sections|smooth section]] in the [[tangent bundle]] $\pi: TM \to M$ of $M$.
```
**Remarks.**
1. Let $p: E \to B$ be a [[vector bundle]] and $S \sub B$ be a [[submanifold]]. Then $$p|_{p^{-1}(S)} : p^{-1}(S) (=:E|_S) \to S$$ is another smooth [[vector bundle]].
2. Let $M$ be a [[manifold|smooth manifold]] and $\phi: U \to V \sub \R^n$ be a [[chart|local chart]] with coordinates $(x_1, \dots, x_n)$. The mapping $$\frac{\partial}{\partial x_i}: U \to TM|_U = TU$$ $$p \mapsto \left. \frac{\partial}{\partial x_i}\right|_p$$ defines a smooth local vector field for all $i \in \{1, \dots, n\}$. In the by the [[chart]] $\phi: U \to V$ defined [[vector bundle|local trivialization]] $\psi: TM|_U \to TV = V \times \R^n$ the vector field $\frac{\partial}{\partial x_i}$ is the constant vector field $$p \mapsto (\phi(p), (0, \dots, 0, 1, 0, \dots, 0)).$$ In every $p \in U$ the vectors $\left\{ \left.\frac{\partial}{\partial x_i}\right|_p\right\}_{i \leq n}$ are a [[basis]] of $T_pM$. Therefore, every on $U$ defined vector field is given by a linear combination of $\left\{ \left.\frac{\partial}{\partial x_i}\right|_p\right\}_{i \leq n}$ with coefficients in $\cC^\infty(U, \R)$.

**Example.**
Let $U \sub M$ be an open subset. Then, $TM|_U = TU$. However, if $S \sub M$ has positive codimension ($\dim S < \dim M$), $TM|_S$ and $TS$ are different because of their different rank.

# Vector Fields along a map

``` ad-Definition
title: Definition (Vector Field along a Map).

Let $N$ and $M$ be [[manifold|smooth manifolds]] and $f: N \to M$ be a [[smooth mapping]]. A __vector field along $f$__ is a [[vector field]] $Y: N \to TM$ such that $$\pi_M \circ Y = f.$$
This makes vector fields along $f$ [[section|sections]] in the pullback of the [[tangent bundle]] $$\pi = pr_1: f^\ast TM = \{ (x,v) \in N \times TM | f(x) = \pi_M (v) \} \to N.$$ The fiber in $x \in N$ is given by $T_{f(x)}M$. The space of vector fields along $f$ is denoted $$\Gamma_f(TM) := \Gamma(f^\ast TM).$$ It is:
1. A [[vector space]] over $R$.
2. A [[module]] over $\cC^\infty(N)$.
3. A [[module]] over $\cC^\infty(M)$, because $f$ induces a [[homomorphism|ring homomorphism]] $f^\ast: \cC^\infty (M) \to \cC^\infty (N)$, $\phi \mapsto \phi \circ f$.

```
For a vector field along a curve, the following diagram commutes:
```tikz
	
	\usepackage{tikz-cd, amsmath, amstext, amsfonts, amssymb}
	
	\begin{document}
	
	\begin{tikzcd}
	
		& TM \arrow[d,"{\pi_M}"] \\
		N \arrow[ur, "{Y}"] \arrow[r, "{f}"] & M
		
	\end{tikzcd}
	
	\end{document}
```

**Examples.**
1. For a curve $\gamma: (a,b) \to M$, $Y(t) = \dot{\gamma} (t)$ is a vector field along $\gamma$.
2. If $\gamma: (a,b) \to M$ is a constant curve $\gamma(t) = p \in M$, a vector field along $\gamma$ is a curve $Y: (a,b) \to T_pM$.

**Remarks.**
1. For every [[vector field]] $X \in \Gamma (TM)$ exists a restriction onto $f$, given by $X \circ f \in \Gamma_f (TM)$. Usually, not all vector fields along $f$ have this form.
2. For every [[vector field]] $A \in \Gamma (TN)$ we obtain a vector field along $f$ given by $f_\ast A \in \Gamma_f (TM)$:
```tikz
	
	\usepackage{tikz-cd, amsmath, amstext, amsfonts, amssymb}
	
	\begin{document}
	
	\begin{tikzcd}
	
		TN \arrow[r, "f_\ast"] \arrow[d, "\pi_N"] & TM \arrow[d,"{\pi_M}"] \\
		N \arrow[r, "f"] \arrow[ur, "Y"] & M
		
	\end{tikzcd}
	
	\end{document}
```
3. For every $Y \in \Gamma_f (TM)$ and every $\psi \in \cC^\infty(M)$ we obtain a map $Y \psi \in \cC^\infty (N)$, defined  as $$(Y \psi)(p)=Y_p\psi.$$ If $Y = X \circ f$ is a restriction, we define $$(X \circ f) (\psi) = (X\psi) \circ f.$$
4. Although not all vector fields along $f$ are given globally as a restriction, every [[vector field]] $Y \in \Gamma_f (TM)$ can locally be written as linear combination of restrictions with coefficients in $\cC^\infty (N)$. If $(x_1, \dots, x_n)$ are local coordinates on a coordinate neighbourhood $U \in M$, define $V := f^{-1} (U) \sub N$. Then, every [[vector field]] $Y \in \Gamma_f (TM)$ admits  a local representation on $U$ given by $$Y|_U = \sum_{k=1}^n (Y_{x_k}) \cdot \left(\partial_{x_k} \circ f\right).$$

# Extending the [[covariant derivative]]
Let $M$ and $N$ be [[manifold|smooth manifolds]], $f: N \to M$ be a [[smooth mapping]] and $\nabla$ be a [[covariant derivative]] on $TM$. Then there exists a unique and canonical extension for any $f \in \cC^\infty(N)$ given by
$$\tilde{\nabla}: \Gamma (TN) \otimes \Gamma_f (TM) \to \Gamma_f (TM)$$
$$(A, Y) \mapsto \tilde{\nabla}_A Y$$
with the following properties:
1. $\tilde{\nabla}$ is $\cC^\infty(N)$-linear in the first argument.
2. $\tilde{\nabla}$ is a [[derivation]] in the second argument: $\tilde{\nabla}_A fY = (Af) \cdot Y + f \tilde{\nabla}_A Y$ for all $f \in \cC^\infty(N)$.
3. For $X \in \Gamma (TM)$ we have $\tilde{\nabla}_A (X \circ f) = (\nabla_{f_\ast A} X) \circ f$.


Furthermore, $\tilde{\nabla}$ satisfies the characterization equations of [[torsion and curvature]]:
4. $T(f_\ast A, f_\ast B) = \tilde{\nabla_A} f_\ast B - \tilde{\nabla}_B f_\ast A - f_\ast [A,B]$
5. $R(f_\ast A, f_\ast B)Y = \tilde{\nabla}_A \tilde{\nabla}_B Y -\tilde{\nabla}_B \tilde{\nabla}_A Y - \tilde{\nabla}_{[A,B]} Y$
Therefore, $\tilde{\nabla}$ is a [[covariant derivative]] on $f^\ast TM$. The first three properties characterize $\tilde{\nabla}$ completely because every [[vector field]] can locally be written as linear combinations of restrictions. We generally write suggestively $\tilde{\nabla} \equiv \nabla$.
