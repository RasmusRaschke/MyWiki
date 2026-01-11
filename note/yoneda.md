<div class="topSpace"></div>

Date Created: {{date::DD/MM/YYYY}}
References: Riehl/CatCont
Tags: #Topic/CategoryTheory #Type/Theorem

Proved By: <i>Not Applicable</i>
Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: [[cayleys theorem]]

```ad-Theorem
title: Theorem (Yoneda Lemma).
Let $\mathtt{C}$ be a [[category#Small Categories|locally small category]] and $\mathcal{F}: \mathtt{C} \to \Set$ be a [[functor|functor]]. Then for any $c \in \ob \mathtt{C}$, there is a bijection $$\Hom(\mathtt{C}(c,-), \mathcal{F}) \cong \mathcal{F}c$$ assigning a [[natural_transformation|natural transformation]] $\alpha: \mathtt{C}(c,-) \Rightarrow \mathcal{F}$ to $\alpha_c(1_c) \in \mathcal{F}c$. This bijection is [[natural_transformation|natural]] in $c$ and $\mathcal{F}$.
```

**_Proof_**

Bijection:
