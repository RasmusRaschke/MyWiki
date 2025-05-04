<div class="topSpace"></div>

Date Created: [[04/05/2025]]
References: #Ref/Topo 
Tags: #Type/Definition #Type/Proposition #Topic/Topology 

Proved by: [[Mayer-Vietoris sequence#Reduced Mayer-Vietoris Sequence]]
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Definition

# Homology

``` ad-Proposition
title: Proposition (Homology of Bouquets of Spaces).
Let $(X_i)_{i\in I}$ be a family of [[topological space|topological spaces]] with chosen basepoints $x_i \in X_i$ and denote the bouquet by 
$$
X = \bigvee_{i \in I} X_i.
$$
If there are open neighbourhoods $U_i$ of $x_i \in X_i$ together with a deformation $U_i \to \{x_i\}$, we have
$$
\tilde{H}_n (X) \cong \bigoplus_{i \in I} \tilde{H}_n(X_i).
$$
In this case, the $x_i$ are called <ins>well-pointed</ins> with respect to $X_i$.
```
*Proof.*
We start by proving the finite case: Let $E \sub I$ be a finite subset. We want to show that
$$
\tilde{H}_n \left( \bigvee_{i \in E} X_i\right) \cong \bigoplus_{i \in E} \tilde{H}_n(X_i).
$$
Consider $X=X_1 \vee X_2.$ We have $\fU:=\{X_1 \vee U_2, U_1 \vee X_2\}$ as open covering of $X_1 \vee X_2.$ With [[Mayer-Vietoris sequence|Mayer-Vietoris]]. we obtain 
$$H_n(X_1 \vee X_2) \cong H_n(X_1 \vee U_2) \oplus H_n(U_1 \vee X_2)$$
for $n>0$. In degree $0$, we have an [[short exact sequence|exact sequence]]
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
\{0\} \ar[r]& \tilde{H}_0(X_1 \vee U_2) \oplus \tilde{H}_0(U_1 \vee X_2) \ar[r, "\cong"]& \tilde{H}_0(X_1 \vee X_2) \ar[r]&\{0\}.
\end{tikzcd}
\end{document}
```
Induction proves this weaker statement.