<div class="topSpace"></div>

Date Created: 27th March 2025
References: #Ref/Aluffi 
Tags: #Type/Definition

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

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
