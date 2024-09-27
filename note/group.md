<div class="topSpace"></div>

Date Created: 
References: 
Tags: #Type/Definition #Topic/Algebra 

Proved by: <i>Not Applicable</i>
References: [[vector space]]
Justifications: <i>Not Applicable</i>

Specializations: [[subgroup]]
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Group).

A __group__ is an ordered pair $(G, \ast)$ where $G$ is a set and $\ast: G \times G \to G$ is a binary relation satisfying the following properties:
1. associativity: $\forall a,b,c \in G: (a \ast b) \ast c = a \ast (b \ast c)$
2. identity: $\exists e \in G \forall a \in G: e \ast a = a \ast e = a$
3. inverse: $\forall a \in G \exists a^{-1} \in G: a \ast a^{-1} = a^{-1} \ast a = e$

```
``` ad-Definition
title: Definition (Abelian Group).

A group $(G, \ast)$ is called __abelian__ if the commutative law holds for $\ast$.

```

**Examples.**
1.  $\Z, \Q, \R$ and $\C$ are groups under addition $+$ with $e = 0$ and $a^{-1} = -a$.
2.  $\Q^\ast, \R^\ast, \C^\ast, \Q^+$ and $\R^+$ are groups under multiplication $\cdot$ with $e=1$ and $a^{-1} = \frac{1}{a}$.
3. A [[vector space|vector space]] forms an abelian group $(V, +)$ under vector addition $+$.