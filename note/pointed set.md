<div class="topSpace"></div>

Date Created: 03/04/25
References: #Ref/Aluffi 
Tags: #Type/Definition #Topic/CategoryTheory

Proved by: <i>Not Applicable</i>
References: [[coslice category]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Pointed Set).

We define a [[coslice category]] $\pSet$, called <ins>pointed sets</ins>, by fixing a singleton $\{\ast\}$ and considering morphisms:
 - $\Obj(\pSet):$ [[set-function|Set-functions]] $f: \{\ast\} \to S$ for any set $S$. An object is therefore encoded by a choice of $S$ and $s \in S$ such that $f(\ast)=:s$. Therefore, we write objects as pairs $(S,s)$.
 - $\Hom_{\pSet}((S,s), (T,t)):$ Morphisms are ordinary [[set-function|set-functions]] $\sigma: S \to T$ such that $\sigma(s) = t$.

```

Pointed sets are important examples of [[coslice category|coslice categories]].