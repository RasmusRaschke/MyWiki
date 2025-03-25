<div class="topSpace"></div>

Date Created: 25th March 2025
References: #Ref/Aluffi 
Tags: #Type/Definition

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Function).

Let $A$ and $B$ be sets. A <ins>(set-)function</ins> $$f: A \to B$$ $$a \mapsto f(a)$$ assignes every $a \in A$ exactly one $b \in B$. The datum of a function is its <ins>graph</ins> $$\Gamma_f := \{(a,b) \in A \times B\mid b=f(a)\} \sub A \times B.$$ For a subset $S \sub A$, we define the <ins>image</ins> of $S$ by $f$ as $$f(S)=\{b \in B \mid \exists a \in S: b=f(a)\}.$$ The image of $A$ is denoted $\im(f)$.
```

**Examples.**
1. Every set is equipped with the <ins>identity function</ins> $$id_A: A \to A$$ $$a \mapsto a.$$
2. Every subset $B \sub A$ has a <ins>canonical inclusion</ins> $$\iota: B \hookrightarrow A$$ $$B \ni b \mapsto b \in A.$$

**Remark.**
A function $f: A \to B$ can be restricted on a subset $S \sub A$, denoted $f|_S$ with $\forall s \in S: f|_S (s) =f(s)$. This can be written as $f|_S = f \circ \iota$.

# Composition

Functions can be composed: For functions $f: A \to B$ and $g: B \to C$ we define the composition $$g \circ f: A \to C$$ $$a \mapsto (g \circ f)(a):=g(f(a))$$ which can be represented by a commutative diagram:
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
A \arrow[dr, left, "g \circ f"'] \arrow[r, "f"] & B \arrow[d, "g"]\\
& C
\end{tikzcd}
\end{document}
```
Furthermore, composition satisfies the associative property: If $f: A \to B$, $g: B \to C$ and $h: C \to D$ are functions, $$h \circ (g \circ f) = (h \circ g) \circ f$$ is always satisfied.

# Injection, Surjection, Bijection



<i>.</i><span style="float:right;">$\blacksquare$</span>