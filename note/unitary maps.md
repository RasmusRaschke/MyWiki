<div class="topSpace"></div>

Date Created: [[21/04/2025]]
References: #Ref/SympGeo 
Tags: #Type/Definition #Topic/Topology #Topic/LinearAlgebra

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Definition

``` ad-Definition
title: Definition (Unitary Group).

Let $(V, \langle \cdot, \cdot \rangle_V),(W, \langle \cdot, \cdot \rangle_W)$ be inner product spaces. A linear map $T: V \to W$ is called <ins>unitary</ins> if
$$
\forall u,v \in V: \langle Tu, Tv \rangle_W = \langle u,v \rangle_V
$$
is satisfied. If $V,W$ are of finite dimension $n$, the group of unitary linear maps is called <ins>unitary group</ins> and denoted $\UU(V,n)$ or $\UU(n)$ for short.
```


# Fundamental Group

``` ad-Proposition
title: Proposition (Fundamental Group of $\UU(n)$).

The complex determinant $\det_\C: \UU(n) \to \S^1$ induces a fundamental group isomorphism $$\pi_1(\UU(n)) \cong \pi_1(\S^1) \cong \Z.$$
```
*Proof.*
First, we show that $\SU(n)$ is simply connected. This holds trivially for $n=1$, so assume $n \geq 2$ and consider the fibration
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
p^{-1}(O) \subseteq \text{SU}(n) \arrow[d, "p|_{p^{-1}(O)}"'] \arrow[r] & O \times \text{SU} (n-1) \arrow[dl, "\text{pr}_1"]\\
O \subseteq \mathbb{S}^{2n-1} &
\end{tikzcd}
\end{document}
```
where $p$ projects a matrix to its first column. This induces an exact sequence of homotopy groups given by
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
\pi_2(\mathbb{S}^{2n-1}) \arrow[r] & \pi_1(\text{SU}(n-1)) \arrow[r] & \pi_1(\text{SU}(n)) \arrow[r, "p_\ast"] & \pi_1(\mathbb{S}^{2n-1}).
\end{tikzcd}
\end{document}
```
Henceforth, if $\SU(n-1)$ is simply connected so is $\SU(n)$.
Now, consider the fibre bundle given by
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
p^{-1}(O) \subseteq \text{U}(n) \arrow[d, "\text{det}_\mathbb{C}|_{p^{-1}(O)}"'] \arrow[r] & O \times \text{SU} (n) \arrow[dl, "\text{pr}_1"]\\
O \subseteq \mathbb{S}^{1} &
\end{tikzcd}
\end{document}
```
This again induces an exact sequence of homotopy groups
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
\{1\} \arrow[r]& \pi_1(\text{U}(n)) \arrow[r, "(\text{det}_\mathbb{C})_\ast"] &\pi_1(\mathbb{S}^{1})\arrow[r] & \pi_0(\text{SU}(n)) = \{1\}.
\end{tikzcd}
\end{document}
```
which implies $\pi_1(\UU(n)) \cong \pi_1(\S^1) \cong \Z$.
<span style="float:right;">$\blacksquare$</span>