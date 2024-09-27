<div class="topSpace"></div>

Date Created: 13/09/24
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: [[topological space]][[Hausdorff property]][[topological basis]]
Justifications: <i>Not Applicable</i>

Specializations: [[submanifold]]
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Topological Manifold).

A __topological manifold__ $M$ of dimension $k$ is a topological Space $\mathcal{M}$ with following properties:
1. For all points $p \in \mathcal{M}$ exists an open neighbourhood $U$ of $p$ which is homeomorphic to on open subset of $\R^k$.
2. $\mathcal{M}$ has the [[Hausdorff property]].
3. $\mathcal{M}$ has a countable [[base]].
```
**Remark.** The Hausdorff property is necessary because of examples of the following type:
Let $Y := \R \times \{0\}$

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