<div class="topSpace"></div>

Date Created: {{date::DD/MM/YYYY}}
References: Riehl/CatCont
Tags: #Type/Definition #Topic/SetTheory

Proved By: <i>Not Applicable</i>
Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Preorder

```ad-Definition
title: Definition (Preorder).
   Given a [[set|set]] $S$, a <u>preorder</u> on $S$ is a binary relation $\lesssim$ such that for all $a,b,c \in S$, we have:
- Reflexivity: $a \lesssim a$
- Transitivity: $a \lesssim b \land b \lesssim c \implies a \lesssim c$.
In that case, we call $(P, \lesssim)$ a <u>preordered set</u>.
```

_Examples_

1. [[Big O|Asymptotic order]] induces a preorder over functions $f: \mathbb{N} \to \mathbb{N}$.
2. If $X$ is a [[topological space|topological space]], we define $x \lesssim y$ if $x$ is in every neighbourhood of $y$. This is a preorder.
