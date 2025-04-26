<div class="topSpace"></div>

Date Created: [[26/04/2025]]
References: #Ref/AlgTop 
Tags: #Type/Definition

Proved by: <i>Not Applicable</i>
References: [[group]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Of Abelian Groups

``` ad-Definition
title: Definition (Short Exact Sequence in $\mathtt{AGrp}$).

A <ins>short exact sequence</ins> of abelian groups is a sequence
$$
\{0\} \to A \overset{f}\to B \overset{g}\to C \to \{0\}
$$
such that $f$ and $g$ are homomorphisms, $f$ is injective, $g$ is surjective and $$\im(f)=\ker(g).$$
```
**Examples.**
1. The sequence 
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
0 \arrow[r] &\mathbb{Z} \arrow[r,"2\cdot"]& \mathbb{Z} \arrow[r, "\pi"]& \mathbb{Z}/2 \mathbb{Z} \arrow[r]&0
\end{tikzcd}
\end{document}
```
is short exact since $\pi(2k)=[2k] \mod 2=[0]$ is always true.

**Remarks.**
1. A [[monomorphism]] $\iota: U \to A$ always gives rise to a short exact sequence $0 \to U \overset{\iota}\to A$.
2. Analogously, an [[epimorphism]] $\rho: B \to Q$ procures a short exact sequence $B \overset{\rho}\to Q \to 0$.
3. An [[isomorphism]] $\phi: A \to A'$ corresponds to the short exact sequence $0 \to A \overset{\phi}\to A' \to 0$.
4. Considering the [[homology]] of an exact sequence, homology measures the degree to which the sequence fails to be exact.

# Of Chain Complexes $\Ch$

``` ad-Definition
title: Definition (Short Exact Sequence in $\Ch$).

Let $A_\ast, B_\ast, C_\ast$ be [[chain complex|chain complexes]] with [[chain complex#Chain Map|chain maps]] 
$$
A_\ast \overset{f_\ast}\to B_\ast \overset{g_\ast}\to C.
$$
This sequence is called <ins>exact</ins> if $$\im(f_n)=\ker(g_n)$$ for all $n\in \Z$.
```
This means exactness corresponds to a commuting double ladder:
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
\vdots \arrow[d,"d"] &  \vdots \arrow[d,"d"]& \vdots \arrow[d,"d"]\\
A_{n+1} \arrow[d,"d"] \arrow[r, "f_{n+1}"] & B_{n+1} \arrow[r, "g_{n+1}"] \arrow[d,"d"]&C_{n+1}\arrow[d,"d"]\\
A_{n} \arrow[d,"d"] \arrow[r, "f_{n}"]&  B_{n} \arrow[d,"d"] \arrow[r, "g_{n}"] &C_{n} \arrow[d,"d"]\\
A_{n-1} \arrow[d,"d"] \arrow[r, "f_{n-1}"] & B_{n-1} \arrow[d,"d"] \arrow[r, "g_{n-1}"] &C_{n-1} \arrow[d,"d"]\\
\vdots & \vdots &\vdots 
\end{tikzcd}
\end{document}
```
where every row is exact.

**Example.**
For any prime $p$, there is a chain exact sequence
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\newcommand{\Z}{\mathbb{Z}}
\begin{document}
\begin{tikzcd}[scale=3]
\vdots \arrow[d] &  \vdots \arrow[d]& \vdots \arrow[d]\\
\Z \arrow[d,"\cdot p"] \arrow[r, "\text{id}"] & \Z \arrow[r, "0"] \arrow[d,"\cdot p^2"]&0 \arrow[d]\\
\Z \arrow[d,"\pi"] \arrow[r, "\cdot p"]&  \Z \arrow[d,"\pi"] \arrow[r, "\pi"] &\Z/p\Z \arrow[d,"\text{id}"]\\
\Z/p\Z \arrow[d] \arrow[r, "\cdot p"] & \Z/p\Z \arrow[d] \arrow[r, "\pi"] &\Z/p\Z \arrow[d]\\
\vdots & \vdots &\vdots 
\end{tikzcd}
\end{document}
```
with exact rows and columns.