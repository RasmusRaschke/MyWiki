<div class="topSpace"></div>

Date Created: 24th March 2025
References: #Ref/Aluffi 
Tags: #Type/Definition #Topic/SetTheory

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Relation

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

We denote <ins>equivalence classes</ins> by $[a]_\sim := \{b \in S \mid b \sim a\}$. The <ins>quotient</ins> $S/_\sim$ of $S$ with respect to $\sim$ is the set of equivalence classes of $S$. 
```

**Remark.**
An equivalence relation carries the same datum as a [[set#Partition|partition]] of a set: If $\sP$ is a partition of $S$, we define an equivalence relation by $a \sim b :\iff a,b \in A$ for some $A \in \sP$. Conversely, if $\sim$ is an equivalence relation, the equivalence classes $[a]_\sim$ partition $S$ such that $\sP$ and $\sim$ agree on each other.

**Examples.**
 1. We define $\equiv_2$ on $\Z$ by setting $a \equiv_2 b :\iff a-b \in 2\Z$. This partitions the integers in even and odd numbers: $\Z/_\sim = \{[0],[1]\}$.
 2. The relation $a \sim b :\iff b-a \in \Z$, defined on $\R$, leads to a quotient isomorphic to the unit circle: $\R / _\sim \cong \S^1$. On $\R^2$, we obtain the unit torus instead.

**Remark.**
The quotient $A/_\sim$ comes with a [[set-function#Injection, Surjection, Bijection|surjective]] <ins>canonical projection</ins> $$\pi: A \twoheadrightarrow A/_\sim$$ defined by $\pi(a):=[a]_\sim$.

# Universal Property

``` ad-Proposition
title: Proposition (Universal Property of the Quotient).

Let $A$ be a [[set]] and $\sim$ be an equivalence relation on $A$. The quotient $A/\sim$ is universal with respect to the property of mapping $A$ to a set such that equivalent elements have equal image.
```

*Proof.*
We are now working in the [[coslice category]]: Objects are functions $\phi: A \to Z$ for arbitrary $Z$ such that $a \sim a' \implies \phi(a)=\phi(a')$, denoted $(\phi, Z)$. Morphisms are commutative diagrams
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
Z_1 \arrow[rr, "\sigma"]& & Z_2\\
& A \arrow[ul, "\varphi_1"] \arrow[ur, "\varphi_2"'] &.
\end{tikzcd}
\end{document}
```
To summarise, we want to prove that $(\pi, A/\sim)$ is [[category#Terminal Objects|initial]] in this [[coslice category]]. This means that there exists a unique morphism $(\pi, A/\sim) \to (\phi, Z)$ equivalent to the unique commutative diagram
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
A/\sim \arrow[rr, "\overline{\varphi}"]& & Z\\
& A \arrow[ul, "\pi"] \arrow[ur, "\varphi"'] &.
\end{tikzcd}
\end{document}
```
Explicitly, we search a function $\overline{\phi}$ which makes this diagram commute. Let $[a] \in A/\sim$. If the diagram is commutative, we necessarily obtain $$\overline{\varphi}([a]) = \phi(a)$$ and therefore uniqueness, but not existence. For that, we need well-definedness of the prescription. This follows directly:
$$
[a_1] = [a_2] \implies a_1 \sim a_2 \implies \phi(a_1)=\phi(a_2).
$$
<span style="float:right;">$\blacksquare$</span>