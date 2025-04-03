<div class="topSpace"></div>

Date Created: 03/04/25
References: #Ref/Aluffi 
Tags: #Type/Definition #Topic/CategoryTheory

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Isomorphisms

``` ad-Definition
title: Definition (Isomorphism).

Let $\tC$ be a [[category]]. An <ins>isomorphism</ins> $f \in \Hom_\tC(A,B)$ is a morphism with a two-sided inverse $g \in \Hom_\tC(B,A)$ such that $gf=\id_A$ and $fg=\id_B$.

```

``` ad-Proposition
title: Proposition (Isomorphisms are unique).

Let $f \in \Hom_\tC(A,B)$ be an isomorphism. Then the inverse $f^{-1}: B \to A$ is unique.

```

*Proof.*
Let $g_1,g_2 \in \Hom_\tC(B,A)$ be inverse morphisms to $f$. Then, by associativity:
$$
g_1 = g_1 \id_A = g_1(fg_2) =(g_1f)g_2 = \id_B g_2 = g_2. 
$$
<span style="float:right;">$\blacksquare$</span>

This justifies our usage of $f^{-1}$ to denote the inverse of an isomorphism  $f$.

**Remarks.**
 1. The identitiy is always an isomorphism and its own inverse.
 2. If $f$ is an isomorphism, so is $f^{-1}$ and $(f^{-1})^{-1} = f$.
 3. If $f \in \Hom_\tC(A,B)$ and $g \in \Hom_\tC(B,C)$ are isomorphisms, so is $gf \in \Hom_\tC(A,C)$ with $(gf)^{-1}=f^{-1}g^{-1}$.
 These properties are proven by direct calculation.

**Examples.**
1. Isomorphisms in $\Set$ are [[set-function#Injection, Surjection, Bijection|bijections]].
2. There are categories where only identities are isomorphisms: Endowing $\Z$ with $\leq$ and considering integers as objects with $(a,b) \in \Hom_\Z(a,b) \iff a \leq b$ and $\Hom_\Z(a,b)=\emptyset$ else gives rise to the isomorphism condition $a \leq b \land b \leq a$, so $a=b$ is necessary for $(a,b)$ to be an isomorphism.
3. [[groupoid|Groupoids]] are categories in which all morphisms are also isomorphisms.



```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
A \arrow[dr, left, "g \circ f"'] \arrow[r, "f"] & B \arrow[d, "g"]\\
& C
\end{tikzcd}
\end{document}
```

<span style="float:right;">$\blacksquare$</span>

# Automorphisms

``` ad-Definition
title: Definition (Automorphism).

Let $\tC$ be a [[category]]. A morphism $f \in \Hom_\tC(A,A)$ is called <ins>automorphism</ins> of $A$. The set of all automorphisms of a given object $A$ is denoted $\Aut_\tC(A)\sub \End_\tC(A)$.

```

**Remark.**
Regardless of the specific [[category]] $\tC$, $\Aut_\tC(A)$ is always a [[group]]:
 1. Composition is defined because $\tC$ is a [[category]].
 2. Composition has to be associative.
 3. There has to be an identity with respect to composition.
 4. Since automorphisms are endomorphisms, they always have an inverse.