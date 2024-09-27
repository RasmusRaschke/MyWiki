<div class="topSpace"></div>

Date Created: 19/09/24
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Smooth Mapping).

Let $M_1$ and $M_2$ be two [[manifolds|smooth manifolds]]. A mapping $$f: M_1 \to M_2$ is called __smooth__ iff:
1. $f$ is continous.
2. For all [[chart|charts]] $(\phi, U)$ of $M_1$ and $(\psi, V)$ of $M_2$ with $f^{-1}(V) \cap U \neq \emptyset$ the transition $$\psi \circ f \circ \phi^{-1}: \phi(f^{-1}(V) \cap U) \to \psi(V)$$ is a smooth mapping between open subsets of $\R^{\dim M_1}$ and $\R^{\dim M_2}$.  
```

**Remarks.**
1. A function $f: M \to \R$ is smooth if $f \circ \phi^{-1}: \phi(U) \to \R$ is smooth for all [[chart|charts]].
2.  Let $M \sub \R^n$ be a $k$ dimensional [[submanifold|submanifold]] of $\R^n$. The function $f: M \to \R^k$ is smooth iff for all points $p \in M$ there exists an open neighbourhood $U \sub \R^n$ and a smooth function $F: U \to \R^k$ such that $$f|_{U \cap M } = F_{U \cap M}.$$