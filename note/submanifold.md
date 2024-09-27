<div class="topSpace"></div>

Date Created: 08/27/24 21:31
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[manifold]]

``` ad-Definition
title: Definition (Characterizations of a submanifold).

A subset $M \sub \R^n$ is called $k$ dimensional submanifold (SMF) of $\R^k$ if for all points $p \in M$ there exists an open neighbourhood $U \sub \R^n$ of $p$ such that $h: U \to V$ with $V \sub \R^n$ open is a diffeomorphism and $h(U \cap M) = V \cap \R^k \times \{0\}^{n-k}$.
```

**Remarks.**
The following two definitions are equivalent to the first one:
1. For every point $p \in M$ exists an open neighbourhood $U \sub \R^n$ and a smooth function $\phi: U \to \R^{n-k}$ such that the derivative $d\phi_x: \R^n \to \R^{n-k}$ has full rank for all $x \in U \cap M$ and $U \cap M = \phi^{-1}(0)$.
2. For every point $p \in M$ exists an open neighbourhood $U \sub \R^n$, an open subset $V^\ast \sub \R^k$ and a smooth function $\phi: V^\ast \to \R^n$ such that the derivative $d\phi_y:\R^k \to \R^n$ has full rank for all $y \in V^\ast$ and $\phi$ maps $V^\ast$ homeomorphically onto $U \cap M$. 
3. Let $M$ and $N$ be [[manifold|smooth manifolds]]. A subset $S \sub M$ is called submanifold if $S$ is the image of an [[submersion, immersion and embedding|embedding]] $f: N \to M$.
*Proof.* TBD

**Examples.**
1.  The $k$ dimensional sphere is defined as $\S^k := \left\{ x \in \R^{k+1} \ | \ \| x \|^2 = \sum_{j} x_j^2 =1  \right\} \sub \R_{k+1}$. The function $$ \phi: \R^{k+1} \to \R$$ $$x \mapsto 1-\| x\|^2 = 1 - \langle x, x \rangle$$ has the differential $\mathcal{D}\phi_x(v) = -2 \langle x, v \rangle \neq 0$ at all points $x \in \S^k$ in direction of $v \in \S^k$ and is therefore *surjective*. 
		To prove the statement of the definition, we assume without loss of generality that $x_1 > 0$ for some $x \in \S^k$ and look at $U:=\left\{ x \in \R^{k+1} \ |  \ x_1 > 0 \right\}$. Construct a function $$h: U \to \R^{k+1}$$ $$(x_1, \dots, x_{k+1} ) \mapsto \left(x_{1}-\sqrt{1-\sum_{j=2}^{k+1} x_{j}^2}, x_{2}, \dots, x_{k+1}\right).$$ From $\sum_j x_j^2 = 1$ (definition of the sphere) follows $x_1^2 = 1-\sum_{j=2}^{k+1}x_j^2$ and with that $h(U \cap \S^k) = \{0\} \times  V \cap \R^{k}$ . Furthermore, $h$ is obviously a diffeomorphism. Therefore, $\S^{k}$ is a $k$ dimensional, smooth submanifold of $\R^{k+1}$.
2. Let $W \sub \R^{k}$ be an open subset and $f: W \to \R^{n-k}$ be a smooth mapping. Then the graph $\Gamma_f = \{(x, f(x)) \in W \times \R^{n-k} \} \sub \R^k \times \R^{n-k}$ is a $k$ dimensional submanifold of $\R^n$. To prove this, choose $W \times \R^{n-k} \sub \R^n$ as open neighbourhood of $p \in \Gamma_f$ and construct the diffeomorphism $h: U \to \R^k \times \R^{n-k}$, $(x,y) \mapsto (x, y-f(x))$.