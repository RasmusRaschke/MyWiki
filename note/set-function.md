<div class="topSpace"></div>

Date Created: 25th March 2025
References: #Ref/Aluffi 
Tags: #Type/Definition 

Proved by: [[axiom of choice]]
References: [[set]]
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

``` ad-Definition
title: Definition (Surjective, Injective, Bijective).

Let $f: A \to B$ be a function. $f$ is called:
 - <ins>injective</ins> or <ins>one-to-one</ins> if $$\forall a',a'' \in A: a' \neq a'' \implies f(a') \neq f(a'')$$ or equivalently $$\forall a',a'' \in A: f(a') = f(a'') \implies a'=a''.$$
 - <ins>surjective</ins> or <ins>onto</ins> if $$\forall b \in B \exists a \in A: b = f(a).$$
 - <ins>bijective</ins> or <ins>[[isomorphism]] of sets</ins> if it is both injective and surjective.

If $f$ is a bijection we call $A$ and $B$ isomorphic and write $A \cong B$.
```

``` ad-Proposition
title: Proposition (Left- and Right-Inverse).

Let $A \neq \emptyset$ and $f: A \to B$ be a function. Then
 1. $f$ has a left-inverse if and only if $f$ is injective.
 2. $f$ has a right-inverse if and only if $f$ is surjective.
```
**Proof.**
 (1) 
 $(\Rightarrow)$ Assume $f: A \to B$ has a left-inverse $g: B \to A$ such that $g \circ f = \id_A$. Let $a',a'' \in A$ be elements such that $a' \neq a''$. Then $$g(f(a'))= \id_A(a')=a'\neq a'' = \id_A(a'')=g(f(a'')),$$ so $f$ needs to sent $a'$ and $a''$ to different elements for this equation to hold. Therefore, $f$ is injective.
 $(\Leftarrow)$ Assume $f$ is injective. We construct a left-inverse $g: B \to A$ in the following way: Fix any $t \in A$ (since $A$ is non-empty) and set 
 $$
 g(b):= 
 \begin{cases}
 a,& \text{ if } \exists a \in A: b=f(a)\\ 
 s, &\text{ if } b \notin \im(f).
 \end{cases}
 $$
 Since $f$ is injective, every element of $B$ is assigned no more than one value. Also, $g$ is the desired left-inverse: If $a \in \im(f)$, then $g(f(a))=a=\id_A(a)$.
 (2)
 $(\Rightarrow)$ Assume $h:B \to A$ to be a right-inverse of $f$. For $B = \emptyset$ the proposition is empty. Therefore, let $B \neq \emptyset$. Since $g$ is a right-inverse, we obtain $$b=f(h(b))$$ for all $b \in B$, but this defines an element $h(b)=:a \in A$ such that $f(a)=b$.
 $(\Leftarrow)$ Assume $f$ is surjective. For every $b \in B$ we have a fiber $f^{-1}(b) \sub A$ over $A$. The set of fibers is a [[set#Partition|partition]] of $A$: Every fiber is non-empty (surjectiveness) and the fibers are pairwise disjoint by construction. The [[axiom of choice]] allows us to choose one $a_b \in f^{-1}(a)$. We define a right-inverse $h:B \to A$ by setting $h(b):=a_b$ which fulfills $f(h(b))=f(a_b)=b$.
<span style="float:right;">$\blacksquare$</span>

``` ad-Proposition
title: Corollary (Two-sided Inverse).

A function $f:A \to B$ is a bijection if and only if it has a two-sided inverse.
```

We denote the inverse of a bijection $f: A \to B$ as $f^{-1}:B \to A$. 
For arbitrary $f:A \to B$, we call $T \sub B$, we call $f^{-1}(T) \sub A$ the <ins>preimage</ins> of $T$. If $T$ is a singleton like above, we call $f^{-1}(p) \sub A$ <ins>fiber</ins> of $f$ over $p$. If $f$ is surjective, the right-inverses of $f$ are called <ins>sections</ins>.