<div class="topSpace"></div>

Date Created: [[29/04/2025]]
References: #Ref/AlgTop 
Tags: #Type/Theorem 

Proved by: <i>Not Applicable</i>
References: [[homology#Relative Homology]]
Justifications: [[relative chain complex]]

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Theorem
title: Theorem (Long Exact Sequence for a Pair of Spaces).
Let $(X,A)$ be a pair of [[topological space|topological spaces]] with $A \sub X$. This yields a [[long exact sequence|long exact sequence]]
$$
\cdots \overset{\delta}\longrightarrow H_n(A) \overset{H_n(\iota)}\longrightarrow H_n(X)\longrightarrow H_n(X,A)\overset{\delta}\longrightarrow H_{n-1}(A) \overset{H_{n-1}(\iota)}\longrightarrow \cdots.
$$
In addition, if $f:(X,A) \to (Y,B)$ is a continuous map between pairs of spaces, a map between [[long exact sequence|long exact sequences]] is induced, as seen below.
```

```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
\cdots \arrow[r,"\delta"] & H_n(A)\arrow[r, "H_n(\iota)"] \arrow[d, "H_n(f|_A)"] & H_n(X) \arrow[r] \arrow[d, "H_n(f)"] & H_n(X,A) \arrow[r, "\delta"] \arrow[d, "H_n(f)"] & H_{n-1}(A) \arrow[r, "H_{n-1}(\iota)"] \arrow[d, "H_{n-1}(f|_A)"] &\cdots\\
\cdots \arrow[r,"\delta"] & H_n(B)\arrow[r, "H_n(\iota)"] & H_n(Y) \arrow[r] & H_n(Y,B) \arrow[r, "\delta"] & H_{n-1}(B) \arrow[r, "H_{n-1}(\iota)"]&\cdots\\
\end{tikzcd}
\end{document}
```
*Proof.*
By definition of $S_\ast(X,A)$,
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
0 \arrow[r] & S_\ast (A) \arrow[r, "S_\ast (\iota)"] & S_\ast (X) \arrow[r, "\pi"] & S_\ast (X,A) \arrow[r]& 0
\end{tikzcd}
\end{document}
```
is a [[short exact sequence#Of Chain Complexes $ Ch$|ses of chain complexes]]. By this [[homology long sequence|proposition]] the homology long sequence follows. For any map $f$ between pairs of spaces the following diagram commutes:
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
0 \arrow[r] & S_n (A) \arrow[r, "S_\ast (\iota)"] \arrow[d, "S_n(f|_A)"] & S_n (X) \arrow[r, "\pi"] \arrow[d, "S_n(f)"] & S_n (X,A) \arrow[r] \arrow[d, "S_n(f)/S_n(f|_A)"]& 0\\
0 \arrow[r] & S_n (B) \arrow[r, "S_n (\iota)"] & S_n (X) \arrow[r, "\pi"] & S_n (Y,B) \arrow[r]& 0.
\end{tikzcd}
\end{document}
```
<span style="float:right;">$\blacksquare$</span>

**Example.**
Consider $A=\S^{n-1}$ and $X=\D^n$. For all $j>0$, $H_j(\iota)$ is trivial. The long exact sequence procures an [[isomorphism]] $$\delta: H_j(\D^n, \S^{n-1}) \cong H_{j-1}(\S^{n-1})$$ for $j>1$ and $n\geq 1$.