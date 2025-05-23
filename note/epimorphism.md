<div class="topSpace"></div>

Date Created: 26th March 2025
References: #Ref/Aluffi 
Tags: #Type/Definition #Topic/CategoryTheory

Proved by: [[set-function#Injection, Surjection, Bijection]]
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Definition

``` ad-Definition
title: Definition (Epimorphism).

Let $\tC$ be a [[category]]. A morphism $f \in \Hom_\tC(A,B)$ is an <ins>epimorphism</ins> if: For any object $Z$ and morphisms $\beta, \beta': B \to Z:$
$$
\beta \circ f = \beta' \circ f \implies \beta = \beta'.
$$

```
The following diagram commutes for any epimorphism $f$:
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
& & Z \\
A \arrow[r, "f"] \arrow[urr, bend left, "\beta \circ f"] \arrow[drr, bend right, "\beta' \circ f"'] & B \arrow[ur, "\beta"] \arrow[dr, "\beta'"']& \\
& & Z 
\end{tikzcd}
\end{document}
```

**Remark.**
There are categories in which epimorphisms are not identical to [[set-function#Injection, Surjection, Bijection|surjections]]. For example, $(\Z, \leq)$ as seen in [[category|here]] has at most one morphism for any two objects. Therefore, being an epimorphism is vacuous and all morphisms are epimorphisms (and [[monomorphism|monomorphisms]]). Nevertheless, there are no [[isomorphism|isomorphisms]] beside the identities. 

# Epimorphisms in the category ${\large \Set}$

``` ad-Proposition
title: Proposition (Surjective set-functions are epimorphisms).

A function $f: A \to B$ is surjective if and only if it is an epimorphism.

```

*Proof.*
$(\Leftarrow)$ Let $f:A \to B$ be surjective and $g: B \to A$ its right-inverse. Let $\beta, \beta': B \to Z$ be arbitrary as above with $\beta \circ f = \beta' \circ f$. Composing with $g$ from the right yields
$$
\beta \circ \underbrace{( f \circ g)}_{\id_B} = (\beta \circ f) \circ g = \beta \circ f = \beta' \circ f = (\beta' \circ f) \circ g = \beta' \circ \underbrace{( f \circ g)}_{\id_B}
$$
and we conclude $\beta = \beta'$ as desired.
$(\Rightarrow)$ Now, let $f$ be an epimorphism. We consider $Z:=\{0,1\}$ and define
$$
\begin{align*}
\beta: b &\mapsto 0 \\
\beta': b &\mapsto
\begin{cases}
0, & \text{ if } b \in \im(f), \\
1, & \text{ else}.
\end{cases}
\end{align*}
$$
Since $f$ is an epimorphism, $\beta \circ f = \beta' \circ f \implies \beta = \beta'$ holds. By construction, $\beta \circ f = \beta' \circ f = 0$. Therefore, we conclude $\beta = \beta'$, which is only possible for $\im(f) =B$.
<span style="float:right;">$\blacksquare$</span>