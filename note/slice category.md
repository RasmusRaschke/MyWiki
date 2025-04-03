<div class="topSpace"></div>

Date Created: 01/04/2024
References: #Ref/Aluffi 
Tags: #Type/Definition #Topic/CategoryTheory 

Proved by: <i>Not Applicable</i>
References:  [[coslice category]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[category]]
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Slice Category).

Let $\tC$ be a [[category]] and $A$ be an object of $\tC$. The <ins>slice category</ins> $\tC_A$ is defined by:
 - $\Obj(\tC_A):$ All morphisms in $\tC$ with desination $A$.
 - $\Hom_{\tC_A}:$ For two arrows $f_1: Z_1 \to A$ and $f_2: Z_2 \to A$ in $\tC$ we consider commutative diagrams $\sigma: Z_1 \to Z_2$ such that $f_1 = f_2 \sigma$.

```

**Proof.**
We have to define composition and prove the existence of the identity and associativity.
 1. Consider two commutative diagrams
 ```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
Z_1 \arrow[dr,"f_1"] \arrow[rr, "\sigma"] & & Z_2 \arrow[dl, "f_2"']\\
& A & 
\end{tikzcd}
\end{document}
```
and
 ```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
Z_2 \arrow[dr,"f_2"] \arrow[rr, "\tau"] & & Z_3 \arrow[dl, "f_3"']\\
& A & .
\end{tikzcd}
\end{document}
```
The commutativity criterion reads as $f_1 = f_2\sigma$ on the one hand and $f_2 = f_3 \tau$ on the other. Combining leads to $$f_1 = f_3 \tau \sigma.$$  This is equivalent to the following commutative diagram which we consider the composition of the diagrams above:
 ```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
Z_1 \arrow[dr,"f_1"] \arrow[rr, "\tau \sigma"] & & Z_3 \arrow[dl, "f_3"']\\
& A & .
\end{tikzcd}
\end{document}
```
 2. The identity is inherited from $\tC$: Composing $\sigma: Z_1 \to Z_2$ with either $\id_{Z_1}$ from the right or $\id_{Z_2}$ from the left yields the same commutative diagram as $\sigma \id_{Z_1} = \sigma = \id_{Z_2} \sigma$.
 3. Associativity is inherited in the same way: If $\sigma: Z_1 \to Z_2$, $\tau: Z_2 \to Z_3$ and $\lambda: Z_3 \to Z_4$ represent commutative diagrams, we have $\lambda (\tau \sigma) = (\lambda \tau) \sigma$ because $\tC$ is a category to begin with. <span style="float:right;">$\blacksquare$</span>

# Slice Categories with multiple destinations

We can expand the above definition by considering two desinations $A$ and $B$ in $\Obj(\tC)$:
 - $\Obj(\tC_{A,B}):$ Diagrams 
 
  ```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
 & A \\
Z \arrow[ur, "f"] \arrow[dr, "g"']& \\
 & B
\end{tikzcd}
\end{document}
```
  in $\tC$.

 - $\Hom_{\tC_{A,B}}:$ Again, we consider commutative diagrams
 ```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
& & A \\
Z_1 \arrow[r, "\sigma"] \arrow[urr, bend left, "f_1"] \arrow[drr, bend right, "g_1"'] & Z_2 \arrow[ur, "f_2"] \arrow[dr, "g_2"']& \\
 & & B
\end{tikzcd}
\end{document}
 ```
where the commutative requirement can be read as $f_1 = f_2 \sigma$ and $g_1 = g_2 \sigma$.

# Fibered Slice Categories

Finally, we consider a fibered variant $\tC_{\alpha, \beta}$ of the slice categories above where we fix two morphisms $\alpha: A \to C$ and $\beta: B \to C$.
 - $\Obj(\tC_{\alpha, \beta}):$ The objects are now commutative diagrams 
 ```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
& A \arrow[dr, "\alpha"]& \\
Z \arrow[ur, "f"] \arrow[dr, "g"'] & & C\\
& B \arrow[ur, "\beta"']& \\
\end{tikzcd}
\end{document}
 ```
in $\tC$.
 - $\Hom_{\tC_{\alpha, \beta}}:$ The homsets are also certain commutative diagrams
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
& & A \arrow[dr, "\alpha"]& \\
Z_1 \arrow[r, "\sigma"] \arrow[urr, bend left, "f_2"] \arrow[drr, bend right, "g_2"'] &Z_2 \arrow[ur, "f_2"] \arrow[dr, "g_2"'] & & C\\
& & B \arrow[ur, "\beta"']& \\
\end{tikzcd}
\end{document}
 ```
 in $\tC$.