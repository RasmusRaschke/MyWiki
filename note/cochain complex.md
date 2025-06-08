<div class="topSpace"></div>

Date Created: [[08/06/2025]]
References: #Ref/AlgTop 
Tags: #Type/Definition

Proved by: <i>Not Applicable</i>
References: [[chain complex]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Category of Cochain Complexes).
The <ins>category of cochain complexes</ins> $\CoCh$ consists of:
- $\Obj(\CoCh):$ Cochain complexes $(C^\ast, \delta)$.
- $\Hom_{\CoCh}:$ Cochain maps $C^\ast \to C'^\ast$.

```

# Objects

``` ad-Definition
title: Definition (Cochain Complex).
A <ins>cochain complex</ins> of abelian groups is a sequence $(C^n)_{n \in \Z}$ of abelian groups $C^n$ together with homomorphisms $$\delta: C^n \to C^{n+1}$$ with $\delta^2 = 0$, called <ins>coboundary operator</ins>.

```

**Remark.**
There is no need for a separate theory on cochain complexes: If $(C_\ast, d)$ is a [[chain complex]], we define $D^n := C_{-n}$. Then $(D^\ast, d)$ is a cochain complex as $d: C_{-n} = D^n \to C_{-n-1} =D^{n+1}$ turns into a coboundary operator.

# Morphisms

``` ad-Definition
title: Definition (Cochain Map).
Let $(C^\ast, \delta), (\tilde{C}, \tilde{\delta}) \in \Obj(\CoCh)$. A <ins>cochain map</ins>
$$
f^\ast: C^\ast \to \tilde{C}^\ast
$$
is a sequence of homomorphisms 
$$
(f^n: C^n \to \tilde{C}^n)_{n \in \Z}
$$
with $f^{n+1}\delta = \tilde{\delta} f^n$.
```
This corresponds to the following commuting diagram:
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
C^{n+1} \ar[r, "f^{n+1}"] & \tilde{C}^{n+1}\\
C^n \ar[r, "f^n"] \ar[u, "\delta"]& \tilde{C}^n \ar[u, "\tilde{\delta}"].
\end{tikzcd}
\end{document}
```