<div class="topSpace"></div>

Date Created: 14/04/25
References: #Ref/AlgTop  
Tags: #Type/Theorem  #Topic/AlgebraicTopology 

Proved by: [[first homology group]]
References: [[homology#Singular Homology]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Definition

``` ad-Definition
title: Definition (Hurewicz Homomorphism).
The map $$h: \pi_1 (X,x) \to H_1(X)$$ that sends homotopy classes $[\omega]_{\pi_1}$ of closed paths $\omega$ to homology classes $[\omega]= [\omega]_{H_1}$ is called <ins>Hurewicz homomorphism</ins>.

```

The well-definedness of this map is given by our considerations of paths and homology in [[first homology group]]. This also yields
$$
h([\omega_1][\omega_2])=h([\omega_1 \ast \omega_2]) = [\omega_1] + [\omega_2] = h([\omega_1]) + h([\omega_2]).
$$
For closed paths, $[\overline{\omega}] = -[\omega]$ holds in $H_1(X)$.

# Theorem

``` ad-Theorem
title: Theorem (of Hurewicz).
The Hurewicz homomorphism factors through the [[abelian group#Abelianization|abelianization]] of $\pi_1(X,x)$, inducing an [[isomorphism]]
$$
\pi_1(X,x)_\text{ab} \cong H_1(X)
$$
for all path-connected $X$.
```


```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext}
\begin{document}
\begin{tikzcd}[scale=3]
\pi_1(X,x) \arrow[d, "p"'] \arrow[r, "h"] & H_1(X) \\
 \pi_1(X,x)_\text{ab} \arrow[ur, "h_\text{ab}"', "\cong"] &
\end{tikzcd}
\end{document}
```

*Proof.*
We construct an explicit inverse. Multiplication in $\pi_1$ will be denoted multiplicatively. For $y \in X$ we choose a path $u_y$ from $x$ to $y$. If $x=y$, we choose the constant path $c_x$. For an arbitrary $1$-[[singular simplex|simplex]] $\alpha: \Delta^1 \to X$ we set $y_i := \alpha (e_i)$. Now, we propose that the inverse is given by
$$
\phi: S_1(X) \to \pi_1(X,x)_\text{ab},
$$
defined on generators as
$$
\alpha \mapsto \phi(\alpha):= [u_{y_0} \ast \alpha \ast \overline{u}_{y_1}].
$$
We need to show that this map vanishes on boundaries. Let $\beta: \Delta^2  \to X$, then:
$$
\phi(\partial \beta) = \phi (\beta d_0 - \beta d_1 + \beta d_2) = \phi(\beta d_0) \phi(\beta d_1)^{-1} \phi(\beta d_2).
$$
Abbreviating $\alpha_i := \beta d_i$ and using that the image of $\phi$ is [[abelian group|abelian]], we obtain:
$$
\begin{align}
[u_{y_1} \ast \alpha_0 \ast \overline{u}_{y_2}][u_{y_0} \ast \alpha_1 \ast \overline{u}_{y_2}]^{-1} [u_{y_0} \ast \alpha_2 \ast \overline{u}_{y_1}] &= [u_{y_0} \ast \alpha_2 \ast \overline{u}_{y_1} \ast u_{y_1} \ast \alpha_0 \ast \overline{u}_{y_2} \ast u_{y_2} \ast \overline{\alpha_1} \ast \overline{u}_{y_0}]\\ \\
&= [u_{y_0} \ast \alpha_2 \ast \alpha_0 \ast\overline{\alpha_1} \ast \overline{u}_{y_0}].
\end{align}
$$
The path $\alpha_2 \ast \alpha_0 \ast \overline{\alpha_1}$ traces the boundary of $\beta$ and is therefore [[chain homotopy|null-homotopic]]. This gives $\phi(\partial \beta) =0,$ $\phi$ is well-defined.
Let $\omega$ be a closed path in $X$. We calculate 
$$
\phi h_\text{ab}[\omega]_\pi = \phi [\omega]_H = [u_x \ast \omega \ast \overline{u}_x]_\pi = [c_x \ast \omega \ast c_x] = [x]
$$
and obtain $\phi h_\text{ab}=\id_\pi$. Now, let $c=\sum \lambda_i \alpha_i$ be a [[chain complex|cycle]].  The expression $h_\text{ab} \phi(c)$ is of form $[c + D_{\partial c}] where $D_{\partial c}$ denotes the contribution of the $u_{y_i}$. However, $\partial c = 0$ implies that the summands in $D_{\partial c}$ cancel off, giving $h_\text{ab} \phi = \id_H$.
<span style="float:right;">$\blacksquare$</span>

**Examples.**
This [[isomorphism]] gives us a multitude of [[first homology group|first homology groups]] for spaces with known fundamental group:
- $H_1(\S^n) = \{0\}$ for all $n > 1$
- $H_1(\S^1) \cong \Z$
- $H_1(\T^n) \cong \Z^n$
- $H_1(\S^1 \vee \S^1) \cong (\Z \ast \Z)_\text{ab} \cong \Z \oplus \Z$
- $H_1(\R P^n) \cong \begin{cases} \Z, \ &n=1\\ \Z/2\Z, \ &n>1\end{cases}$
- $H_1(F_g) \cong \Z^{2g}$ for $g\geq 1$
- $H_1(K) \cong \Z \oplus \Z/2\Z$