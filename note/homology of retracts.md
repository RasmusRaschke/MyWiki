<div class="topSpace"></div>

Date Created: [[30/04/2025]]
References: #Ref/AlgTop 
Tags: #Type/Proposition 

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: [[retract]]

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Weak Retract

``` ad-Proposition
title: Proposition (Homology of Weak Retracts).
Let $(X,A)$ be a pair of spaces and $A$ be a [[retract#Weak Retraction|weak retract]] of $X$ by means of inclusion. Then
$$
H_n(X) \cong H_n(A) \oplus H_n(X,A)
$$
for all $n \geq 0$.
```

*Proof.*
Being a weak retract, we obtain $r: X \to A$ such that $r \iota_A \simeq \id_A$. This means that the induced maps satisfy
$$
H_n(r)H_n(\iota_A)=H_n(r\iota_A)=H_n(\id_A)=\id_{H_n(A)}
$$
for all $n$. Hence, $H_n(\iota_A)$ is injective for all $n$ by means of having a left-inverse. This implies exactness of
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
0 \arrow[r] & H_n(A) \arrow[r, "H_n(\iota_A)"] & H_n(X) \arrow[r,"\pi_\ast"] & H_n(X,A) \arrow[r] &0
\end{tikzcd}
\end{document}
```
for all $n$. With $H_n(r)$ being a left-inverse, we already obtain a split exact sequence
$$
H_n(X) \cong H_n(A) \oplus H_n(X,A)
$$
by mapping $[c] \in H_n(X)$ to $([r(c)], \pi_\ast[c])$ with inverse
$$
([a],[b]) \mapsto H_n(\iota_A)[a]+[a']-H_n(\iota_Ar)[a'] \in H_n(X)
$$
for any $[a'] \in H_n(X)$ with $\pi_\ast[a']=[b]$. We have to check well-definedness: If $[a''] \in H_n(X)$ is another element with $\pi_\ast[a'']=[b]$, then $[a'-a'']$ is of form $H_n(\iota_A)[\tilde{a}]$ because it lies in $\ker(\pi_\ast)=\im(H_n(\iota_A))$. Therefore, $[a'-a'']-H_n(\iota_Ar)[a'-a'']=[0]$.
<span style="float:right;">$\blacksquare$</span>

# Deformation Retract

``` ad-Proposition
title: Proposition (Homology of Deformation Retracts).
Let $(X,A)$ be a pair of spaces with $\emptyset \neq A \sub X$ such that $X$ [[retract#Deformation Retraction|deformation retracts]] on $A$. Then
$$
H_n(\iota_A):H_n(A) \cong H_n(X)
$$
and
$$
H_n(X,A) \cong \{0\}
$$
for all $n \geq 0$.
```
*Proof.*
Since $A$ is a [[retract#Deformation Retraction|deformation retract]] of $X$, there exists a homotopy
$$
H: X \times [0,1] \to X
$$
such that $H_0(x)=x$ and $H_1(x) \in A$ for all $x \in X$ as well as $H_1(a)=a$ for all $a \in A$. This means that $H$ is a homotopy $\iota_A r \simeq \id_X$ such that $r=H_1(\cdot): X \to A$ is a [[retract|retraction]] with $r\iota_A = \id_A$. This means that $A \simeq X$ and $H_n(\iota_A)$ is an [[isomorphism]] for all $n \geq 0$.
<span style="float:right;">$\blacksquare$</span>