<div class="topSpace"></div>

Date Created: 24th March 2025
References: #Ref/Aluffi 
Tags: #Type/Definition

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Relation).

Let $S$ be a [[set]]. A <ins>relation</ins> on $S$ is a subset $R \sub S \times S$. We say $a$ and $b$ are related by $R$, written as $aRb$, if $(a,b) \in R$.
```

**Example**
The trivial relation is given by $=$. It corresponds to the <ins>diagonal</ins> $$\Delta := \{(a,b) \in S \times S \mid a=b\}=\{(a,a)\mid a \in S\}.$$

# Equivalence Relation

``` ad-Definition
title: Definition (Equivalence Relation).

Let $S$ be a [[set]]. A relation $\sim$ on $S$ is called <ins>equivalence relation</ins> if it satisfies the following conditions:
 - reflexivity: $\forall a \in S: a \sim a$
 - symmetry: $\forall a, b \in S:$ $a \sim b \implies b \sim a$
 - transitivity: $\forall a,b,c \in S:$ $a \sim b \land b \sim c \implies a \sim c$.

We denote <ins>equivalence classes</ins> by $[a]_\sim := \{b \in S \mid b \sim a\}$. The <ins>quotient</ins> $S/\sim$ of $S$ with respect to $\sim$ is the set of equivalence classes of $S$. 
```

**Remark.**
An equivalence relation carries the same datum as a [[set#partition]] of a set: If $\sP$ is a partition of $S$, we define an equivalence relation by $a \sim b :\iff a,b \in A$ for some $A \in \sP$. Conversely, if $\sim$ is an equivalence relation, the equivalence classes $[a]_\sim$ partition $S$.

<i>.</i><span style="float:right;">$\blacksquare$</span>