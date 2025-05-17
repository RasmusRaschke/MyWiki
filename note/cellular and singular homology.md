<div class="topSpace"></div>

Date Created: [[17/05/2025]]
References: #Ref/AlgTop 
Tags: #Type/Theorem #Topic/AlgebraicTopology 

Proved by: <i>Not Applicable</i>
References: [[homology#Cellular Homology]], [[CW complex]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Theorem
title: Theorem (Comparision of Cellular and Singular Homology).
For every [[CW complex]] $X$ exists an [[isomorphism]]
$$
\Upsilon: H_\ast(C_\ast(X),d) \overset{\cong}\to H_\ast(X).
$$
```
*Proof.*
Take a look at this diagram:
![[algtop_cellular_hom.png]]
- Suppose $[c] \in H_n(X^n)$ such that $\rho[c]=[0]$. This implies that $[c]=db+b'$ where $b \in H_n(X^n)$ and $b' \in H_n(X^{n-1})$. The term $db$ vanishes obviously in $H_n(X^n)$ and $H_n(X^{n-1})\cong\{0\}$, so $[c]=[0]$ and all $\rho$ are injective.
- Let $a \in H_n(X^n)$. We have $d\rho[a]=\rho \delta \rho [a] = [0]$, hence $\rho[a]$ is a cycle for $d$.
- For some $d$-cycle $c \in C_n(X)$ we have $0 = dc= \rho \delta [c]$. Injectivity of $\rho$ means that $\delta [c] =0$. Exactness now yields some $a \in H_n(X^n)$ such that $\rho(a)=c$. Hence, $$H_n(X^n) \cong \ker(d:C_n(X) \to C_{n-1}(X)).$$
- With this we define $$\Upsilon: \ker(d) \to H_n(X)$$ as $\Upsilon[c]:= H_n(\iota_n)[a]$ for $[c]=\rho[a]$ and $H_n(\iota_n): H_n(X^n) \to H_n(X).$
- $\Upsilon$ is surjective by [[singular homology of CW complexes#Inclusion Map of Skeleta|this proposition]].
- The triangles above commute: $\delta = \delta' \lambda.$
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
H_{n+1}(X^{n+1}) \ar[r, two heads] & H_{n+1}(X)\ar[r]& H_{n+1}(X, X^{n+1}) \ar[r]& X_n(X^{n+1}) \ar[r, "\cong"]& H_n(X)
\end{tikzcd}
\end{document}
```
- Consider the long sequence above. Since the first map is surjective, the whole of $H_{n+1}(X)$ lies in the kernel of the second surjective map, so $H_{n+1}(X,X^{n+1})\cong \{0\}$. This implies the surjectivity of $\lambda$ by [[relative homology long exact sequence#Triple of Spaces|the homology long sequence for a triple of spaces]].
- This leads to $\im(\delta)=\im(\delta')=\ker(H_n(\iota_n))$. Since $d=\rho \delta$, the map $\rho$ induces an [[isomorphism]] between $\im(d)$ and $\im(\delta)$.
- Together we obtain an [[isomorphism]] induced by $\rho$: $$\frac{\ker(d:C_n(X) \to C_{n-1}(X))}{\im(d:C_{n+1}(X)\to C_n(X))} \cong \frac{H_n(X^n)}{\ker(H_n(\iota_n))}.$$

But the sequence
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
0 \ar[r]& \ker(H_n)(\iota_n)\ar[r]& H_n(X^n) \ar[r]& \text{im}(H_n(\iota_n)) \ar[r] &0
\end{tikzcd}
\end{document}
```
is exact so $$H_n(X^n) / \ker(H_n(\iota_n)) \cong \im(H_n(\iota_n)) \cong H_n(X).$$<span style="float:right;">$\blacksquare$</span>