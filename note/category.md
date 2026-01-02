<div class="topSpace"></div>

Date Created: Thu 1 Jan 19:10:31 CET 2026
References: Riehl/CatCont
Tags: #Type/Definition #Topic/CategoryTheory

Proved By: <i>Not Applicable</i>
Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: [[topological space]], [[manifold#smooth manifold]], [[vector space]], [[set]], [[chain complex]]

```ad-Definition
title: Definition (Category).
A <u>category</u> $\mathtt{C}$ consists of a class of objects $\ob \mathtt{C}$ and a class of morphisms $\mor \mathtt{C}$ between said objects such that the follwing is satisfied:
- Each morphism $f \in \mor \mathtt{C}$ has a specified domain $\dom f$ and codomain $\codom f$ in $\ob \mathtt{C}$.
- For any pair $f,g \in \mor \mathtt{C}$ such that $\codom f = \dom g$ exists a composition morphism $$gf: \dom f \to \codom g.$$
- For any $x \in \ob \mathtt{C}$ exists the identity morphism $1_x: x \to x$ which behaves as identity with respect to composition.
- For any $f,g,h \in \mor \mathtt{C}$ such that $$a \overset{f}\to b \overset{g}\to c \overset{h}\to d,$$ we have associativity: $$(hg)f=h(gf)$$.
The class of morphisms between $a,b \in \ob \mathtt{C}$ is denoted $\mathtt{C}(a,b)$ or $\Hom_\mathtt{C}(a,b)$. A morphism is also called <u>homomorphism</u>. If $ \dom f= \codom f$, we call $f$ an <u>endomorphism</u>.
```

We focus on special abstract examples not covered in other articles.

_Examples_

1. Given a [[order#preorder|preordered]] or a [[order#partial order|partially ordered]] set $(P, \leq)$, we define a category by setting $\ob \mathtt{C} := P$ and declare $\mathtt{C}(a,b)$ to consist of precisely one element if $a \leq b$, and being empty otherwise.
2. Given a [[monoid|monoid]] or a [[group|group]] $G$, we define a category $\mathtt{B}G$ with $\ob \mathtt{B}G:= \{\ast\}$ and $\mor \mathtt{B}G := G$. This category has only one object. The group identity and associativity carry over in this way.
3. The category $\Htpy$ shares its objects with $\Top$, but the morphisms are given by [[homotopy|homotopy classes]] of [[continuity|continuous maps]].

# Subcategories

```ad-Definition
title: Definition (Subcategory).
Given a category $\mathtt{C}$, a subcategory $\mathtt{D} \subset \mathtt{C}$ is a category with objects and morphisms of $\mathtt{C}$ such that $\mathtt{D}$ contains all domains and codomains, all identities and all compositions of its morphisms.
```

# Small Categories

```ad-Definition
title: Definition ((Locally) Small Category).
A category $\mathtt{C}$ is <u>small</u> if $\ob \mathtt{C}$ is a [[set|set]].
It is <u>locally small</u> if $\mor \mathtt{C}$ consists only of sets of morphisms. In this case, we call sets of morphisms also <u>hom-sets</u>.
```

_Examples_

1. The concrete categories $\Set$, $\Top$, $\Man$ and so on are not small or locally small.
2. The category $\mathtt{B}G$ defined above is small and locally small.
