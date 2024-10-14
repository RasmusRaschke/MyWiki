<div class="topSpace"></div>

Date Created: 15/10/24
References: #Ref/DiffGeo 
Tags: #Type/Definition #Topic/Topology 

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Covering Projection).

Let $X,Y$ be [[topological space|topological spaces]] and $\pi: X \to Y$ be a continous map. $\pi$ is called __covering (projection)__ if $\pi$ is surjective and every point $b \in Y$ has a neighbourhood $U \sub Y$ such that $$\pi^{-1}(U) = \bigsqcup_{i \in I} V_i$$ with $V_i \sub X$ is open and $$\pi|_{V_i}: V_i \to U$$ is a [[homeomorphism]] for all $i \in I$. 

```
**Example.**
$$\exp: \R \to \S^1$$ $$t \mapsto \exp(2\pi it)$$