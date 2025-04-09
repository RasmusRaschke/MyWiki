<div class="topSpace"></div>

Date Created: 09/04/25
References: #Ref/AlgTop 
Tags: #Type/Definition

Proved by: <i>Not Applicable</i>
References: [[chain complex]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Chain Homotopy

``` ad-Definition
title: Definition (Chain Homotopy).

Let $f,g: C_\ast \to D_\ast$ be two [[chain complex#Chain Map|chain maps]]. A <ins>chain homotopy</ins> $H$ between $f$ and $g$ is a family of homomorphisms $(H_n)_{n \in \Z}$ with $$H_n: C_n \to D_{n+1}$$ such that $$\forall n \in \Z: d_{n+1}^D H_n + H_{n-1}d_n^C = f_n - g_n$$. In this case, $f$ and $g$ are <ins>chain homotopic</ins>, denoted $f \simeq g$.

```
This corresponds to the following diagram which is non-commutative:
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath}
\begin{document}
\begin{tikzcd}[scale=3]
\cdots \arrow[r] & C_{n+1} \arrow[dl] \arrow[r, "d_{n+1}^C"] \arrow[d, bend right, "g_{n+1}"']  \arrow[d, bend left, "f_{n+1}"]  & C_n \arrow[r, "d_{n}^C"] \arrow[dl, "H_n"] \arrow[d, bend right, "g_{n}"'] \arrow[d, bend left, "f_{n}"] & C_{n-1} \arrow[r, "d_{n-1}^C"]  \arrow[d, bend right, "g_{n-1}"'] \arrow[dl, "H_{n-1}"] \arrow[d, bend left, "f_{n-1}"]  &\cdots\\
\cdots \arrow[r] & D_{n+1} \arrow[r, "d_{n+1}^D"] & D_n \arrow[r, "d_{n}^D"] & D_{n-1} \arrow[r, "d_{n-1}^D"] & \cdots
\end{tikzcd}
\end{document}
```
 We want to show that this is actually an [[relation#Equivalence Relation|equivalence relation]]:
 1. Reflexivity: $f$ is chain homotopic to itself by choosing $H=0$.
 2. Symmetry: Let $f\simeq g$ with $f_n-g_n = d_{n+1}^D H_n + H_{n-1}d_n^C$. Rearranging leads to $g_n - f_n = - d_{n+1}^D H_n - H_{n-1}d_n^C$, which makes $-H$ a witness for $g \simeq f$.
 3. Transitivity: Let $f \simeq g$ and $g \simeq h$ by $H$ and $G$, respectively. Adding the two given equations results in $$f_n-h_n = d_{n+1}^D H_n + H_{n-1}d_n^C + d_{n+1}^D G_n + G_{n-1}d_n^C= d_{n+1}^D(H_n+G_n) + (H_{n-1}+G_{n-1})d_n^C.$$ We conclude that $f \simeq h$ by $H+G$.

``` ad-Proposition
title: Proposition (Homotopy on induced maps).

Let $f,g$ be chain maps with $f \simeq g$. Then, $$\forall n \in \Z: H_n(f)=H_n(g)$$ holds.

```

*Proof.*
Let $c\in Z_n(C_\ast)$ be an [[chain complex|$n$-cycle]]. Applying the induced maps results in:
$$H_n(f)_\ast [c] - H_n(g)_\ast [c] = [f_nc-g_nc] = [d_{n+1}^D H_n(c)] + [H_{n+1} d_n^C(c)] = 0$$ because cycles are mapped to cycles, so $c \in \ker(d_n^C)$ and $H_n(c) \in \ker(d_{n+1}^D)$.
<span style="float:right;">$\blacksquare$</span>

# Chain Homotopy Equivalence

``` ad-Definition
title: Definition (Chain Homotopy Equivalence).

Let $f: C_\ast \to D_\ast$ be a chain map. $f$ is called <ins>chain homotopy equivalence</ins> if there is a [[chain complex|chain map]] $g: D_\ast \to C_\ast$ such that $gf \simeq \id_{C_\ast}$ and $gf \simeq \id_{D_\ast}$. If this is the case, we call $C_\ast$ and $D_\ast$ <ins>chain homotopy equivalent</ins>.

```
