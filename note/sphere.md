<div class="topSpace"></div>

Date Created: [[21/04/2025]]
References: #Ref/LeeSmooth 
Tags: #Type/Definition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Definition

``` ad-Definition
title: Definition (Unit Sphere).

For some $n \geq 0$, define the <ins>$n$-dimensional unit sphere</ins>
$$
\S^n := \{x \in \R^{n+1} \mid \|x\|=1\} \sub \R^{n+1}.
$$

```

# Manifold

``` ad-Proposition
title: Proposition (Spheres are Manifolds).
The unit sphere $\S^n$ is for all $n\geq 0$ a $n$-dimensional [[manifold#Topological Manifold|manifold]].

```
*Proof.*
As a subspace of $\R^{n+1}$, all unit spheres are Hausdorff and second countable. For each $0 \leq i \leq n+1$, define
$$
U_i^{\pm} := \{(x^1, \dots, x^{n+1}) \mid x^i \gtrless 0\} \sub \R^{n+1}
$$
and consider the continuous function $f(u)= \sqrt{1- |u|^2}$.

# Homology

``` ad-Proposition
title: Proposition (Homology of Spheres).
We have
$$
H_n(\S^m) \cong \begin{cases}
\Z \oplus \Z, \ &n=m=0,\\
\Z, \ &n=0, m>0,\\
\Z, \ &n=m>0\\
\{0\}, \ &\text{otherwise.}
\end{cases}
$$
```
*Proof.*
Let $X=\S^m$ and $X^\pm := \S^m \setminus \{\mp e_{m+1}\}.$ Since $X^\pm$ are contractible, $H_\ast(X^\pm)=0.$ The [[Mayer-Vietoris sequence|Mayer-Vietoris sequence]] reads as follows:
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
\cdots \arrow[r, "\delta"] & H_n(X^+ \cup X^-) \arrow[r] & H_n(X^+) \oplus H_n(X^-) \arrow[r] & H_n(\mathbb{S}^m) \arrow[r, "\delta"] & H_{n-1}(X^+ \cup X^-) \arrow[r]& \cdots
\end{tikzcd}
\end{document}
```

With the [[connecting homomorphism]] $\delta$ and the second map
$$
H_{n-1}(\iota): H_n(\S^{m-1}) \to H_{n-1}(X^+ \cap X^-)
$$
induced by the inclusion $\iota: \S^{m-1} \hookrightarrow X^+ \cap X^-$ we obtain an [[isomorphism]] for $n \geq 2:$
$$
H_n(\S^m) \cong H_{n-1}(X^+ \cap X^-) \cong H_{n-1}(\S^{m-1}).
$$
Now define $D:=H_{n-1}(\iota)^{-1}\delta$, which is again an [[isomorphism]] for all $n \geq 2$. We have to control smaller dimensions.
The [[hurewicz theorem|hurewicz isomorphism]] yields $H_1(\S^m) \cong \{0\}$ for $m > 1$ and $H_1(\S^1) \cong \Z.$
For $0<n<m$ we obtain
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
H_n(\mathbb{S}^m) \arrow[r, "\cong"]& H_{n-1}(\mathbb{S}^{m-1}) \arrow[r, "\cong"]& \cdots \arrow[r, "\cong"]& H_1(\mathbb{S}^{m-n+1}) \cong \pi_1(\mathbb{S}^{m-n+1}) \cong \{0\}.
\end{tikzcd}
\end{document}
```
Similarly, for $0<m<n$ we get
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
H_n(\mathbb{S}^m) \arrow[r, "\cong"] & H_{n-1}(\mathbb{S}^{n-1}) \arrow[r, "\cong"]& \cdots \arrow[r, "\cong"]& H_{n-m+1} (\mathbb{S}^1) \cong \{0\}
\end{tikzcd}
\end{document}
```
where the last claim is a simple Mayer-Vietoris argument.
The remaining case $0<m = n$ yields something non-trivial:
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
H_n(\mathbb{S}^n) \arrow[r, "\cong"] &H_{n-1}(\mathbb{S}^{m-1}) \arrow[r, "\cong"]& \cdots \arrow[r, "\cong"]& H_1(\mathbb{S}^1) \cong \mathbb{Z},
\end{tikzcd}
\end{document}
```
proving the proposition.<span style="float:right;">$\blacksquare$</span>

**Remark.**
It is possible to prove this using only the [[Mayer-Vietoris sequence]]:
We need to understand the map
$$
\Z \cong H_0(X^+ \cap X^-) \to H_0(X^+) \oplus H_0(X^-) \cong \Z \oplus \Z.
$$
Choose $1$ as base point on the intersection $X^+ \cap X^-.$ The inclusion induces a map on $H_0$ as $[1] \mapsto ([1],[1]).$ This map is clearly injective, making the [[connecting homomorphism]] $\delta: H_1(\S^m) \to H_0(X^+ \cap X^-)$ trivial. Therefore, $H_1(\S^m) \cong \{0\}$ for $m>1.$
Next, we consider $n=1=m.$ The intersection $X^+ \cap X^-$ splits into two connected components. Choose a $p_+ \in X^+$ and a $p_- \in X^-$ such that $p_\pm \in X^+ \cap X^-$ lie in different path components. Then
$$
H_i(\iota_1)([p_+])= [e_2] = H_0(\iota_1)([p_-])
$$
and
$$
H_0(\iota_2)([p_+]) = [-e_2] = H_0(\iota_2)([p_-]).
$$
Hence,
$$
H_0(\iota_1)([p_+],[p_-]) = 0 = H_0 (\iota_2)([p_+], -[p_-]).
$$
This means that $\ker(H_0(\iota_1), H_0(\iota_2)) = \span ([p_+],-[p_-])$ and is therefore isomorphic to $\Z$. The exact sequence
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
\{0\} \arrow[r]& H_1(\mathbb{S}^1) \arrow[r, "\delta"]& H_0(X^+ \cap X^-) \arrow[r, "(H_0(\iota_1){,} H_0(\iota_2))"]&H_0(X^+) \oplus H_0(X^-) \arrow[r]& H_0(\mathbb{S}^1)
\end{tikzcd}
\end{document}
```
finally yields $H_1(\S^1) \cong \Z.$

This discussion produces the following definition:

``` ad-Definition
title: Definition (Fundamental Class).
Define
$$\mu_0 := [p_+] - [p_-] \in H_0(X^+ \cap X^-) \cong H_0(\S^0)$$
and $\mu_1 \in H_1(\S^1) \cong \Z$ by the degree one map (class of identity on $\S^1$ or class of the loop $t \mapsto \exp(2\pi it)$), The higher $\mu_n$ are defined inductively as $D \mu_n = \mu_{n-1}$. Then $\mu_n$ is called <ins>fundamental class</ins> in $H_n(\S^1)$.
```