<div class="topSpace"></div>

Date Created: [[14/05/2025]]
References: #Ref/AlgTop 
Tags: #Type/Proposition #Topic/AlgebraicTopology 

Proved by: <i>Not Applicable</i>
References: [[product]] [[CW complex]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Proposition
title: Proposition (Products of CW Complexes).

Let $X,Y$ be [[CW complex|CW complexes]]. The [[product]] $X \times Y$ is a CW complex if $X$ or $Y$ is locally compact.
```

*Proof.*
Products of cells are cells, hence the [[cell decomposition]] of $X \times Y$ is inherited from $X$ and $Y$. The point in question is the weak topology, for which we prove a more general, auxiliary fact: 
Let $X,Y,Z$ be [[topological space|topological spaces]] which are Hausdorff. If $Z$ is locally compact and $\pi: X \to Y$ endows $Y$ with the quotient topology, then 
$$
\pi \times \id: X \times Z \to Y \times Z
$$
endows $Y \times Z$ with the quotient topology. We need to show that $Y \times Z$ has the universal property of a quotient space:
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
X \times Z \ar[r, "\pi \times \text{id}"] \ar[dr, "g(\pi \times \text{id})"'] & Y \times Z \ar[d, "g"]\\
& W
\end{tikzcd}
\end{document}
```
Consider the space $\cC(X \times Z, W)$ of continuous maps $X \times Z \to W$ endowed with the compact-open topology. Since $Z$ is locally compact, there is a homeomorphism
$$
\cC(X \times Z, W) \cong \cC(X, \cC(Z,W)).
$$
Now assume that $g: Y \times Z \to W$ is a [[set-function]] such that $g (\pi \times \id)$ is continuous. Under our assumption $g$ corresponds to 
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
\tilde{g}: X \ar[r, "\pi"]& Y \ar[r, "\overline{g}"] & \mathcal{C}(Z,W)
\end{tikzcd}
\end{document}
```
We know that $\tilde{g}$ and $\pi$ are continuous and $Y$ has the universal property of the quotient, hence $\overline{g}$ is continuous. Since $\overline{g}$ corresponds to $g$, $g$ is also continuous. This proves the auxiliary fact.
Now we turn to the characteristic maps
$$
\Phi_\sigma: \mathring{\D}^n \to X
$$
and
$$
\Psi_\tau: \mathring{\D}^m \to Y
$$
for cells $\sigma \sub X$ and $\tau \sub Y$. With this we can write the product as
$$
\Phi \times \Psi: \coprod_{\sigma} \mathring{\D}^n \times \coprod_\tau \mathring{\D}^m \to X \times Y.
$$
Wlog let $Y$ be locally compact. Our goal is to show that $X \times Y$ has the quotient topology with respect to $\Phi \times \Psi$. We need to apply our lemma two times: 
1. Each $\mathring{\D}^n$ is locally compact, so the disjoint union is too. The map
$$
\id_{\coprod \mathring{\D}^n} \times \Psi
$$
endows $\coprod \mathring{\D}^n \times Y$ with the quotient topology. 
2. Since $Y$ is locally compact, we can conclude that $\Phi \times \id_Y$ endows $X \times Y$ with the quotient topology.

Combining those two statements yields a map $(\Phi \times \id_Y)(\id_{\coprod \mathring{\D}^n} \times \Psi) = \Phi \times \Psi$, proving the claim. <span style="float:right;">$\blacksquare$</span>