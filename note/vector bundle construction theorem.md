<div class="topSpace"></div>

Date Created: 23/09/24
References: 
Tags: #Type/Theorem #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[manifold]], [[vector bundle]], [[möbius strip]], [[n-sphere]]
Justifications: [[cocycle condition]]

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Theorem
title: Theorem (Vector Bundle Construction Theorem).
Let $B$ be a [[manifold|smooth manifold]] and $\{U_\alpha\}_{\alpha \in I}$ be an open cover. We assume that there exist maps $\phi_{\alpha \beta}: U_\alpha \cap U_\beta \to \text{GL}(k, \R)$ for $\alpha, \beta \in I$ such that for $\alpha, \beta, \gamma \in I$ the [[cocycle condition]]
$$\phi_{\alpha \gamma}|_{U_\alpha \cap U_\beta \cap U_\gamma} = (\phi_{\alpha \beta} \circ \phi_{\beta \gamma})|_{U_\alpha \cap U_\beta \cap U_\gamma}$$
is satisfied. From this we construct a vector bundle of rank $k$ over $B$:
On $\sqcup_{\alpha \in I} U_\alpha \times \R^k$ we define an [[equivalence|equivalence relation]] by $$(x,v) \in U_\alpha \times \R^k \sim (x, w) \in U_\beta \times \R^k \iff \phi_{\alpha \beta}(w)=v.$$ Transitivity is guaranteed by the cocycle condition. Let $E$ be the set of all equivalence classes of $\sim$ and define $p: E \to B$, $[(x,v)]\mapsto x$. If $U \sub U_\alpha$ is the domain of a chart $$h: U \to V \sub \R^k$$ of $B$ then $$V \times \R^k \to E$$ $$(y,v) \mapsto [h^{-1}(y), v]$$ is a local parametrization of $p^{-1}(U)$.
```

<i>Proof.</i>
This arises from the [[cocycle condition]].
<span style="float:right;">$\blacksquare$</span>

**Examples.**
1. Let $B = \S^n \sub \C$ with $U_1 := \S^1 \setminus \{-1\}$ and $U_2 := \S^1 \{1\}$. The intersection is given by $U_1 \cap U_2 = U_+ \cup U_-$ in reference to the [[n-sphere|parametrization of the n-Sphere]]. For $k=1$ we have [[vector bundle|local trivializations]]] $$\phi_{12}: U_1 \cap U_2 \to \text{GL}(1,\R) = \R \setminus \{0\}$$ $$z \mapsto \sgn(\Im (z)) = \begin{cases} +1 \ \text{on} \ U_+ \\ -1 \ \text{on} \ U_- \end{cases}$$. This [[vector bundle]] has a total space [[diffeomorphism||diffeomorphic]] to an open Möbius strip.
2. In general we define $B = \S^n$ with open subsets $U_{1,2} = \S^n \setminus \{(\pm 1, 0, \dots, 0)\}$ such that the union is $U_1 \cup U_2 \cong \R^n \setminus \{0\}$. For given $k \in \N$ and a [[smooth mapping]] $$\rho: \R^n \setminus \{0\} \to \text{GL}(k, \R)$$ a [[vector bundle]] over $\S^n$ of rank $k$ is determined by glueing $U_1 \times \R^k$ and $U_2 \times \R^k$ along $U_1 \cap U_2 \times \R^k$ with the mapping $$\Psi: (U_1 \cap U_2) \times \R^k \to (U_1 cap U_2) \times \R^k$$ $$(p,v) \mapsto (p, \rho(p)v).$$
		In general, the mapping $\rho: \R^n \setminus \{0\} \to \text{GL}(k, \R)$ can be constructed by chaining a given mapping $\tilde{\rho}: \S^{n-1} \to \text{GL}(k, \R)$ with the projection $$\pi: \R^n \setminus \{0\} \to \S^{n-1}$$ $$x \mapsto \frac{x}{\|x\|}$$ such that $\rho = \tilde{\rho} \circ \pi$.
		For $n=k=2$ we construct for $m \in \Z$ the map $\tilde{\rho}_m: \text{SO}(2) \cong \S^1 \to \text{SO}(2) \sub \text{GL}(2, \R)$, given by $A \mapsto A^m$. This yields many different vector bundles of rank $2$ over $\S^2$.