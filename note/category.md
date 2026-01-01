<div class="topSpace"></div>

Date Created: {{date::DD/MM/YYYY}}
References:
Tags: #Type/Definition #Topic/CategoryTheory

Proved By: <i>Not Applicable</i>
Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: [[topological space|$\mathtt{Top}, \mathtt{Top}_\ast$]], [[set|$\mathtt{Set}$]], [[group|$\mathtt{Grp}$]], [[field|$\mathtt{Fld}$]], [[vector space|$\mathtt{Vec}_\mathbb{K}$]], [[module|$\mathtt{Mod}_R$]], [[manifold|\mathtt{Man}$]], [[measureable space|$\mathtt{Mea}$]]

``` ad-Definition
title: Definition (Category).
    A category $\mathtt{C}$ consists of objects $\ob \mathtt{C}$ and of morphisms $\mor \mathtt{C}$ such that the following is satisfied:
1. Each morphism $f$ has a specified domain $\dom f \in \ob \mathtt{C}$ and codomain $\codom f \in \ob \mathtt{C}$.
2. For two morphisms $f: x \to y$ and $g: y \to z$, there exists a composition morphism $gf: x \to z$.
3. Composition is associative: $h(gf)=(hg)f$.
4. For all objects $x$ of $\mathtt{C}$, there is an identity morphism $1_x: x \to x$ with respect to composition.
For two objects $x,y$, a morphism $x \to y$ is called homomorphism. The space of all homomorphisms between $x$ and $y$ is denoted $\Hom_\mathtt{C}(x,y)$ or $\mathtt{C}(x,y)$.

```
*Examples*
1. Given a [[order#preorder|preordered set]] $(P, \leq)$, one defines a category by  setting $\Ob \mathtt{P} := P$. For two elements $x,y \in P$, we have precisely one morphism $x \to y$ if and only if $x \leq y$. Else, $\mathtt{C}(x,y) = \emptyset$.
