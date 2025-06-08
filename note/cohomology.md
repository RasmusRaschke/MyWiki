<div class="topSpace"></div>

Date Created: [[08/06/2025]]
References: #Ref/AlgTop 
Tags: #Type/Definition #Topic/AlgebraicTopology 

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: [[cochain complex]]

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Of Abelian Groups

``` ad-Definition
title: Definition (Cohomology Group).
Let $C^\ast$ be a [[cochain complex]]. The <ins>$n$-th cohomology group</ins> of $C^\ast$ is given by
$$
H^n(C^\ast) := \frac{\ker(\delta: C^n \to C^{n+1})}{\im(\delta: C^{n-1}\to C^n)}.
$$

```

# Singular Cohomology

``` ad-Definition
title: Definition (Singular Cochain Group).
Let $X$ be a [[topological space]]. The <ins>n-th singular cochain group</ins> of $X$ is given by
$$
S^n(X):=\Hom(S_n(X), \Z)
$$
with coboundary operator $\delta = \Hom(\partial, \Z)$.
```

**Example.**
For $\alpha: \Delta^{n+1} \to X$ and $\phi: S_n(X) \to \Z$, we have $$\delta(\phi)(\alpha)=\phi(\partial \alpha)$$ as 
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
S_n(X) \ar[r, "\varphi"] & \mathbb{Z} \\
S_{n+1}(X) \ar[u, "\partial"] \ar[ur, "\delta (\varphi)"'] & 
\end{tikzcd}
\end{document}
```
Now let $\beta: \Delta^{n+2} \to X$. The composition is given by 
$$
\delta^2 (\phi) (\beta) = \delta(\phi)(\partial \beta) = \phi(\partial^2 \beta) = 0.
$$
 [[coefficient homology|Analogously,]] we define:
 
 ``` ad-Definition
title: Definition (Cohomology with Coefficients).
Let $G$ be an abelian group and $X$ be a [[topological space]]. The <ins>$n$-th cochain group with coefficients</ins> in $G$ is given by
$$
S^n(X;G):= \Hom(S_n(X),G).
$$
The <ins>$n$-th cohomology group with coefficients</ins> in $G$ is defined as
$$
H^n(X;G):=\frac{\ker(\delta: S^n(X;G) \to S^{n+1}(X;G))}{\im(\delta: S^{n-1}(X;G) \to S^n(X;G))}.
$$
```


# Functorial Properties

``` ad-Proposition
title: Proposition (Cohomology Functor).
For an abelian group $G$, the maps
$$
S^n(\cdot; G): \Top \to \mathtt{AGrp}
$$
and
$$
H^n(\cdot; G): \Top \to \mathtt{AGrp}
$$
are [[functor#Contravariant Functors|contravariant functors]] from the [[category]] of [[topological space|topological spaces and continuous maps]] to the category of abelian groups and group homomorphisms.
```

This means that every map $f: X \to Y$ between topological spaces induces a map 
$$
S^\ast(f)=f^\ast: S^\ast(Y;G) \to S^\ast(X;G).
$$
For $\phi \in S^\ast(Y;G)$ and $\alpha \in S_\ast(X)$, we have
$$
f^\ast(\phi)(\alpha) = \phi(f_\ast \alpha) \in G.
$$