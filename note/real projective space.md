<div class="topSpace"></div>

Date Created: [[04/05/2025]]
References: #Ref/AlgTop f
Tags: #Type/Definition #Type/Proposition #Topic/Topology 

Proved by: [[Mayer-Vietoris sequence#Relative Mayer-Vietoris Sequence]]
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Definition

# Homology

Consider $\R P^2$ as quotient $\R P^2 \cong \D^2/(z \sim -z)$ for $z \in \S^1.$ Setting $X=\R P^2$, $X_1 :=X \setminus \{[0,0]\}$ and $X_2:=\mathring{\D}^2$ yields
$$
X_1 \cap X_2 = \mathring{D}^2 \setminus\{[0,0]\} \simeq \S^1.
$$
Note that $X_1$ is an open Möbius strip, homotopically equivalent to its soul $\S^1.$ This yields $H_1(X_1)\cong \Z,$ $H_1(X_2) \cong \{0\}$ and $H_2(X_1)=H_2(X_2)=\{0\}$. Choose generators for $H_1(X)$ and $H_1(X_1 \cap X_2)$ in the following way: Let $\omega$ be a path running halfway around the outer circle in mathematically positive direction starting at $(1,0)$. Let $\gamma$ be a loop running around the inner circle in positive direction. The inclusion $\iota: X_1 \cap X_2 \hookrightarrow X_1$ induces $H_1(\iota)[\gamma]=2[\omega].$ The [[Mayer-Vietoris sequence]] reads as
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\let\tilde\widetilde
\begin{document}
\begin{tikzcd}[scale=3]
\{0\}\cong \tilde{H}_2(X_1) \oplus \tilde{H}_2(X_2) \ar[r]& \tilde{H}_2(X) \ar[r]& \tilde{H}_1(X_1 \cap X_2) \cong \mathbb{Z} \ar[r]& \tilde{H}_1(X_1) \cong \mathbb{Z} \ar[r]& \tilde{H}_1(X) \ar[r]& \tilde{H}_0(X_1 \cap X_2) \cong \{0\}
\end{tikzcd}
\end{document}
```
therefore it is not necessary to consider homology groups of degree $\geq 3$. The map on the two copies of $\Z$ are given as above, so we have $\cdot 2: \Z \to \Z$. This yields
$$
H_2(\R P^2) \cong \ker(\cdot 2: \Z \to \Z) = \{0\},
$$
$$
H_1(\R P^2) \cong \coker(\cdot 2: \Z \to \Z) \cong \Z /2\Z
$$
and
$$
H_0(\R P^2) \cong \Z.
$$