<div class="topSpace"></div>

Date Created: [[01/05/2025]]
References: #Ref/AlgTop 
Tags: #Type/Theorem 

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: [[sphere#Homology]]

We consider the following situation: $X$ is a [[topological space|topological space]] with open subspaces $X_1, X_2 \sub X$ such that $X=X_1 \cup X_2.$ Let $\fU:= \{X_1,X_2\}$ be an open covering of $X$. This is reflected in the diagram:
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
& X_1 \arrow[dr, "\kappa_1"]& \\
X_1 \cap X_2 \arrow[dr, "\iota_2"'] \arrow[ur, "\iota_1"]& &X \\
& X_2 \arrow[ur, "\kappa_2"']& 
\end{tikzcd}
\end{document}
```

This immediately yields an exact sequence

```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
0 \arrow[r] & S_\ast (X_1 \cap X_2) \arrow[r, "(\iota_1 {,} \iota_2)"] & S_\ast(X_1) \oplus S_\ast(X_2) \arrow[r] & S_\ast^\mathfrak{U}(X) \arrow[r]& 0
\end{tikzcd}
\end{document}
```
where the second map is given by
$$
(\alpha_1, \alpha_2) \mapsto \kappa_1(\alpha_1) - \kappa_2(\alpha_2).
$$

``` ad-Theorem
title: Theorem (of Mayer and Vietoris).
There exists a [[long exact sequence]] 
$$
\cdots \overset{\delta}\longrightarrow H_n(X_1 \cap X_2) \longrightarrow H_n(X_1) \oplus H_n(X_2) \longrightarrow H_n(X)\overset{\delta}\longrightarrow H_{n-1}(X_1 \cap X_2) \overset{H_{n-1}(f_\ast)}\longrightarrow \cdots.
$$
```
*Proof.*
Follows from [[small singular simplex#Impact on Homology|this proposition]] because $H_n^\fU (X) \cong H_n(X).$<span style="float:right;">$\blacksquare$</span>