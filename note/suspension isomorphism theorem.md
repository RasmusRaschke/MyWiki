<div class="topSpace"></div>

Date Created: [[04/05/2025]]
References: #Ref/AlgTop 
Tags: #Type/Theorem 

Proved by: [[excision theorem]]
References: <i>Not Applicable</i>
Justifications: [[cone]], [[suspension]]

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Theorem
title: Theorem (Suspension Isomorphism).

Let $X$ be a [[topological space|topological space]] such that $A \sub X$ is a closed subspace and a [[retract#Deformation Retraction|deformation retract]] of some open neighbourhood $A \sub U \sub X$. Then
$$
H_n(\Sigma X, \Sigma A) \cong \tilde{H}_{n-1}(X,A)
$$
for all $n > 0$.

```
*Proof.*
Consider the pairwise inclusion $(X,A) \sub (CX, CA) \sub (\Sigma X, \Sigma A)$ and the triple $(CX, X \cup CA, CA)$. This induces a [[homology long sequence]]
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
\cdots \ar[r]& H_n(CX,CA) \ar[r]& H_n(CX, CA \cup X) \ar[r, "\delta"]& \widetilde{H}_{n-1}(X \cup CA, CA) \ar[r] & \cdots
\end{tikzcd}
\end{document}
```
[[retract#Impact on Homology|The impact of deformation retracts on homology]] gives
$$
\tilde{H}_n(CX, CA \cup X) \cong \tilde{H}_n(CX / CA \cup X)
$$
and
$$
\tilde{H}_{n-1}(X \cup CA,CA) \cong \tilde{H}_{n-1}((X \cup CA)/CA).
$$
Now $\tilde{H}_{n-1}((X \cup CA)/CA)$ is isomorphic to $\tilde{H}_{n-1}(X/A) \cong \tilde{H}_{n-1}(X,A)$. Similarly, $CX/CA \cup X \simeq \Sigma X / \Sigma A.$ This yields
$$
\tilde{H}_n(CX, CA \cup X) \cong \tilde{H}_n(CX/CA \cup X) \cong \tilde{H}_n(\Sigma X / \Sigma A) \cong H_n(\Sigma X, \Sigma A)
$$
<span style="float:right;">$\blacksquare$</span>