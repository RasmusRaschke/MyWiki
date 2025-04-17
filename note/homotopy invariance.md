<div class="topSpace"></div>

Date Created: 17/04/25
References: #Ref/AlgTop 
Tags: #Type/Theorem #Topic/AlgebraicTopology 

Proved by: <i>Not Applicable</i>
References: [[chain homotopy]], [[singular simplex]]
Justifications: [[singular simplex#Chain Homotopy Map]]

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Theorem
title: Theorem (Homotopy Invariance).
Let $f,g: X \to Y$ be homotopic maps between [[topological space|topological spaces]]. If they are homotopic, they induce the same map on [[homology]].

```

*Proof.*
Denote the homotopy between $f$ and $g$ by $$H: X \times [0,1] \to Y$$ such that $Hj_0=f$ and $Hj_1=g$. We claim that $(K_n := S_{n+1}(H)P)_{n \in \Z}$ is a [[chain homotopy]] between $(S_n(f))_n$ and $(S_n(g))_n$. Denote the by $H$ induced chain map by $(S_n(H))_n$. This yields:
$$
\begin{align}
\partial S_{n+1}(H)P + S_n(H) P \partial &= S_n(H) \partial P + S_n(H)P \partial = S_n(H) \left( \partial P+ P \partial\right)\\ \\
&= S_n(H) (S_n(j_1)-S_n(j_0)) = S_n(Hj_1) - S_n(Hj_0) = S_n(g)-S_n(f).
\end{align}
$$
Henceforth, the two maps are [[chain homotopy|chain homotopic]], $H_n(g)=H_n(f)$.

<span style="float:right;">$\blacksquare$</span>

``` ad-Proposition
title: Corollary (of Homotopy Invariance).
If $X \simeq Y$, then $H_\ast(X) \cong H_\ast(Y)$. In addition, if $X$ is contractible:
$$
H_\ast (X) \cong
\begin{cases}
Z, \ &\text{for } \ast = 0,\\
0, \ &\text{otherwise.}
\end{cases}
$$

```
**Examples.**
1. $\R^n$ is contractible, so $H_m(\R^n)$ is trivial but for $m=1$.
2. The Möbius strip retracts on its soul $\S^1$: $H_n(M) \cong $H_n(\S^1)$.
3. The zero section of any vector bundle $p: E \to B$ induces a a homotopy equivalence $H_n(E) \cong H_n(B)$.