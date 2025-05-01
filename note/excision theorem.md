<div class="topSpace"></div>

Date Created: [[01/05/2025]]
References: #Ref/AlgTop 
Tags: #Type/Theorem #Topic/AlgebraicTopology 

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: [[small singular simplex]] [[barycentric subdivision]] [[simplicial cone]]

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Theorem
title: Theorem (Excision).
Let $(X,A,W)$ be a triple of [[topological space|topological spaces]] such that $W \sub A \sub X$ and $\overline{W}\sub \mathring{A}$. Then the inclusion
$$
\iota: (X \setminus W, A \setminus W) \hookrightarrow (X,A)
$$
induces an [[isomorphism]]
$$
H_n(\iota): H_n(X \setminus W, A \setminus W) \overset{\cong}\to H_n(X,A)
$$
for all $n\geq 0$.
```
*Proof.*
Surjectivity: Let $c \in S_n(X,A)$ be a [[relative chain complex|relative cycle]], i.e. $\partial (c) \in S_{n-1}(A).$ Consider the open covering $\fU = \{\mathring{A}, X \setminus \overline{W}\} =:\{U,V\}.$ We find a $k$ such that $c':=B^k c$ is a chain in $S_n^\fU(X)$ and decompose $c'=c^U+c^V$ such that $c^U$ and $c^V$ are the components in the respective chain complex (not unique).
The boundary of $c'$ is given as $\partial c' = \partial B^k c = B^k \partial c,$ which is by assumption a chain in $S_{n-1}(A).$ However, we also have $\partial c' = \partial c^U + \partial c^V$ with $\partial c^U \sub S_{n-1}(U) \sub S_{n-1}(A)$, so $\partial c^V \in S_{n-1}(A \setminus W).$ Therefore, $c^V$ is a relative cycle in $S_n(X \setminus W, A \setminus W)$.  With this, we obtain surjectivity as
$$
H_n(\iota)[c^V] = [c] \in H_n(X,A)
$$
because $[c]=[c^U+c^V]=[c^V]$ in $H_n(X,A).$
Injectivity: Assume there exists $c \in S_n(X \setminus W)$ with $\partial c \in S_{n+1}(A \setminus W)$ and assume $H_n(\iota)[c]=0.$ This means precisely that $c$ is of form $c=\partial b + a'$ for some $b \in S_{n+1}(X)$ and $a' \in S_n(A).$ Write $b$ again as $b=b^U + b^V$ with $b^U \in S_{n+1}(U) \sub S_{n+1}(A)$ and $b^V \in S_{n+1}(V) \sub S_{n+1}(X \setminus W).$ Then
$$
c = \partial b^U + \partial b^V + a'.
$$
But $\partial b^U$ and $a'$ are elements in $S_n(A \setminus W)$, so $c = \partial b^V \in S_n(X \setminus W, A \setminus W).$