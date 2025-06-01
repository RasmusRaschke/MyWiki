<div class="topSpace"></div>

Date Created: [[18/05/2025]]
References: #Ref/AlgTop 
Tags: #Type/Definition

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: [[homology]], [[singular simplex]], [[chain complex]]
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Chain Complex with Coefficients

``` ad-Definition
title: Definition (Singular Chain Complex with Coefficients).

Let $X$ be a [[topological space]]. The <ins>singular chain complex with coefficients</ins> in $G$ is given by
$$
S_n(X;G) = \bigoplus_{\{\alpha: \Delta^n \to X\}} G. 
$$
```
Elements in $S_n(X;G)$ are finite sums $\sum_{i=1}^N g_i \alpha_i$ with $g_i \in G$ and $\alpha_i: \Delta^n \to X$. Addition is given by
$$
\sum_{i=1}^N g_i \alpha_i + \sum_{i=1}^N h_i \alpha_i = \sum_{i=1}^N (g_i+h_i) \alpha_i.
$$

**Remark.**
This yields an obvious [[isomorphism]] $S_n(X;G) \cong S_n(X) \otimes G$.
# Homology with Coefficients

``` ad-Definition
title: Definition (Singular Homology with Coefficients).
Let $X$ be a [[topological space]]. The <ins>$n$-th singular homology group with coefficients</ins> in $G$ is given by
$$
H_n(X;G):=H_n(S_\ast(X;G))
$$
with the boundary operator $\partial: S_n(X;G) \to S_{n-1}(X;G)$ obtained by
$$
\partial \left( \sum_{i=1}^N g_i \alpha_i \right) = \sum_{j=0}^N (-1)^j \left( \sum_{i=1}^N g_i(\alpha_i d_j\right).
$$

```
**Remark.**
In agreement with our usual definition where $G = \Z$ we have $H_n(X) \cong H_n(X;\Z)$ for all spaces $X$.


## Cellular Homology with Coefficients

``` ad-Definition
title: Definition (Cellular Homology with Coefficients).
We define $C_n(X;G)$ analogously by $H(X^n, X^{n-1}; G)$ and denote $c \in C_n(X;G)$ by 
$$
c = \sum_{i=1}^N g_i \sigma_i \in \bigoplus_{\sigma} G
$$
with $\sigma$ being an $n$-cell. The boundary operator $\tilde{d}$ turns into
$$
\tilde{d}c = \sum_{i=1}^N g_i d\sigma_i)
$$
where $d: C_n(X) \to C_{n-1}(X)$ is the usual boundary operator in the [[homology#Cellular Homology|cellular complex]].
```
**Remark.**
Note that [[cellular and singular homology|our theorem about cellular and singular homology]] transfers to this case to yield
$$
H_n(X;G) \cong H_n(C_\ast(X;G), \tilde{d} ).
$$
 **Example.**
 Consider [[projective space#Of general Projective Spaces|$\R P^2$]]: For $G=\Z$ we have $H_0(\R P^2) \cong \Z$, $H_1(\R P^2) \cong \Z / 2\Z$ and $H_2(\R P^2) \cong 0$. Considering $G= \Z / 2\Z$ changes the homology drastically: The cellular chain complex is now given by
 ```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\newcommand{\Z}{\mathbb{Z}}
\begin{document}
\begin{tikzcd}[scale=3]
0 \ar[r] & \Z / 2\Z \ar[r, "\cdot 2 = \cdot 0"] & \Z / 2\Z  \ar[r, "0"] & \Z / 2\Z \ar[r] & 0
\end{tikzcd}
\end{document}
```
and hence $H_i(\R P^2; \Z / 2\Z) \cong \Z / 2\Z$ for $0 \leq i \leq 2$.
For $H_\ast(\R P^2;\Q)$, the picture changes again: The cellular chain complex looks like this
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\newcommand{\Z}{\mathbb{Q}}
\begin{document}
\begin{tikzcd}[scale=3]
0 \ar[r] & \Z  \ar[r, "\cdot 2 "] & \Z \ar[r, "0"] & \Z \ar[r] & 0
\end{tikzcd}
\end{document}
```
where multiplication by $2$ is an [[isomorphism]], so $H_0(\R P^2; \Q) \cong \Q$, $H_1(\R P^2; \Q) \cong \Q / 2\Q$ and $H_2(\R P^2; \Q) \cong 0$.