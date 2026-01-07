<div class="topSpace"></div>

Date Created: {{date::DD/MM/YYYY}}
References: Aluffi/Alg
Tags: #Topic/GroupTheory #Type/Definition

Proved By: <i>Not Applicable</i>
Specializations: [[abelian group]]
Generalizations: [[monoid]], [[semigroup]], [[magma]]
Examples: <i>Not Applicable</i>

# Category

``` ad-Definition
title: Definition (Category of Groups).
The [[category|category]] $\Grp$ consists of groups as objects and group homomorphisms as morphisms.
```

## Objects of $\Grp$

``` ad-Definition
title: Definition (Group).
A <u>group</u> is a [[set|set]] $G$ together with a binary operation $$\ast: G \times G \to G$$ that is:
1. Associative: $$\forall g,h,k \in G: \, (g \ast h) \ast k = g \ast (h \ast k)$$
2. Unital: $$\exists e \in G \, \forall g \in G: e \ast g = g \ast e = g$$
3. Invertible: $$\forall g \in G \exists g^{-1} \in G: g\ast g^{-1} = g^{-1} \ast g=e$$
```

*Remarks*
1. One can also define this rather tersely by saying that a group is a [[groupoid|groupoid]] with one object.
2. If the group operation is clear from context, we often omit it from notation.


## Morphisms of $\Grp$

``` ad-Definition
title: Definition (Group Homomorphism).
Let $G,H$ be groups. A <u>group homomorphism</u> is a function $$\phi: G \to H$$ such that for all $g,g' \in G$: $$\phi(g \ast_G g')=\phi(g)\ast_H \phi(g').$$
The group homomorphisms between $G$ and $H$ are denoted by $\Hom_\Grp(G,H)$.
```

*Remark*
Similarly, we could have demanded that $\phi$ makes the following diagram commute:
```tikz
\usepackage{amsmath,amssymb,pgfplots, amstext, amsfonts, tikz-cd}
\usetikzlibrary{decorations.pathreplacing}
\begin{document}
\tikzset{every picture/.style={line width=0.75pt}} %set default line width to 0.75pt        
\begin{tikzcd}[x=0.75pt,y=0.75pt,yscale=-0.5,xscale=0.5]
    G \times G \ar[r, "\varphi \times \varphi"] \ar[d, "- \ast_G -"] & H \times H \ar[d, "- \ast_H -"]\\
G \ar[r, "\varphi"] & H
\end{tikzcd}
\end{document}
```


# Opposite Group

```ad-Definition
title: Definition (Opposite Group).
Given a group $(G, \cdot)$, the opposite group $G^\op$ has the same underlying set $G$, but $$g \cdot^\op h := h \cdot g$ for all $g,h \in G$.
```
