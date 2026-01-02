<div class="topSpace"></div>

Date Created: {{date::DD/MM/YYYY}}
References: Aluffi/Algebra0
Tags: #Topic/GroupTheory #Type/Definition

Proved By: <i>Not Applicable</i>
Specializations: [[abelian group]]
Generalizations: [[monoid]], [[semigroup]], [[magma]]
Examples: <i>Not Applicable</i>

```ad-Definition
title: Definition (Group).
A <u>group</u> is a pair $(G, \cdot)$ consisting of a non-empty set $G$ and a binary operation
$$
\cdot: G \times G \to G
$$
such that the following is satisfied:
- Associativity: $\forall g,h,k \in G: \, (g \cdot h) \cdot k = g \cdot (h \cdot k)$
- Identity: $\exists e \in G: \, \forall g \in G: \, g\cdot e=e\cdot g=g$
- Inverse: $\forall g \in G \exists g^{-1} \in G: \, g\cdot g^{-1}=g^{-1}\cdot g = e$
```

# Opposite Group

```ad-Definition
title: Definition (Opposite Group).
Given a group $(G, \cdot)$, the opposite group $G^\op$ has the same underlying set $G$, but $$g \cdot^\op h := h \cdot g$ for all $g,h \in G$.
```
