<div class="topSpace"></div>

Date Created: 13/09/24
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[topological space]][[Hausdorff property]][[topological basis]]
Justifications: <i>Not Applicable</i>

Specializations: [[submanifold]]
Generalizations: <i>Not Applicable</i>

# Topological Manifolds

``` ad-Definition
title: Definition (Topological Manifold).

A __topological manifold__ $M$ of dimension $k$ is a topological Space $\mathcal{M}$ with following properties:
1. For all points $p \in \mathcal{M}$ exists an open neighbourhood $U$ of $p$ which is homeomorphic to on open subset of $\R^k$.
2. $\mathcal{M}$ has the [[Hausdorff property]].
3. $\mathcal{M}$ has a countable [[base]].
```
**Remark.** The Hausdorff property is necessary because of examples of the following type:
Let $Y := \R \times \{0\}$

# Smooth Manifolds

``` ad-Definition
title: Definition (Smooth Manifold).

A __smooth manifold__ is a topological manifold $X$ together with a chosen smooth structure. A smooth structure is an [[equivalence class]] of [[atlas|smooth atlases]].
```
**Examples.**
1.  The identity $\id_{\R^n}: \R^n \to \R^n$ makes $\R^n$ a smooth manifold.
2.  Open subsets of smooth manifolds are again smooth manifolds by inheritance of a smooth structure. Let $O \sub M$ be an open subset and $\phi: U \to \R^n$ be a chart of $M$. Then $$\phi|_{O \cap U}: O \cap U \to \R^n$$ is a chart of $O$.
3.  The general linear group $\text{GL}(n,  \R) \sub \text{Mat}(n, \R) \cong \R^{n^2}$ is as preimage of $\R \setminus \{0\} \sub \R$ under $\text{det}: \text{Mat}(n, \R) \to \R$ open in $\text{Mat}(n, \R)$.
4. Every $k$ dimensional submanifold of $\R^n$ is a smooth $k$ dimensional manifold.
5. Let $M$ and $N$ be two smooth manifolds. Then the product $M \times N$ is again a smooth manifold. If $\phi_M$ is a chart of $M$ an $\phi_N$ is a chart of $N$, the product chart $\phi_M \times \phi_N: U_M \times U_N \to \R^{\dim M + \dim N}$ is a chart of $M \times N$.

**Remarks.**
There exists another equivalent definition of smooth manifolds.
Let $X$ be a set and $U_\alpha \sub X$ finitely many subsets with $\cup_\alpha U_\alpha = X$. Let $\phi_\alpha: U_\alpha \to V_\alpha$ with open subsets $V_\alpha \sub \R^n$ be [[bijections]]. We define a topology: $U \sub X$ is open iff for all $\alpha \in A$ the images $\phi(U \cap U_\alpha) \sub \R^n$ are open. If this topology is [[Hausdorff property|Hausdorff]], $X$ is a topological manifold. For smooth chart transitions $X$ is also smooth.

# Manifolds with boundary

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

# Riemannian manifolds

``` ad-Definition
title: Definition (Pseudo-Riemannian Manifold).

A __(pseudo-)Riemannian manifold__ is a pair $(M, g)$ consisting of a smooth manifold $M$ and a [[metric tensor|(pseudo-)Riemannian metric]] $g$.
```

**Remark.**
The product of two pseudo-Riemannian manifolds is again a pseudo-Riemannian manifold.

``` ad-Definition
title: Definition (Geodesically Complete Manifold).

A Riemannian Manifold $(M,g)$ is called __(geodesically complete) manifold__ if every [[geodesic]] can be extended to a [[geodesic#Maximal Geodesics|maximal geodesic]] $\gamma: \R \to M$.
```
**Remark.**
This is equivalent to $\exp_p$ being defined for all $p \in M$ on all of $T_pM$.

**Examples.**
1. $(\R^n, g_\text{st})$ and $\S^n$ with the round [[metric tensor|metric]] are geodesically complete.
2. The open ball $B^n \sub (\R^n, g_\text{st})$ and $(\R^n \setminus \{0\}, g_\text{st})$ are not geodesically complete.


``` ad-Definition
title: Definition (Einstein Metric).

Let $g$ be a [[metric tensor]]. If $$\text{Ric} = \lambda g$$ with $\lambda \in \R$, $g$ is called __Einstein metric__. A pair $(M,g)$ of a (pseudo-)Riemannian manifold $M$ and an Einstein metric $g$ is called __Einstein manifold__.
```
**Examples.**
1. $(\R^n, g_\text{st})$ is an Einstein manifold with $\lambda =0$.
2. $(\S^n, g_\text{st})$ is an Einstein manifold with $\lambda = 1$.