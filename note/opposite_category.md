<div class="topSpace"></div>

Date Created: {{date::DD/MM/YYYY}}
References: Riehl/CatCont
Tags: #Type/Definition #Topic/CategoryTheory

Proved By: <i>Not Applicable</i>
Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

```ad-Definition
title: Definition (Opposite Category).
Given a [[category|category]] $\mathtt{C}$, the <u>opposite category</u> $\mathtt{C}^\op$ is defined as follows:
- $\ob \mathtt{C}^\op := \op \mathtt{C}$
- There is a morphism $f^\op$ in $\mathtt{C}^\op$ for every morphism $f: a \to b$ in $\mathtt{C}$, but we define $\dom f^\op = \codom f$ and $\codom f^\op = \dom f$.
- For any $x \in \mathtt{C}^\op$, the identity $1_x$ is retained.
- For $$a \overset{f^\op}\to b \overset{g^\op}\to c,$$ we define composition by $$g^\op f^\op := (fg)^\op= (c \to a)^\op.$$
```

Diagrammatically, $\mathtt{C}^\op$ is obtained from $\mathtt{C}$ by simply reversing all arrows.

_Examples_

1. The opposite category to the category given by a [[order#preorder|preordered set]] $(P, \leq)$ has precisely one morphism $a \to b$ if $b \leq a$.
2. Given a group $G$ and its category $\mathtt{B}G$, we have $(\mathtt{B}G)^\op = \mathtt{B}G^\op$, where $G^\op$ is the [[group#Opposite Group|opposite group]].

# Duality

Any theorem in category theory starting with ''In every category $\mathtt{C}$ $\dots$'' has a dual theorem obtained by reversing all arrows in the statement, i.e. passing from $\mathtt{C}$ to $\mathtt{C}^\op$. Since the proof of the dual statement is just the proof of the original statement carried out in the opposite category, it is not necessary to prove it again. This means that any such theorem is actually a two-for-one deal in disguise: One always obtains the dual statement together with the formulated one.
