<div class="topSpace"></div>

Date Created: [[14/05/2025]]
References: #Ref/Hatcher
Tags: #Type/Definition #Topic/AlgebraicTopology #Type/Theorem 

Proved by: <i>Not Applicable</i>
References: [[CW complex]] [[cofibration]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Homotopy Extension Property).
Let $X$ be a [[topological space]] and $A \sub X$ be a subspace. The pair $(X,A)$ is said to have the <ins>homotopy extension property (HEP)</ins> if the following holds:
For any map $f: X \to Y$ between [[topological space|topological spaces]] and any homotopy
$$
H: A \times [0,1] \to Y
$$
exists an extended homotopy
$$
\tilde{H}: X \times [0,1] \to Y
$$
such that $\tilde{H}(x,0)=f$ for all $x \in X$ and $\tilde{H}|_A = H$.
```

**Remark.**
Equivalently, a pair $(X,A)$ has the HEP if and only if $X \times \{0\} \cup A \times [0,1]$ is a [[retract]] of $X \times I$.
For the first implication, we note that the HEP implies that the identity $$\id: X \times \{0\} \cup A \times I \to X \times \{0\} \cup A \times [0,1]$$ extends  to a map $$X \times [0,1] \to X \times \{0\} \cup A \times [0,1],$$ hence $X \times \{0\} \cup A \times [0,1]$ is a [[retract]] of $X \times [0,1]$.
The converse is only easy when $A$ is closed.

# HEP of CW complexes

``` ad-Proposition
title: Proposition (CW Complexes have HEP).
Let $X$ be a [[CW complex#Objects|CW complex]] and $A$ a [[CW complex#Subcomplexes|subcomplex]]. Then $X \times \{0\} \cup A \times [0,1]$ is a [[retract#Strong Retraction|strong deformation retract]] of $X \times [0,1]$.
```
*Proof.*
The strong retraction
$$
r: \D^n \times [0,1] \to \D^n \times \{0\} \cup \S^{n-1} \times [0,1]
$$
is given by the standard retraction of the cylinder onto its bottom and sides.
The $n$-skeleton $X^n \times [0,1]$ is build out of $X^n \times \{0\} \cup (X^{n-1} \cup A^n) \times [0,1]$ by gluing copies of $D^n \times [0,1]$ along $\D^n \times \{0\} \cup \S^{n-1} \times [0,1]$. This already yields a [[retract#Deformation Retraction|deformation retract]]. We parametrize the retracting homotopy such that it takes place in a time interval $\left[ \frac{1}{2^{n+1}}, \frac{1}{2^n}\right].$ With the direct limit topology on $X$, we obtain a deformation from $X \times [0,1]$ to $X \times \{0\}\cup A \times [0,1]$.