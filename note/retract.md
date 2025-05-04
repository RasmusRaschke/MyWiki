<div class="topSpace"></div>

Date Created: [[30/04/2025]]
References: #Ref/Topo #Ref/AlgTop #Ref/LeeTop
Tags: #Type/Definition

Proved by: [[Mayer-Vietoris sequence]]
References: [[bouquet#Homology]], [[homology]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Deformation Retraction

``` ad-Definition
title: Definition (Deformation Retraction).
Let $X$ be a [[topological space|topological space]] and $A \sub X$ be a subspace. A continuous map $$r: X \to A$$ is called <ins>deformation retraction</ins> if $\iota_A r \simeq \id_X$, turning $A$ into a <ins>deformation retract</ins> of $X$.

```
Since $\iota_Ar \simeq \id_X$ and $r \iota_A \simeq \id_A$, $\iota_A$ and $r$ are homotopy equivalences.

## Impact on Homology

``` ad-Proposition
title: Proposition (Homology of Deformation Retracts).

Let $X$ be a [[topological space|topological space]] with a closed subspace $A \sub X$ such that $A$ is a deformation retract of some open neighbourhood $A \sub U \sub X$. Denote the image of $A$ under $\pi: X \to X/A$ by $b$. Then $X/A$ is well-pointed with respect to $b$ and
$$
H_n(X, A) \cong \tilde{H}_n(X/A)
$$
for all $n \geq 0.$
```
*Proof.*
The projection $\pi$ induces a homeomorphism
$$
(X \setminus A, U \setminus A) \cong ((X / A) \setminus \{b\}, \pi(U) \setminus \{b\}). 
$$
Consider the diagram
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
H_n(X,A) \ar[r, "\cong"] \ar[d, "H_n(\pi)"]& H_n(X,U) & H_n(X \setminus A, U \setminus A) \ar[l, "\cong"'] \ar[d, "\cong"', "H_n(\pi)"]\\
H_n(X/A, b) \ar[r, "\cong"]& H_n(X/A, \pi(U)) & \ar[l, "\cong"'] H_n((X/A)\setminus \{b\}, \pi(U) \setminus \{b\})
\end{tikzcd}
\end{document}
```

The isomorphisms from the left to the middle are justified by $A$ being a deformation retract of $U$. The isomorphism from the right to the middle are given by [[excision theorem|excision]] since $A = \overline{A} \sub U$ and $\overline{\{b\}} = \{b\} \sub \pi(U)$.
<span style="float:right;">$\blacksquare$</span>

# Strong Retraction

``` ad-Definition
title: Definition (Strong Deformation Retraction).
A deformation retraction $r: X \to A$ is called <ins>strong</ins> if $\iota_Ar$ is homotopic to $\id_X$ relative to $A$.

```

# Weak Retraction

``` ad-Definition
title: Definition (Weak Retraction).
A <ins>weak retract</ins> $r: X \to A$ is a continuous map such that $r\iota_A \simeq \id_A$, turning $A$ into a <ins>weak retract</ins> of $X$.

```

