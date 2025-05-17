<div class="topSpace"></div>

Date Created: [[17/05/2025]]
References: #Ref/AlgTop 
Tags: #Type/Proposition 

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: [[CW complex]], [[homology#Singular Homology]]

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Homology of Skeleta

## Lower Relative Skeletal Homology

``` ad-Proposition
title: Proposition (Homology of Skeleta).
Let $X$ be a [[CW complex]] with skeleta $X^n$. For all $q \neq n \geq 1$ we have
$$
H_q(X^n, X^{n-1}) \cong \{0\}.
$$
```

*Proof.*
We use [[retract#Impact on Homology|the connection between relative homology and reduced homology]] to obtain
$$
H_q(X^n, X^{n-1}) \cong \tilde{H}_q(X^n/X^{n-1}) \cong \bigoplus_\sigma \tilde{H}_q(\S^n)
$$
for $n$-cells $\sigma$. Since $\tilde{H}_{q < n} (\S^n) =0$, the claim follows. <span style="float:right;">$\blacksquare$</span>

## Inclusion Map of Skeleta

``` ad-Proposition
title: Proposition (Inclusion of Skeleta).
Let $X$ be a [[CW complex]] and $\iota_n: X^n \to X$ be the inclusion. 
1. The induced map $H_n(\iota_n): H_n(X^n) \to H_n(X)$ is [[set-function#Injection, Surjection, Bijection|surjective]].
2. There is an [[isomorphism]] $$H_n(\iota_{n+1}): H_n(X^{n+1}) \overset{\cong}\to H_n(X).$$
```

*Proof.*
1. With the inclusions $\alpha_i: X^i \hookrightarrow X^{i+1}$ we can factor $\iota_n$ as 
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
X^n \ar[d, "\alpha_1"'] \ar[rrr, "\iota_n"]& & & X\\
X^{n+1} \ar[r, "\alpha_2"'] \ar[urrr, "\iota_{n+1}"]& X^{n+2} \ar[urr, "\iota_{n+2}"] \ar[r, "\alpha_3"']& X^{n+3}\ar[ur, "\iota_{n+3}"]  \ar[r, "\cdots"']& \cdots
\end{tikzcd}
\end{document}
```
We [[singular homology of CW complexes#Lower Relative Skeletal Homology|already established]] that $H_n(X^{n+1},X^n) =0$, so $H_n(\alpha_1): H_n(X^n) \to H_n(X^{n+1})$ has to be surjective by [[relative homology long exact sequence|the long exact sequence on a pair of spaces]]. For $i>1$, the same sequence applied to the pair $(X^{n+1}, X^{n+i-1})$ yields
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
0 \cong H_{n+1}(X^{n+i}, X^{n+i-1}) \ar[r]& H_n(X^{n+i-1}) \ar[r, "H_n(\alpha_i)"]& H_n(X^{n+i}) \ar[r] & H_n(X^{n+i}, X^{n+i-1}) \cong 0
\end{tikzcd}
\end{document}
```
so $H_n(\alpha_i)$ is an [[isomorphism]]. For finite-dimensional $X$ we are done since in this case $X=X^{\dim X}$ and $\iota_{\dim X}$ is obviously surjective.
By compactness of the [[simplex#Simplex|standard simplices]], every [[singular simplex#Singular Simplices|singular simplex]] in $X$ has an image completely contained in one of the $X^m$. Let $a \in S_n(X)$ with $a=\sum_{i=1}^m \lambda_i \beta_i$ be a chain. Find some $M$ such that the images of all the $\beta_i$ are contained in $X^M$. Wlog let $M=n+q$. Every $[a] \in H_n(X)$ can now be written as $\iota_M[b]$. Because $\alpha_q \cdots \alpha_1$ is surjective, we find some $[c]\in H_n(X^n)$ such that $[b] = (\alpha_q \cdots \alpha_1) [c]$. This yields
$$
[a] = (\iota_M \alpha_q \cdots \alpha_1) [c] = \iota_n[c]
$$
by our diagram above, so $\iota_n$ has to be surjective as well.
2. Since we have already proven that $\iota_{n+1}$ is surjective, only injectivity remains to be shown. Choose some $[u] \in H_n(X^{n+1})$ with $[a]=[0]=H_n(\iota_{n+1})[u]$. By the argument above we find some cycle $b$ on an $M$-skeleton of $X$ for finite $M=n+q+1$. Starting with $X^{n+1}$, we obtain $$(\alpha_q \cdots \alpha_2)[u] = [b].$$ But each $\alpha_i$ is an [[isomorphism]], so $[u]=[0]$.
<span style="float:right;">$\blacksquare$</span>

# Homology of the whole Complex

The propositions above allow us to make some general statements:

``` ad-Proposition
title: Proposition (Singular Homology of CW Complexes).
Let $X,Y$ be [[CW complex|CW complexes]]. We have:
(a) If $X^n \cong Y^n$ as topological spaces, then $H_q(X) \cong H_q(Y)$ for all $q < n$.
(b) If $X$ has no $q$-cells, $H_q(X) \cong \{0\}$.
(c) If $q >  \dim X$ we have $H_q(X) \cong \{0\}$.

```
*Proof.*
(a) follows from [[singular homology of CW complexes#Inclusion Map of Skeleta|from part 2 of the proposition above]].
(b) By assumption, $X^{q-1} = X^q$, so $H_q(X^{q-1})=H_q(X^q)$. Now [[singular homology of CW complexes#Inclusion Map of Skeleta|we know that]] the latter surjects onto $H_q(X)$. Choose $r$ such that $n>r$ and observe that
$$
H_n(X^r) \cong H_n(X^{r-1}) \cong \cdots \cong H_n(X^0)
$$
because the adjacent relative groups $H_n(X^i, X^{i-1})$ are trivial for $i<n$, as demonstrated above. We conclude that $H_n(X^r)\cong \{0\}$.