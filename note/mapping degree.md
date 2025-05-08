<div class="topSpace"></div>

Date Created: [[08/05/2025]]
References: #Ref/AlgTop #Ref/LeeSmooth 
Tags: #Type/Definition #Topic/AlgebraicTopology #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: [[fundamental class]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Mapping Degree in Algebraic Topology

``` ad-Definition
title: Definition (Mapping Degree).
Let $f: \S^n \to \S^n$ be a continuous map and $\mu_n \in \tilde{H}_n(\S^n)$ be the $n$-th [[fundamental class|fundamental class]]. This map induces a homomorphism 
$$
\tilde{H}_n(f): \tilde{H}_n(\S^n) \to \tilde{H}_n(\S^n)
$$
with 
$$
\tilde{H}_n(f)\mu_n = \deg(f)\mu_n
$$
for $\deg(f) \in \Z$. We call $\deg(f)$ the <ins>(mapping) degree</ins> of $f$. 
```

**Example.**
For $n=1$, we obtain the usual definition of degree for $\pi_1(\S^1,1).$ The generator of the fundamental group can be represented by the loop
$$
\begin{align}
\gamma: [0,1] &\to \S^1 \\ \\
t &\mapsto \exp(2\pi it).
\end{align}
$$
With the [[hurewicz theorem]], we have an [[isomorphism]] $h_\text{ab}: \pi_1(\S^1 ,1) \to H_1(\S^1)$ with $h_\text{ab}[\gamma]=\mu_1$. The naturality square
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
\pi_1(\mathbb{S}^1, 1) \ar[r, "\pi_1(f)"] \ar[d, "h_\text{ab}"]& \pi_1(\mathbb{S}^1, 1) \ar[d, "h_\text{ab}"] \\
H_1(\mathbb{S}^1) \ar[r, "H_1(f)"] & H_1(\mathbb{S}^1)
\end{tikzcd}
\end{document}
```
yields
$$
\deg(f)\mu_1=H_1(f)\mu_1 = h_\text{ab}\pi_1(f)[\gamma] = h_\text{ab}\deg_1(f)(\gamma) = \deg_1(f) \mu_1
$$
where $\deg_1$ is the usual degree defined on $\pi_1$.

## Extension to general Functions

Since the [[connecting homomorphism]] induces an isomorphism $H_n(\D^n, \S^{n-1}) \cong \tilde{H}_{n-1}(\S^{n-1})$, we can define the degree of any map
$$
f: (\D^n, \S^{n-1}) \to (\D^n, \S^{n-1})
$$
by $\tilde{\mu}_n:=\delta^{-1}\mu_n,$ guaranteeing $\deg(f) \in \Z.$

## General Properties

``` ad-Proposition
title: Proposition (Properties of the Mapping Degree).
1. $f \simeq g \iff \deg(f)=\deg(g)$
2. $\deg(\id_{\S^1})=1$
3. $\deg(gf)=\deg(g)\deg(f)$
4. If $f$ is not surjective, $\deg(f)=0$.

```
*Proof.*
