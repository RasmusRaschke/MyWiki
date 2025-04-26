<div class="topSpace"></div>

Date Created: 27th March 2025
References: #Ref/Aluffi 
Tags: #Type/Definition #Topic/CategoryTheory

Proved by: <i>Not Applicable</i>
References: [[set]]
Justifications: [[slice category]]

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: [[cartesian products]]

# Universal Products

``` ad-Definition
title: Definition (Product).
A [[category|category]] $\tC$ is said to have <ins>(finite) products</ins> if for all $A,B \in  \Obj(\tC)$ the [[slice category|slice category]] $C_{A,B}$ has [[category#Terminal Objects|final objects]]. Such a final object consists of an [[category|object]] $$A \times B,$$ called <ins>product</ins> of $A$ and $B$, and two morphisms $\pi_A: A \times B \to A$ and $\pi_B: A \times B \to B$, called <ins>canonical projections</ins>.

```
This is equal to the following universal property: For all $Z \in \Obj(\tC)$ and all morphisms $f_A \in \Hom_\tC (Z,A), f_B \in \Hom_\tC (Z,B)$, there is a unique morphism $\sigma: Z \to A \times B$ such that the following diagram commutes:
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
 & & A \\
 Z \arrow[r, "\sigma"] \arrow[urr, bend left, "f_A"] \arrow[drr, bend right, "f_B"']& A \times B \arrow[ur, "\pi_A"] \arrow[dr, "\pi_B"'] & \\
 & & B
\end{tikzcd}
\end{document}
```

**Example.**
Products do not have to look like classical [[cartesian products]]. Consider the category given by $(\Z, \leq)$. Products would be of form $a \times b$ for $a,b \in \Z$ with the universal property being that for all $z \in \Z$ with $z \leq a$ and $z \leq b$, we have $z \leq a \times b$. This problem is solved by the minimum operation $a \times b := \min(a,b)$ is actually a solution.

