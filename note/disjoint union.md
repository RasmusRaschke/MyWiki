<div class="topSpace"></div>

Date Created: \today
References: #Ref/Aluffi
Tags: #Type/Definition

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[initial topology]]
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Disjoint Union).

Let $\{A_i\}_{i \in I}$ be a family of sets indexed by the set $I$. The <ins>disjoint union</ins> of all $A_i \in \cA$ is constructed by taking pairwise disjoint copies $A_i'$ for all $i \in I$ and forming the union: $$ \coprod_{i \in I} A_i := \bigcup_{i \in I} A_i' \cong \bigcup_{i \in I} A_i \times \{i\}.$$
```

**Remark.** This operation is well defined as different ways to produce disjoint copies $A_i'$ out of $A_i$ lead to isomorphic structures.
<i>Proof.</i>
Let $A' \cong A''$, $B' \cong B''$ be sets and $A' \cap B' = \emptyset$. We have to show that $A' \cup B' \cong A'' \cup B''$. Let $\phi_A: A' \to A''$ and $\phi_B: B' \to B''$ be the given isomorphisms. We define a set-function $$\psi: A' \cup B' \to A'' \cup B''$$ $$x \mapsto \begin{split} \phi_A(x), \ &\text{if} \ x \in A'\\ \phi_B(x), \ &\text{if} \ x \in B' \end{split}$$ with the obvious inverse $$\psi^{-1}: A'' \cup B'' \to A' \cup B'$$ $$y \mapsto \begin{split} \phi^{-1}_A(y), \ &\text{if} \ y \in A''\\ \phi^{-1}_B(y), \ &\text{if} \ y \in B'' \end{split}.$$ Since $A'$ and $A''$ as well as $B'$ and $B''$ are disjoint, $\psi$ is well defined. Bijectivity is inherited from the fact that $\phi_{A,B}$ are isomorphisms. Therefore, $A' \cup B' \cong A'' \cup B''$ and $\coprod$ is well defined up to isomorphism.
<span style="float:right;">$\blacksquare$</span>