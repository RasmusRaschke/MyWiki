<div class="topSpace"></div>

Date Created: 01/04/2024
References: #Ref/Aluffi 
Tags: #Type/Definition #Topic/CategoryTheory

Proved by: <i>Not Applicable</i>
References:  [[slice category]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[category]]
Examples: [[pointed set]]

Fixing a common origin instead of the destination of morphisms leads to several dual counterparts of [[slice category|slice categories]].

``` ad-Definition
title: Definition (Coslice Category).

Let $\tC$ be a [[category]] and $A$ be an object of $\tC$. The <ins>coslice category</ins> $\tC^A$ is defined by:
 - $\Obj(\tC^A):$ All morphisms in $\tC$ with origin $A$.
 - $\Hom_{\tC^A}:$ For two arrows $f_1: A \to Z_1$ and $f_2: A \to Z_2$ in $\tC$ we consider commutative diagrams $\sigma: Z_1 \to Z_2$ such that $f_2 = \sigma f_1$.

```

**Proof.**
We have to define composition and prove the existence of the identity and associativity.
 1. Consider two commutative diagrams
 ```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
& A \arrow[dl,"f_1"']  \arrow[dr, "f_2"]& \\
Z_1  \arrow[rr, "\sigma"] & & Z_2
\end{tikzcd}
\end{document}
```
and
 ```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
& A \arrow[dl,"f_2"']  \arrow[dr, "f_3"]& \\
Z_2  \arrow[rr, "\tau"] & & Z_3
\end{tikzcd}
\end{document}
```
The commutativity criterion reads as $f_2 = \sigma f_1$ on the one hand and $f_3 = \tau f_2$ on the other. Combining leads to $$f_3 = \tau \sigma f_1$$.  This is equivalent to the following commutative diagram which we consider to be the composition of the diagrams above:
 ```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
& A \arrow[dl,"f_1"']  \arrow[dr, "f_3"]& \\
Z_1  \arrow[rr, "\tau \sigma"] & & Z_3
\end{tikzcd}
\end{document}
```
 2. The identity is inherited from $\tC$: Composing $\sigma: Z_1 \to Z_2$ with either $\id_{Z_1}$ from the right or $\id_{Z_2}$ from the left yields the same commutative diagram as $\sigma \id_{Z_1} = \sigma = \id_{Z_2} \sigma$.
 3. Associativity is inherited in the same way: If $\sigma: Z_1 \to Z_2$, $\tau: Z_2 \to Z_3$ and $\lambda: Z_3 \to Z_4$ represent commutative diagrams, we have $\lambda (\tau \sigma) = (\lambda \tau) \sigma$ because $\tC$ is a category to begin with. <span style="float:right;">$\blacksquare$</span>

**Example.**
[[pointed set|Pointed sets]] are a prominent example of a coslice category.

# Coslice Categories with multiple destinations

We can expand the above definition by considering two desinations $A$ and $B$ in $\Obj(\tC)$:
 - $\Obj(\tC^{A,B}):$ Diagrams 
 
  ```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
A \arrow[dr, "f"] & \\
& Z\\
B \arrow[ur, "g"]& 
\end{tikzcd}
\end{document}
```
  in $\tC$.

 - $\Hom_{\tC_{A,B}}:$ Again, we consider commutative diagrams
 ```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
A \arrow[dr, "f_1"] \arrow[drr, bend left, "f_2"] & & \\
& Z_1 \arrow[r, "\sigma"] & Z_2\\
B \arrow[ur, "g_1"] \arrow[urr, bend right, "g_2"'] & & 
\end{tikzcd}
\end{document}
 ```
where the commutative requirement can be shortened to $f_2 = \sigma f_1$ and $g_2 = \sigma g_2$.

Composition is defined analogously:

 ```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
A \arrow[dr, "f_1"] \arrow[drr, bend left, "f_2"] \arrow[drrr, bend left, "f_3"] & & & & &A \arrow[dr, "f_1"] \arrow[drr, bend left, "f_3"] & & \\
& Z_1 \arrow[r, "\sigma"] & Z_2 \arrow[r, "\tau"] & Z_3&:= & &Z_1 \arrow[r, "\tau \sigma"] &Z_3 \\
B \arrow[ur, "g_1"'] \arrow[urr, bend right, "g_2"'] \arrow[urrr, bend right, "g_3"']& & & & &B \arrow[ur, "g_1"] \arrow[urr,bend right, "g_3"] & & 
\end{tikzcd}
\end{document}
 ```

Identity and associativity are inherited from $\tC$ like above.

# Fibered Coslice Categories

Finally, we again consider a fibered variant $\tC^{\alpha, \beta}$ of the coslice categories above where we fix two morphisms $\alpha: C \to A$ and $\beta: C \to B$.
 - $\Obj(\tC^{\alpha, \beta}):$ The objects are now commutative diagrams 
 ```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
& A \arrow[dr, "f"]& \\
C \arrow[ur, "\alpha"] \arrow[dr, "\beta"'] & & Z\\
& B \arrow[ur, "g"']& \\
\end{tikzcd}
\end{document}
 ```
in $\tC$ with the requirement $f \alpha = g \beta$.
 - $\Hom_{\tC_{\alpha, \beta}}:$ The homsets are also certain commutative diagrams
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
& A \arrow[dr, "f_1"] \arrow[drr, bend left, "f_2"] & & \\
C \arrow[ur, "\alpha"] \arrow[dr, "\beta"'] & & Z_1 \arrow[r, "\sigma"] & Z_2\\
& B \arrow[ur, "g_1"'] \arrow[urr, bend right, "g_2"'] & & \\
\end{tikzcd}
\end{document}
 ```
 in $\tC$ with the commutation requirements $f_2 = \sigma f_1$ and $g_2 = \sigma g_1$.

We define composition again in the same way:

```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
& A \arrow[dr, "f_1"] \arrow[drr, bend left, "f_2"] \arrow[drrr, bend left, "f_3"] & & & & & & A\arrow[dr, "f_1"] \arrow[drr, bend left, "f_3"]& & \\
C \arrow[ur, "\alpha"] \arrow[dr, "\beta"'] & & Z_1 \arrow[r, "\sigma"] & Z_2 \arrow[r, "\tau"] & Z_3& := & C\arrow[ur, "\alpha"] \arrow[dr, "\beta"']& & Z_1 \arrow[r, "\tau \sigma"] & Z_3\\
& B \arrow[ur, "g_1"'] \arrow[urr, bend right, "g_2"'] \arrow[urrr, bend right, "g_3"'] & & & & & & B\arrow[ur, "g_1"'] \arrow[urr, bend right, "g_3"']  & & \\
\end{tikzcd}
\end{document}
 ```
 and note that identity and associativity are inherited from $\tC$ as above.