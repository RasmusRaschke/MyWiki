<div class="topSpace"></div>

Date Created: 11/04/25
References: #Ref/LeeSmooth
Tags: #Type/Definition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[topological space]]
Examples: <i>Not Applicable</i>

# Topological Manifold

``` ad-Definition
title: Definition (Topological Manifold).

Let $M$ be a [[topological space]]. $M$ is called <ins>topological $n$-manifold</ins> if the following conditions are satisfied:
1. $M$ is Hausdorff.
2. $M$ is second-countable.
3. $M$ is <ins>locally Euclidean</ins> of dimension $n$: For every $p \in M$ there is an open neighbourhood $U \sub M$ of $p$, an open subset $\widetilde{U} \sub \R^n$ and a homeomorphism $\phi: U \to \widetilde{U}$.
The dimension of $M$ is abbreviated $\dim M \in \N$ or $M^n$.
```

## Coordinate Chart

``` ad-Definition
title: Definition (Coordinate Chart).

Let $M$ be a manifold of dimension $n$.
```

```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
A \arrow[dr, left, "g \circ f"'] \arrow[r, "f"] & B \arrow[d, "g"]\\
& C
\end{tikzcd}
\end{document}
```

<span style="float:right;">$\blacksquare$</span>