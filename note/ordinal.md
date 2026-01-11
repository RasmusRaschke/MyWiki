<div class="topSpace"></div>

Date Created: {{date::DD/MM/YYYY}}
References: Riehl/CatCont
Tags: #Topic/SetTheory #Type/Definition

Proved By: <i>Not Applicable</i>
Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

```ad-Definition
title: Definition (Ordinal Number).
A [[set|set]] $S$ is called <u>ordinal number</u> if:
- $S$ is [[order|totally ordered]] with respect to set inclusion.
- Every element of $S$ is a subset of $S$.
```

_Examples_

1. The [[natural numbers|natural numbers]] are ordinal numbers by construction, since e.g. $2=\{0,1\}$.

_Remark_
Ordinals $\alpha = \{\beta \mid \beta < \alpha\}$ form a category $\Ord$ whose objects are smaller ordinals such that there is a morphism from any object to every greater or equal object and every morphism decomposes as a morphism between successors. For example, $\overline{0}$ has no objects and no morphisms, $\overline{1}$ has one object and the identity, $\overline{2}$ has two objects, the identities and one morphism in between. The category $\overline{\omega}$ is freely gnerated by $$0 \to 1 \to 2 \to \cdots$$.
