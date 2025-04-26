<div class="topSpace"></div>

Date Created: [[26/04/2025]]
References: #Ref/Aluffi 
Tags: #Type/Definition

Proved by: <i>Not Applicable</i>
References: [[product]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Definition

``` ad-Definition
title: Definition (Coproduct).
A [[category|category]] $\tC$ is said to have a <ins>coproduct</ins> $A \coprod B \in \Obj(\tC)$ for $A,B \in \Obj(\tC)$ if [[coslice category|$\tC^{A,B}$]] has [[category#Terminal Objects|initial objects]]. It comes with morphisms $\iota_A: A \to A \coprod B$ and $\iota_B: B \to \iota_B$, called <ins>canonical injections</ins>.
```
This is equivalent to the following universal property:
For all $Z \in \Obj(\tC)$ and morphisms Sf_A \in \Hom_\tC(A,Z),f_B \in \Hom_\tC(B,Z)$ there is a unique morphism $\sigma: A \coprod B \to Z$ such that the following diagram commutes:
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
A\arrow[dr, "\iota_A"] \arrow[drr, bend left, "f_A"]& &  \\
& A \coprod B \arrow[r, "\sigma"] &Z\\
B\arrow[ur, "\iota_B"'] \arrow[urr, bend right, "f_B"']& & .
\end{tikzcd}
\end{document}
```
**Example.**
Dual to [[product|products]], the category $(\Z, \leq)$ has coproducts, this time given by $a \coprod b := \max(a,b)$.