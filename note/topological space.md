<div class="topSpace"></div>

Date Created: 18/04/2025
References: #Ref/Topo
Tags: #Type/Definition #Topic/Topology

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[set]]
Examples: [[cofinite topology]]

# Definition

``` ad-Definition
title: Definition (Topological Space).

A <ins>topological space</ins> is a pair $(X, \cT)$ consisting of a [[set]] $X$ and a collection $\cT$ of subsets of $X$ such that
1. $X, \emptyset \in \cT$
2. Let $(A_i)_{i \in I}$ be an arbitrary family of sets with $A_i \in \cT$ for all $i$. Then $\bigcup_{i \in I} A_i \in \cT$.
3. $\forall A,B \in \cT: A \cap B \in \cT$

The elements of $\cT$ are called <ins>open sets</ins>. $\cT$ is called <ins>topology</ins> on $X$.
```

A topology therefore has to be closed under finite intersections and arbitrary unions.

**Examples.**
1. Any [[set]] $X$ can be endowed with the <ins>discrete topology</ins> $\cT = \fP(X)$, where $\fP(X)$ is the power set of $X$.
2. Analogously, any set $X$ can be endowed with the <ins>indiscrete or trivial topology</ins> $\cT:=\{X,\emptyset\}$. 

# Comparison of Topologies

``` ad-Definition
title: Definition (Fine and Coarse).

Let $\cT, \cT'$ be topologies on the same set $X$. $\cT$ is called <ins>coarser</ins> and $\cT'$ <ins>finer</ins> if $\cT \subseteq \cT'$. If the inclusion is strict, they are called <ins>strictly</ins> coarser resp. finer. If either $\cT \subset \cT'$ or $\cT' \subset \cT$ holds they are called <ins>comparable</ins>.
```

**Remark.**
Sometimes, the words <ins>stronger</ins> and <ins>weaker</ins> are used instead. However, analysts and topologists tend to use those two words with opposing meaning.