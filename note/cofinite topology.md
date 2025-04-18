<div class="topSpace"></div>

Date Created: [[18/04/2025]]
References: #Ref/Topo 
Tags: #Type/Definition

Proved by: <i>Not Applicable</i>
References: [[topological space]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Definition 

``` ad-Definition
title: Definition (Cofinite Topology).

Let $X$ be a set. The <ins>cofinite or finite complement topology</ins> $\cT_f$ contains all subsets $U \sub X$ such that either $X \setminus U$ is finite or $X \setminus U =X$. 

```

*Proof.*
We have to show that this actually defines a [[topological space|topology]] on $X$:
1. We have $X \setminus X = \emptyset$ and $X \setminus \emptyset = X$, so $X, \emptyset \in \cT_f$.
2. Let $(A_i)_{i \in I}$ be a family of open sets, so $X \setminus A_i$ is either finite or all of $X$ for any $A_i$. But $$X \setminus \bigcup U_i = \bigcap (X \setminus U_i)$$ and intersections of finite sets are finite.
3. Let $A,B \in \cT_f$. We have $X \setminus (A \cap B) =  (X \setminus A)  \cup (X \setminus B)$ which is clearly finite as finite unions of finite sets are finite.

<span style="float:right;">$\blacksquare$</span>