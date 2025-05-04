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

# General Mayer-Vietoris Sequence

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

## Reduced Mayer-Vietoris Sequence

``` ad-Proposition
title: Proposition (Reduced Mayer-Vietoris Sequence).
Consider the same situation as above. There is a [[long exact sequence]]
$$
\cdots \overset{\delta}\longrightarrow \tilde{H}_n(X_1 \cap X_2) \longrightarrow \tilde{H}_n(X_1) \oplus \tilde{H}_n(X_2) \longrightarrow \tilde{H}_n(X)\overset{\delta}\longrightarrow \tilde{H}_{n-1}(X_1 \cap X_2) \overset{\tilde{H}_{n-1}(f_\ast)}\longrightarrow \cdots.
$$
```

# Relative Mayer-Vietoris Sequence

We also want to consider the relative situation where we have a triple of [[topological space|topological spaces]] $(X,A,B)$ with $A,B \sub X$ open in $A \cup B$. We choose the open cover $\fU := \{A,B\}$ of $A \cup B.$ This leads to a diagram of [[short exact sequence|exact sequences]] as follows:
![[algtop_rel_mvs.png]]
The map $\Delta: S_n(X) \to S_n(X) \oplus S_n(X)$ is the diagonal map while $\text{diff}: S_n(X) \to S_n(X) \to S_n(X)$ is the difference map. Obviously, $\im(\Delta)=\ker(\text{diff})$, so the second row is exact. The map $\psi$ is induced by the inclusion $\phi: S_n^\fU (A \cup B) \to S_n(A\cup B).$ By the [[nine-lemma]], the third row is also exact.
We focus on the two right-most non-trivial columns in this diagram. These give rise to [[homology long sequence|homology long sequences]]
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
H_n(S_\ast^\mathfrak{U} (A \cup B)) \arrow[r] \arrow[d, "H_n(\phi)"] & H_n(X) \arrow[r] \arrow[d, equal]&H_n(S_\ast(X)/S_\ast^\mathfrak{U}(A \cup B)) \arrow[r, "\delta"] \arrow[d, "H_n(\psi)"]& H_{n-1}(S_\ast^\mathfrak{U}(A \cup B)) \arrow[r] \arrow[d, "H_{n-1}(\phi)"]& H_{n-1}(X) \arrow[d, equal]\\
H_n(A \cup B) \arrow[r]& H_n(X) \arrow[r] & H_n(X, A \cup B) \ar[r, "\delta"] & H_{n-1}(A \cup B)\arrow[r] & H_{n-1}(X)
\end{tikzcd}
\end{document}
```
Observing that $H_n(\phi)$ and $H_{n-1}(\phi)$ are [[isomorphism|isomorphisms]], we can deduce that $H_n(\psi)$ also has to be a [[isomorphism]] by the [[five lemma]]. This justifies the relative Mayer-Vietoris Sequence

``` ad-Theorem
title: Theorem (Relative Mayer-Vietoris Sequence).
Let $(X,A,B)$ be a triple of [[topological space|topological spaces]] such that $A,B \sub X$ are open in $A \cup B$. Then the following sequence is [[long exact sequence|exact]]:
$$
\cdots \overset{\delta}\longrightarrow H_n(X, A \cap B) \longrightarrow H_n(X,A) \oplus H_n(X, B) \longrightarrow H_n(X, A \cup B)\overset{\delta}\longrightarrow \cdots.
$$

```
<span style="float:right;">$\blacksquare$</span>
