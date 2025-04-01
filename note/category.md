<div class="topSpace"></div>

Date Created: 27th March 2025
References: #Ref/Aluffi 
Tags: #Type/Definition

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: [[set]], [[set-function]]

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