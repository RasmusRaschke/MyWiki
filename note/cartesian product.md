<div class="topSpace"></div>

Date Created: [[26/04/2025]]
References: #Ref/Aluffi 
Tags: #Type/Definition

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[product]]
Examples: <i>Not Applicable</i>

# Definition
``` ad-Definition
title: Definition (Cartesian Product).

Let $\{A_i\}_{i \in I}$ be a family of sets indexed by $I$. The <ins>(cartesian) product</ins> $$\prod_{i \in I} A_i = A_1 \times A_2 \times \cdots $$ consists of ordered $|I|$-tuples $(a_1, a_2, \dots)$ with $a_i \in A_i$ for all $i \in I$.

```

**Remark.**
The cartesian product is equipped with <ins>canonical surjections</ins> called <ins>projections</ins> $\pi_A$ and $\pi_B$:
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
& A \times B \arrow[dr, twoheadrightarrow, "\pi_A"'] \arrow[dl, twoheadrightarrow, "\pi_B"] &\\
A& &B
\end{tikzcd}
\end{document}
```
defined by $\pi_A((a,b))=a$ and $\pi_B((a,b))=b$, respectively.

# Universal Property

``` ad-Proposition
title: Proposition (Universal Property of the Cartesian Product).

Let $A,B \in \Obj(\Set)$. Their cartesian product $A \times B$ satisfies the following universal property:
	For all $Z \in \Obj(\Set)$ and morphisms $f_A: Z \to A$ and $f_B: Z \to B$ there is a unique morphism $\sigma: Z \to A \times B$ such that $f_A=\pi_A \sigma$ and $f_B = \pi_B \sigma$.
```
Note that this is equivalent to the following diagram being commutative:
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
This justifies the notation $\sigma = f_A \times f_B$.
*Proof.*
For $z \in Z$, we make the obvious choice and define $\sigma: Z \to A \times B$ by $\sigma(z):=(f_A(z), f_B(z))$. Clearly, we have $\pi_A \sigma(z)=f_A(z)$ and $\pi_B \sigma(z)=f_B(z)$. By commutativity of the diagram, any other $\sigma'$ is necessarily equal to $\sigma$.<span style="float:right;">$\blacksquare$</span>