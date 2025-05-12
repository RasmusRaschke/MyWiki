<div class="topSpace"></div>

Date Created: [[04/05/2025]]
References: #Ref/Topo 
Tags: #Type/Definition

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Of Topological Spaces

``` ad-Definition
title: Definition (Suspension).
Let $X$ be a [[topological space|topological space]]. The <ins>suspension</ins> $\Sigma X$ of $X$ is defined as
$$
\Sigma X:= \big(X \times [-1,1]\big) \big/ \big( (X \times \{-1\}),(X \times \{1\}) \big).
$$

```

We can visualise this construction like this:
```tikz
\usepackage{tikz}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzpicture}[scale=3]
\draw (-1,0) -- (1,0) node[right=2pt] {$X \times \{0\}$};
\draw (0,1) node[above=2pt] {$X \times \{1\}$} -- (1,0);
\draw (0,1) -- (-1,0);
\draw (0,-1) -- (-1,0);
\draw (0,-1) node[below=2pt] {$X \times \{-1\}$} -- (1,0);
\end{tikzpicture}
\end{document}
```

## Degree Invariance

If we have a continuous map $f: \S^n \to \S^n$ we can use the fact that $\Sigma \S^n \cong \S^{n+1}$ to lift the map to the suspension by 
$$
\begin{align}
\Sigma(f): \Sigma \S^n &\to \Sigma \S^n \\
[x,t] &\mapsto [f(x),t].
\end{align}
$$

``` ad-Proposition
title: Proposition (Degree Invariance of Suspension).
The [[mapping degree#Mapping Degree in Algebraic Topology|mapping degree]] is invariant under suspensions:
$$
\deg(\Sigma(f))=\deg(f)
$$
for any continuous $f: \S^n \to \S^n$.
Particulary, for every $k \in \Z$ exists a map $f: \S^n \to \S^n$ with $\deg(f)=k$.
```
*Proof.*
The [[suspension isomorphism theorem]] provides an [[isomorphism]] $H_{n+1}(\S^{n+1})\cong H_{n+1}(\Sigma \S^n)$ via the [[connecting homomorphism]] $\delta$. This isomorphism hence sends $\mu_{n+1} \in H_{n+1}(\S^{n+1})$ to $\pm \mu_n \in \tilde{H}_n(\S^n)$. The identical sign is guaranteed by the following commutative diagram:
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
\mu_{n+1} \in H_{n+1}(\mathbb{S}^{n+1}) \ar[r,"\cong"]& H_{n+1}(\Sigma \mathbb{S}^n) \ar[r, "H_{n+1}(\Sigma f)"] \ar[d,"\delta"]& H_{n+1}(\Sigma \mathbb{S}^n) \ar[d, "\delta"] &\text{deg}(\Sigma f)\mu_{n+1} \in H_{n+1}(\mathbb{S}^{n+1}) \ar[l, "\cong"']\\
&\mu_n \in \widetilde{H}_n(\mathbb{S}^n) \ar[r,"H_n(f)"] & \pm \text{deg}(f) \mu_n \in \widetilde{H}_n(\mathbb{S}^n) \ni \pm \deg(\Sigma f)\mu_n&
\end{tikzcd}
\end{document}
```
which yields $$\pm \deg(f)\mu_n = \pm \deg(\Sigma f)\mu_n$$ with the same sign.
<span style="float:right;">$\blacksquare$</span>