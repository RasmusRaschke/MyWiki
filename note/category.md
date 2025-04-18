<div class="topSpace"></div>

Date Created: 27th March 2025
References: #Ref/Aluffi 
Tags: #Type/Definition #Topic/CategoryTheory

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: [[set]], [[set-function]], [[chain complex]]

``` ad-Definition
title: Definition (Category).

A <ins>category</ins> $\tC$ consists of
 - a [[class]] $\Obj(\tC)$ of <ins>objects</ins> of the category and,
 - for every $A,B \in \Obj (\tC)$, a set $\Hom_\tC(A,B)$ of <ins>morphisms</ins> with the following properties:
	 1. For every object $A \in \Obj(\tC)$ exists at least one morphism $1_A \in \Hom_\tC(A,A)$, called <ins>identity</ins> on $A$.
	 2. Two morphisms $f \in \Hom_\tC(A,B)$ and $g \in \Hom_\tC(B,C)$ can be composed to a morphism $gf \in \Hom_\tC(A,C)$. This defines a [[set-function]] $$\Hom_\tC(A,B) \times \Hom_\tC(B,C) \to \Hom_\tC(A,C)$$ for every triple $A,B,C \in \Obj(\tC)$.
	 3. Composition is associative.
	 4. The identities are identities with respect to composition: If $f \in \Hom_\tC (A,B)$ is a morphism and $1_A, 1_B$ are the identities on $A$ and $B$, the following holds: $$f1_A=f$$ $$1_B f= f.$$
	 5. The sets $\Hom_\tC(A,B)$ and $\Hom_\tC(C,D)$ are disjoint unless $A=C$ and $B=D$.

```
**Examples.**
1. The category $\Set$ consists of [[set|sets]] as objects and [[set-function|set-functions]] as morphisms. This is one example where is is necessary to allow classes instead of sets in the definition of objects of a category since the set of all sets can not be defined without contradiction in ZFC.
2. A set $S$ with a reflexive and transitive [[relation]] $\approx$ comprises a category. The objects are elements of $S$ and morphisms are pairs $(a,b) \in S \times S$ if $a \sim b$ and $\emptyset$ otherwise. This set has at most one morphism between any two objects. A similar example is obtained by considering the power set $\sP(S)$ as object and defining morphisms similar with the subset relation, so $(A,B) \in \sP(S) \times \sP(S)$ is a morphism if $A \sub B$. 

# Opposite category

For a given category $\tC$, we define a new category $\tC^\op$ by keeping the objects of $\tC$ and reversing all arrows: $$\Hom_{\tC^\op}(A,B) = \Hom_{\tC}(B,A).$$ Composition, identities and associativity carry over from the source category.

# Subobject classifiers

For a given category $\tC$, the objects don't have to be a set. Therefore, we can not always make sense of the notion of a subobject in the way we did with subsets of [[set|sets]]. If it is possible to talk about subobjects, the subobjects of any given object $A$ have to be in bijection with the homset $\Hom_{\tC}(A, \Omega)$. The special set $\Omega$ is called <ins>subobject classifier</ins>.

**Example.**
If we look at $\Set$, the subobject classifier is $\Omega := \{0,1\}$. For any given set $X$ we have [[characteristic function|characteristic functions]] $\chi_A: X \to \Omega$ for any subset $A \sub X$.  For every subobject resp. subset of $X$, we obtain one characteristic function corresponding to that subset. Conversely, any function from $X$ to $\Omega$ is a characteristic function of some subset of $X$. If we define $\text{true}: \{0\} \to \{0,1\}$ by $\text{true}(0):=0$, a commutative diagram ensures for a subset $A \in X$:
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath}
\newcommand{\true}{\text{true}}
\begin{document}
\begin{tikzcd}[scale=3]
A \arrow[r, "\chi_A"] \arrow[d, hook, "\iota"] & \{0\} \arrow[d, "\true"]\\
X \arrow[r, "\chi_A"] & \{0,1\}
\end{tikzcd}
\end{document}
```

# Terminal Objects

``` ad-Definition
title: Definition (Initial and Final Objects).

Let $\tC$ be a category. An object $I \in \Obj(\tC)$ is called <ins>initial</ins> if for every $A \in \Obj(\tC)$ there is exactly one morphism $I \to A$, so $\Hom_\tC(I,A)$ is a singleton. Similarly, an object $F \in \Obj(\tC)$ is called <ins>final</ins> if there is exactly one morphism $A \to F$ for every $A \in \Obj(\tC)$, so $\Hom_\tC(A,F)$ is a singleton. An initial or final object is also called <ins>terminal</ins>.

```

**Examples.**
1. The category $(\Z, \leq)$ has no terminal object because there are no integers smaller or lager than any other integer.
2. The empty set $\emptyset$ is initial in [[set|$\Set$]] with the empty graph as morphism. On the other side, every singleton is final in $\Set$ by means of the constant function.

``` ad-Proposition
title: Proposition (Terminal Objects are unique up to Isomorphism).

Let $\tC$ be a category.
1. If $I_1,I_2$ are initial in $\tC$, they are [[isomorphism|isomorphic]]: $I_1 \cong I_2$.
2. If $F_1, F_2$ are final in $\tC$, they are also [[isomorphism|isomorphic]]: $F_1 \cong F_2$.

```

*Proof.*
1. For every object $I$, $\id_I \in \Hom(I,I)$. If $I$ is final, there can be at most one morphism $I \to I$, so every morphism $I \to I$ is the identity. Now, since $I_1$ and $I_2$ are initial, there exist exactly two morphisms $f:I_1 \to I_2$ and $g: I_2 \to I_1$ with $fg: I_1 \to I_1$ and $gf: I_2 \to I_2$. By the aforementioned argument we obtain $gf=\id_{I_2}$ and $fg=\id_{I_1}$.
2. We make the analogous observation about any morphism $F_1 \to F_1$ and $F_2 \to F_2$. With this, the assertion follows completely analogous.
<span style="float:right;">$\blacksquare$</span>