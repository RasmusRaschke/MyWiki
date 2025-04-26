<div class="topSpace"></div>

Date Created: [[26/04/2025]]
References: #Ref/AlgTop 
Tags: #Type/Proposition #Topic/AlgebraicTopology 

Proved by: <i>Not Applicable</i>
References: [[short exact sequence]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition (Existence of Connecting Homomorphism).
Let
$$
0 \to A_\ast \overset{f_\ast}\to B_\ast \overset{g_\ast}\to C_\ast \to 0
$$
be a [[short exact sequence#Of Chain Complexes $ Ch$|short exact sequence of chain complexes]]. There exists a homomorphism
$$
\delta: H_n(C_\ast) \to H_{n-1}(A_\ast)
$$
for all $n \in \Z$ which is natural, called <ins>connecting homomorphism</ins>.
```
The naturality can be stated as follows: If
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
0 \arrow[r] & A_\ast \arrow[r,"f"] \arrow[d,"\alpha"]& B_\ast \arrow[r, "g_\ast"] \arrow[d, "\beta"]& C_\ast \arrow[r] \arrow[d, "\gamma"]&0\\
0 \arrow[r] & A'_\ast \arrow[r,"f_\ast'"] & B'_\ast \arrow[r, "g'_\ast"] & C'_\ast \arrow[r]&0\\
\end{tikzcd}
\end{document}
```
is a commutative diagram of [[chain complex#Chain Map|chain maps]] with exact rows then
$$
H_{n-1}(\alpha) \delta = \delta H_n(\gamma),
$$
and the diagram
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
H_n(C_\ast) \arrow[r,"\delta"] \arrow[d, "H_n(\gamma)"]& H_{n-1}(A_\ast) \arrow[d, "H_{n-1}(\alpha)"]\\
H_n(C_\ast') \arrow[r, "\delta"]& H_{n-1}(A_\ast')
\end{tikzcd}
\end{document}
```
commutes. Implicitly, we state that $\delta$ is not the zero map.
*Proof.*
