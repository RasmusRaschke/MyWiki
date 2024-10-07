<div class="topSpace"></div>

Date Created: 20/09/24 
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry

Proved by: <i>Not Applicable</i>
References: 
Justifications: <i>Not Applicable</i>

Specializations: [[tangent space of Rn]]
Generalizations: <i>Not Applicable</i>

# Real Tangent Space

``` ad-Definition
title: Definition (Tangent Space in $\R^n$).

The __tangent space__ $T_p\R^n$ at a point $p \in \R^n$ is given by $$T_p\R^n:= \{(p, \xi) | \xi \in \R^n \}.$$
```

# Tangent Space of Manifolds

``` ad-Definition 
title: Definition (Tangent space as equivalent charts).

Let $M$ be a [[manifold|smooth manifold]] with an [[atlas]] $\fA$. Define a equivalence relation $\sim_p$ on $$\{(\phi, v) | \phi: U \to V \sub \R^k, \ p \in U, \ v \in T_{\phi(p)} \R^k \},$$ where $\phi$ is a [[chart]] in $\fA$, by $$(\phi, v) \sim_p (\psi, w) \iff w = (\psi \circ \phi^{-1})_{\ast, \phi(p)}(v).$$ Transitivity is given by the [[chain rule]]. Two charts are called __equivalent__ if they are equivalent under $\sim_p$. A __tangent vector__ at $p \in M$ is a [[equivalence|equivalence class]] of $\sim_p$. The set of all equivalence classes constitutes the __tangential space__ of $M$ in $p$, denoted by $T_pM$.
```
**Remark.**
1.  The equivalence class of any [[chart]] $\phi: U \to V \sub \R^k$ in $p$ containes an element of the form $(\phi, v)$.
2.  With addition $[(\phi, v)]+[(\phi, w)] = [(\phi, v+w)]$ and scalar multiplication $\lambda [(\phi, v)] = [(\phi, \lambda v)]$, $T_pM$ is a [[vector space|real vector space]] of dimension $k$.

``` ad-Definition 
title: Definition (Tangent space as equivalent curves).

Let $\epsilon > 0$ and define an equivalence relation $\approx_p$ on $$\{\gamma: (-\epsilon_\gamma, \epsilon_\gamma) \to M | \gamma \ \text{is smooth}, \ \gamma(0)=p \}$$ by $$\gamma_1 \approx_p \gamma_2 \iff \exists \phi: U \to V: (\phi \circ \gamma_1)'(0) = (\phi \circ \gamma_2)'(0)$$ with a chart $\phi$ at $p$. The [[chain rule]] guarantees that $\gamma_1$ and $\gamma_2$ are the same for any chart. The set of [[equivalence|equivalence classes]] is called __tangential space__ $T_pM'$ of $M$ at $p$.
```
**Remark.**
The two definitions are equivalent as there exists a [[real function|bijection]] $$T_pM' \to T_pM$$$$[\gamma] \mapsto [(\phi, (\phi \circ \gamma)'(0))]$$ for fixed $\phi: U \to V \sub R^k$.

A third equivalent definition follows from the definition of [[derivation|derivations]].