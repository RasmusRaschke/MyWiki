<div class="topSpace"></div>

Date Created: 09/04/2025
References: #Ref/AlgTop
Tags: #Type/Definition

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Chain Complexes

``` ad-Definition
title: Definition (Chain Complex).

A <ins>chain complex</ins> is a sequence $(C_n)_{n \in \Z}$ of [[group|abelian groups]] $C_n$ with [[category|homomorphisms]] $$d_n: C_n \to C_{n-1}$$ for every $n \in \Z$, called <ins>differentials</ins> or <ins>boundary operators</ins>, such that $d_{n-1}d_n=0$. Chain complexes are denoted $C_\ast$ for short.
```

```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
\cdots \arrow[r] & C_{n+1} \arrow[r, "d_{n+1}"] & C_n \arrow[r,"d_n"] & C_{n-1} \arrow[r]& \cdots
\end{tikzcd}
\end{document}
```
**Remark.**
One can also define chain complexes with $R$-modules $C_n$ and $R$-linear boundary operators $d_n$.

``` ad-Definition
title: Definition (Boundary and Cycles).

We call $x \in C_n$ an <ins>$n$-chain</ins>. An $n$-chain $x$ is called <ins>$n$-cycle</ins> if $d_nx=0$. The set of $n$-cycles
$$Z_n(C):= \ker(d_n) = \{x \in C_n \mid d_nx=0\}  \leq C_n$$
consitutes a [[group#subgroup|subgroup]].
If an $n$-chain $x \in C_n$ satisfies $x=d_{n+1}y$ for some $y\in C_{n+1}$, we call $x$ an <ins>$n$-boundary</ins>. The set of $n$-boundaries
$$B_n(C):= \im(d_{n+1})=\{d_{n+1}y\mid y \in C_{n+1}\} \leq C_n$$
is again a [[group#subgroup|subgroup]].
```

*Proof.*
Since $B_n(C)$ is always the image of a [[category|homomorphism]]. [[image is subgroup|it has to be a subgroup]]. Analogously, $Z_n(C)$ is the kernel of a homomorphism and therefore also a subgroup. <span style="float:right;">$\blacksquare$</span>

**Remark.**
Since $d_{n+1}d_n=0$, we know that $\im(d_{n+1}) \leq \ker(d_n)$ and therefore also $B_n(C) \sub Z_n(C)$.

# Chain Map

``` ad-Definition
title: Definition (Chain Maps).

Let $C_\ast, D_\ast$ be chain complexes. A <ins>chain map</ins> $f:C_\ast \to D_\ast$ is a family of homomorphisms $(f_n: C_n \to D_n)_{n \in \Z}$ such that $d_n^D f_n = f_{n-1}d_n^C$ for all $n$.
```
This is equivalent to the commuting diagrams
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
\cdots \arrow[r] &C_n \arrow[r,"d_n"] \arrow[d, "f_n"] & C_{n-1} \arrow[r] \arrow[d, "f_{n-1}"] & \cdots\\
\cdots \arrow[r] &D_n \arrow[r,"d_n"] & D_{n-1} \arrow[r]& \cdots
\end{tikzcd}
\end{document}
```
for all $n \in \Z$. Since such chain maps send cycles to cycles and boundaries to boundaries, a map $$\begin{split}H_n(f)_\ast:H_n(C) &\to H_n(D)\\ [c] &\mapsto H_n(f)_\ast[c] = [f_nc]\end{split}$$ between [[homology|homology groups]] is induced.

**Examples.**
Consider the examples from [[homology]]:
1. There is a chain map
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
\cdots \arrow[r] & 0 \arrow[r, "0"] \arrow[d, "0"] & Z \arrow[r,"\cdot n"] \arrow[d, "0"] & Z \arrow[r] \arrow[d, "\pi"]& 0 \arrow[r, "0"] \arrow[d, "0"] &\cdots\\
\cdots \arrow[r] & 0 \arrow[r, "0"] & 0 \arrow[r,"0"] & Z/nZ  \arrow[r]&0 \arrow[r, "0"] & \cdots
\end{tikzcd}
\end{document}
```
where $H_0(f)_\ast: \Z /n\Z \to \Z/n\Z$ is an [[isomorphism]].
2. There is a chain map between example 2 and 3 given by $$f_n  = \begin{cases} \id_\Z \, &\text{if}\, n \, \text{is odd}\\ 0 \, &\text{otherwise.}\end{cases}$$:
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath}
\begin{document}
\begin{tikzcd}[scale=3]
\cdots \arrow[r] & Z \arrow[r, "id_Z"] \arrow[d, "id_Z"] & Z \arrow[r,"0"] \arrow[d, "0"] & Z \arrow[r, "id_Z"] \arrow[d, "id_Z"] & Z \arrow[r, "0"] \arrow[d, "0"] &\cdots\\
\cdots \arrow[r] & Z \arrow[r, "0"] & Z \arrow[r,"0"] & Z \arrow[r, "0"] & Z \arrow[r, "0"] &\cdots
\end{tikzcd}
\end{document}
```
A simpler one is just given by $f_n=0$ for all $n$.

**Remark.**
The induced maps are compatible with composition of chain maps. If $f, g: C_\ast \to D_\ast$ are two chain maps, $$H_n(g)_\ast H_n(f)_\ast = H_n(gf)_\ast.$$ always holds.

# Direct Sum

``` ad-Definition
title: Definition (Direct Sum of Chain Complexes).

Let $C_\ast$ and $C_\ast'$ be chain complexes. Their <ins>direct sum</ins> $C_\ast \oplus C_\ast'$ is the chain complex with $$(C_\ast \oplus \C_\ast')_n = C_n \oplus C_n' = C_n \times C_n'$$ and the differential $$d_\oplus (c,c') = (dc,dc').$$
For an arbitrary family of chain complexes $(C_\ast^{(j)}, d^{(j)})_{j \in J}$, we define the direct sum as $$\left( \bigoplus_{j \in J} C_\ast^{(j)} \right)_n := \bigoplus_{j \in J} C^{(j)}$$ such that the differential $d_\oplus$ satisfies the universal property $d_\oplus |_{C_n^{(j)}} = d^{(j)}$.
```

# Category

``` ad-Definition
title: Definition (Category of Chain Complexes).

Let $(C_n)_{n \in \Z}$ be a family of abelian groups. The category $\Ch$ of chain complexes is defined as follows:
1. $\Obj(\Ch):$ Chain complexes $C_\ast$ of $(C_n)_{n \in \Z}$.
2. $\Hom_{\Ch}:$ Chain maps between those chain complexes.
```