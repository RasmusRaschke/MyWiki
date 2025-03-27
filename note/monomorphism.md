<div class="topSpace"></div>

Date Created: 26th March 2025
References: #Ref/Aluffi 
Tags: #Type/Definition

Proved by: [[set-function#Injection, Surjection, Bijection]]
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Monomorphism).

A map $f: A \to B$ is a <ins>monomorphism</ins> if: For any set $Z$ and functions $\alpha, \alpha': Z \to A:$
$$
f \circ \alpha = f \circ \alpha' \implies \alpha = \alpha'.
$$

```
The following diagram commutes for any monomorphism $f$:
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
Z \arrow[dr, "\alpha"] \arrow[drr, bend left, "f \circ \alpha"] & &\\
& A \arrow[r, "f"]& B\\
Z \arrow[ur, "\alpha'"'] \arrow[urr, bend right, "f \circ \alpha'"']& &
\end{tikzcd}
\end{document}
```

# Monomorphisms in the cathegory ${\large \set}$

``` ad-Proposition
title: Proposition (Injective set-functions are monomorphisms).

A function $f: A \to B$ is injective if and only if it is a monomorphism.

```

**Proof.**
$(\Leftarrow)$ Let $f: A \to B$ be injective. By [[set-function#Injection, Surjection, Bijection|injections have left-inverses]], we find a left-inverse $g: B \to A$. Now, let $\alpha, \alpha': Z \to A$ be as described above with $f \circ \alpha = f \circ \alpha'$. We compose with $g$ from the left:
$$
\underbrace{(g \circ f)}_{id_A} \circ \alpha = g \circ (f \circ \alpha) = g \circ (f \circ \alpha') = \underbrace{(g \circ f)}_{id_A} \circ \alpha'.
$$
We conclude that $\alpha = \alpha'$.
$(\Rightarrow)$ Assume $f$ is a monomorphism and let $Z = \{p\}$ for some arbitrary $p$. We define $a := \alpha(p)$ and $a' := \alpha'(p)$. By assumption,
$$
f \circ \alpha(p) = f \circ \alpha'(p) \implies \alpha = \alpha'.
$$
Now, since there is only one value $p$, $\alpha$ and $\alpha'$ are equal if and only if they send $p$ to the same value in $A$. This means
$$
f(a) = f(a') \implies a = a'
$$
for all choices of $\alpha$ and $\alpha'$ (and $a,a'$ respectively). Therefore, $f$ is surjective.
<span style="float:right;">$\blacksquare$</span>