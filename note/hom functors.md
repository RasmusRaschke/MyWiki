<div class="topSpace"></div>

Date Created: [[04/05/2025]]
References: #Ref/Aluffi 
Tags: #Type/Definition #Topic/CategoryTheory 

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[functor]]
Examples: <i>Not Applicable</i>

# Definition

``` ad-Definition
title: Definition (Hom Functor).
Let $\tC$ be a [[category]] and $X \in \Obj(\tC).$ The assignment
$$
\begin{align}
\Hom_\tC(X, \cdot): \tC &\to \Set\\
A &\mapsto \Hom_C(X,A)
\end{align}
$$
defines the <ins>covariant hom-functor</ins>, while
$$
\begin{align}
\Hom_\tC(\cdot, X): \tC &\to \Set\\
A &\mapsto \Hom_C(A,X)
\end{align}
$$
defines the <ins>contravariant hom-functor</ins> on $\tC$. We denote $\Hom_\tC(X, \cdot)$ by $h^X$ and $\Hom_\tC(\cdot, X)$ by $h_X$ for short.
```

Pictorially, if
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
A \arrow[r,"\alpha"]&B\arrow[r,"\beta"]&C
\end{tikzcd}
\end{document}
```
is a diagram in $\tC,$ consider the diagram
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
A \arrow[r,"\alpha"] \ar[dr,"\xi_A"'] &B \ar[d,"\xi_B"] \arrow[r,"\beta"]&C \ar[dl,"\xi_C"]\\
& X & .
\end{tikzcd}
\end{document}
```
Every morphism $\alpha: A \to B$ gives rise to a function
$$
\Hom_\tC (B, X) \to \Hom_\tC(A,X)
$$
by mapping $\xi_B \mapsto \xi_A:= \xi_B \alpha,$ requiring commutativity of the left triangle. Associativity reads as
$$
\xi_C (\beta \alpha)=(\xi_C \beta)\alpha,
$$
displaying the contravariant property.