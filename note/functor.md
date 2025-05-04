<div class="topSpace"></div>

Date Created: [[04/05/2025]]
References: #Ref/Aluffi 
Tags: #Type/Definition #Topic/CategoryTheory 

Proved by: <i>Not Applicable</i>
References: [[category]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Definition

## Covariant Functors

``` ad-Definition
title: Definition (Covariant Functor).

Let $\tC, \tD$ be two [[category|categories]]. A <ins>covariant functor</ins>
$$
\sF: C \to D
$$
is an assignment of an object $\sF(A) \in \Obj(\tD)$ for every $A \in \Obj(\tC)$ and of a function
$$
\Hom_\tC(A,B) \overset{\sF}\to \Hom_\tD (\sF(A), \sF(B))
$$
for every pair $A,B \in \Obj(\tC)$ such that for all $A,B,C \in \Obj(\tC),$ all $\alpha \in \Hom_\tC(A,B)$ and all $\beta \in \Hom_\tC(B,C):$
1. $\sF(1_A) = 1_{\sF(A)},$
2. and $\sF(\beta \alpha)=\sF(\beta)\sF(\alpha).$
```

**Remark.**
Covariant functors are assignments which preserve arrows. If
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
& B \ar[dr, "\beta"]& \\
A \ar[ur, "\alpha_1"] \ar[dr,"\alpha_3"'] \ar[rr, "\alpha_2"]& & D \\
& C \ar[ur, "\gamma"']& 
\end{tikzcd}
\end{document}
```
is a diagram in $\tC$, it is mapped to a diagram
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\DeclareMathOperator{\sF}{\mathcal{F}}
\begin{document}
\begin{tikzcd}[scale=3]
& \sF(B) \ar[dr, "\sF(\beta)"]& \\
\sF(A) \ar[ur, "\sF(\alpha_1)"] \ar[dr,"\sF(\alpha_3)"'] \ar[rr, "\sF(\alpha_2)"]& & \sF(D) \\
& \sF(C) \ar[ur, "\sF(\gamma)"']& 
\end{tikzcd}
\end{document}
```
preserving all arrow directions.

## Contravariant Functors

``` ad-Definition
title: Definition (Contravariant Functor).

Let $\tC, \tD$ be two [[category|categories]]. A <ins>contravariant functor</ins> or <ins>presheaf</ins>
$$
\sG: C \to D
$$
is an assignment of an object $\sG(A) \in \Obj(\tD)$ for every $A \in \Obj(\tC)$ and of a function
$$
\Hom_\tC(B,A) \overset{\sG}\to \Hom_\tD (\sF(A), \sF(B))
$$
for every pair $A,B \in \Obj(\tC)$ such that for all $A,B,C \in \Obj(\tC),$ all $\alpha \in \Hom_\tC(A,B)$ and all $\beta \in \Hom_\tC(B,C):$
1. $\sG(1_A) = 1_{\sG(A)},$
2. and $\sG(\beta \alpha)=\sG(\alpha)\sG(\beta).$
```

**Examples.**
1. We can forget the group structure of a group $(G, \circ)$ to obtain a [[set]]. This gives rise to a so-called <ins>forgetful functor</ins> $\Grp \to \Set.$
2. If $R$ is a ring with $R^\ast$ being the group of units of $R$, every ring homomorphism $R \to S$ induces a group homomorphism $R^\ast \to S^\ast.$ This defines a covariant functor $\Ring \to \Grp$


**Remark.**
A contravariant functor can be thought of a covariant functor from the [[category#Opposite category|opposite category]] $\tC^{\text{op}}$ to $\tD$. Such a functor reverses all arrows: If
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
& B \ar[dr, "\beta"]& \\
A \ar[ur, "\alpha_1"] \ar[dr,"\alpha_3"'] \ar[rr, "\alpha_2"]& & D \\
& C \ar[ur, "\gamma"']& 
\end{tikzcd}
\end{document}
```
is a diagram in $\tC$, it is mapped to a diagram
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\DeclareMathOperator{\sF}{\mathcal{G}}
\begin{document}
\begin{tikzcd}[scale=3,arrows=<-]
& \sF(B) \ar[dr, "\sF(\beta)"]& \\
\sF(A) \ar[ur, "\sF(\alpha_1)"] \ar[dr,"\sF(\alpha_3)"'] \ar[rr, "\sF(\alpha_2)"]& & \sF(D) \\
& \sF(C) \ar[ur, "\sF(\gamma)"']& 
\end{tikzcd}
\end{document}
```
in which all arrows are reversed. This is seen by looking at the composition rule. If
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
A \ar[r,"\alpha"] \ar[rr, bend right, "\beta \alpha"'] &B \ar[r, "\beta"]& C
\end{tikzcd}
\end{document}
```
is a diagram in $\tC$, it is mapped to a diagram
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\DeclareMathOperator{\sG}{\mathcal{G}}
\begin{document}
\begin{tikzcd}[scale=3, arrows=<-]
\sG(A) \ar[r,"\sG(\alpha)"] \ar[rr, bend right, "\sG(\beta \alpha)"'] &\sG(B) \ar[r, "\sG(\beta)"]& \sG(C).
\end{tikzcd}
\end{document}
```

In both cases, functors map commutative diagrams to commutative diagrams.


# Additivity

``` ad-Definition
title: Definition (Additive Functors).
Let $\tC, \tD$ be two [[category|categories]] such that all homsets $\Hom_\tC$ and $\Hom_\tD$ have the additional structure of an abelian group. If $\sF:\tC \to \tD$ is a functor such that
$$
\Hom_\tC \overset{\sF}\to \Hom_\tD
$$
is a group homomorphism, $\sF$ is called <ins>additive</ins>.
```