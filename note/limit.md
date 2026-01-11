<div class="topSpace"></div>

Date Created: {{date::DD/MM/YYYY}}
References: Riehl/CatCont
Tags: #Topic/CategoryTheory #Type/Definition

Proved By: <i>Not Applicable</i>
Specializations: <i>Not Applicable</i>
Generalizations: [[cone]]
Examples: [[product]]

# Limits and Colimits

```ad-Definition
title: Definition (Limit and Colimit).
Let $\mathcal{F}: \mathtt{J} \to \mathtt{C}$ be a [[diagram|diagram]] of shape $\mathtt{J}$.
- A <u>limit</u> over $\mathcal{F}$, written $\lim_\mathtt{J} \mathcal{F}$, is a [[terminal object|final object]] in the [[cone|category]] $\Cone_\mathcal{F}$.
- A <u>colimit</u> over $\mathcal{F}$, written $\colim_\mathtt{J} \mathcal{F}$, is a [[terminal object|final object]] in the [[cone|category]] $\Cone^\mathcal{F}$.
```

# Complete Categories

```ad-Definition
title: Definition (Completeness and Cocompleteness).
- A [[category|category]] is <u>complete</u> if every small [[diagram|diagram]] has a limit in $\mathtt{C}$.
- A [[category|category]] is <u>cocomplete</u> if every small [[diagram|diagram]] has a colimit in $\mathtt{C}$.
```

# Limits and Functors

```ad-Definition
title: Definition (Limits and Functors).
Let $\mathtcal{K}: \mathtt{J} \to \mathtt{C}$ be a [[diagram|diagram]] of shape $\mathtt{J}$ and $\mathcal{F}: \mathtt{C} \to \mathtt{D}$ be a [[functor|functor]]. We say:
- $\mathcal{F}$ <u>preserves</u> limits of shape $\mathtt{J}$ if for any limit over $\mathcal{K}$, the image of the limit cone is again a limit over $\mathcal{F}\mathcal{K}: \mathtt{J} \to \mathtt{D}$.
- $\mathcal{F}$ <u>reflects</u> limits of shape $\mathtt{J}$ if for any [[cone|cone]] over $\mathcal{K}: \mathtt{J} \to \mathtt{C}$ whose image is a limit cone over $\mathcal{F}\mathcal{K}: \mathtt{J} \to \mathtt{D}$ the original cone is also a limit in $\mathtt{C}$.
- $\mathcal{F}$ <u>creates</u> limits of shape $\mathtt{J}$ if whenever $\mathcal{F}\mathcal{K}: \mathtt{J} \to \mathtt{D}$ has a limit in $\mathtt{D}$, there is some limit cone over $\mathcal{F}\mathcal{K}$ that can be lifted to a limit cone over $\mathcal{K}$, and $\mathcal{F}$ reflects the limits of this shape.
These definitions dualize to colimits.
```
