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

## Of $\R P^2$

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

## Of general Projective Spaces
Let $K \in \{\R, \C,\H\}$ with $m:= \dim_\R(K)$ and $\K^\ast = K \setminus \{0\}$. We define an action of $K^\ast$ on $K^{n+1}$ via
$$
\begin{align}
K^\ast \times K^{n+1} \setminus \{0\} &\to K^{n+1} \setminus \{0\} \\
(\lambda, v) &\mapsto  \lambda \cdot v.
\end{align}
$$
Denote the $n$-th projective space by $KP^n = (K^{n-1}\setminus \{0\}) /K^\ast$ as orbit space with equivalence classes of some $(x_0,\dots,x_n)$ given by $[x_0:\cdots :x_n].$
Now we define
$$
X_i := \{[x_0: \cdots: x_n]\mid x_i \neq 0, x_{i+1}=\cdots = x_n=0\}
$$
and a map
$$
\begin{align}
\xi_i: X_i &\to K^i \\
[x_0: \cdots : x_n] &\mapsto \xi_i[x_0: \cdots:x_n]:= \left(\frac{x_0}{x_i}, \cdots, \frac{x_{i-1}}{x_i} \right).
\end{align}
$$
This map is a homeomorphism, so $X_i$ is a cell of dimension $i\cdot m$. We write $KP^n = \coprod_{i=0}^n X_i$ and obtain characteristic maps
$$
\Phi_i(y)=\Phi_i(y_0, \dots, y_{i-1})=[y_0: \cdots y_{i-1}:1-\|y\|:0:\cdots:0]
$$
with $X_i = \Phi_i(\mathring{\D}^{mi}).$
1. $K=\C$: We have a cell in each even dimension for $\C P^n$. The [[homology#Cellular Homology|cellular chain complex]] is $$ C_k(\C P^n) = \begin{cases} \Z \ &k=2i, 0 \leq i \leq n,\\ 0 \ &k=2i-1 \, \text{or} \, k>2n.\end{cases}$$ Since the boundary operator is $0$ in each degree we get $$ H_k(\C P^n) = \begin{cases} \Z \ &k=2i, 0 \leq i \leq 2n,\\ 0 \ &\text{else}.\end{cases}$$ 
2. $K=\H$: Now the cells are spread out in degrees mod $4$, thus $$ H_k(\H P^n) = \begin{cases} \Z \ &k=4i, 0 \leq i \leq 4n,\\ 0 \ &\text{else}.\end{cases}$$ 
3. $K=\R$: Here we have to look out for non-trivial boundary operators. We have a cell in each dimension up to $n$, so the homology of $\R P^n$ is the homology of the chain complex
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
0 \ar[r]& C_n \cong \mathbb{Z} \ar[r, "d"]& C_{n-1}\cong \mathbb{Z} \ar[r, "d"]& \cdots \ar[r, "d"]& C_0 \cong \mathbb{Z}.
\end{tikzcd}
\end{document}
```
To compute $d$, we take a look at this diagram:
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\newcommand{\R}{\mathbb{R}}
\renewcommand{\S}{\mathbb{S}}
\begin{document}
\begin{tikzcd}[scale=3]
H_i(\R P^i, \R P^{i-1}) \cong H_i(\R P^i / \R P^{i-1}) \ar[d, "\delta"] \ar[dd, bend right=70, "d"'] & H_i(\S^i) \ar[l, "\cong"'] \ar[d, "\cong"', "\delta"]\\
H_i(\R P^{i-1})\ar[d, "H_{i-1}(\pi)"]& \widetilde{H}_{i-1}(\S^{i-1}) \ar[l, "\phi_i"]\\
H_{i-1}(\R P^{i-1}, \R P^{i-2})
\end{tikzcd}
\end{document}
```
with $\phi_i := \Phi_i|_{\S^{i-1}}: \S^{i-1} \to \S^{i-1}/\pm \id.$ The preimage of $[x] \in \S^{i-1} / \pm \id$ is $\{\pm x\}$.