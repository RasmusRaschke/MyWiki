<div class="topSpace"></div>

Date Created: 18/09/24
References: 
Tags: #Type/Definition #Topic/SetTheory

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Relation).
Let $X$ and $Y$ be two not necessarily different sets and $X \times Y$ be their cartesian product. A __relation__ between $X$ and $Y$ is a subset $R \sub X \times Y$. For $(x,y) \in X \times Y$ we write $xRy$ iff $(x,y) \in R$.

```

``` ad-Definition
title: Definition (Equivalence Relation).
A relation $\sim$ on $X$ is called __equivalence relation__ iff it has three properties:
1. reflexivity: $\forall x \in X: x \sim x$
2. symmetry: $\forall x,y \in X: x \sim y \implies y \sim x$
3. transitivity: $\forall x,y,z \in X: (x \sim y \wedge y \sim z) \implies x \sim z$

```
``` ad-Definition
title: Definition (Equivalence Class).
Let $X$ be a set and $\sim$ an equivalence equation on $X$. Any element $x \in X$ defines an __equivalence class__ $$[x] := \{y \in x | y \sim x\}$$

```
``` ad-Definition
title: Definition (Quotient Set).
Let $X$ be a set with an equivalence relation $\sim$. The set of all equivalence classes $X \diagup \sim$ is called __quotient set__ of $X$ by $\sim$.

```
``` ad-Definition
title: Definition (Canonical Projection).
The surjective map $$\pi: X \to X \diagup \sim$$ $$x \mapsto [x]$$ is called __canonical projection__ or __canonical surjection__.

```


<i>.</i>