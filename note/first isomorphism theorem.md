<div class="topSpace"></div>

Date Created: 27th March 2025
References: #Ref/Aluffi 
Tags: #Type/Theorem 

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Canonical Decomposition of [[set-function|Functions]]

``` ad-Theorem
title: Theorem (Canonical Decomposition).

Let $f:A \to B$ be a function. We define an [[relation#Equivalence Relation|equivalence relation]] on $A$ by
$$
a' \sim a'' :\iff f(a') \sim f(a'').
$$
Then $f$ decomposes into $$f = \iota \circ \widetilde{f} \circ \pi$$
where $\pi:A \twoheadrightarrow A/_\sim$ is the [[relation#Equivalence Relation|canonical projection]], $\iota: \im(f) \hookrightarrow B$ is the [[set-function|canonical inclusion]] and $\widetilde{f}: A/_\sim \to \im (f)$ is a bijection defined by $\widetilde{f}([a]_\sim):=f(a)$.
```
This is equivalent to the following commuting diagram:
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
A \arrow[d, twoheadrightarrow, "\pi"] \arrow[r, "f"] & B\\
A/_\sim \arrow[r,"\widetilde{f}", "\cong"'] & im(f) \arrow[u, hookrightarrow, "\iota"]
\end{tikzcd}
\end{document}
```
**Proof.**
$\widetilde{f}$ is well defined: If $a' \sim a''$ we also have $f(a') = f(a'')$ by construction. Therefore, the value of $\widetilde{f}$ does not depend on a chosen representative of an equivalence class $[a]_\sim$.
$\widetilde(f)$ is bijective: $\widetilde{f}([a'])=\widetilde{f}([a''])$ implies  $f(a')=f(a'')$ by definition, which in turn implies $[a']=[a'']$. Therefore, $\widetilde{f}$ is injective. For any $b \in \im(f)$, there is $a \in A$ with $f(a)=b$. By construction, $f(a) = \widetilde{f}([a]) = b$. Henceforth, $f$ is also surjective since $a$ was arbitrarily chosen. <span style="float:right;">$\blacksquare$</span>

**Example.**
The function given by
$$
\begin{align*}
f: \R &\to \C\\
r &\mapsto \exp(2\pi i r)
\end{align*}
$$
is obviously not bijective. We define $\sim$ on $\R$ by $r_1 \sim r_2 :\iff \exp(2\pi ir_1) = \exp(2 \pi i r_2)$. Rearranging yields
$$
\exp(2 \pi i (r_2-r_1)) = 1 \iff r_1 = kr_2, k \in \Z \iff r_1-kr_2 \in \Z
$$
for arbitrary integers $k$. Therefore, we identify all reals by their integer distances. We have [[relation#Equivalence Relation|already seen]] that $\R/_\sim \cong \S^1$. The canonical decomposition is given by
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[scale=3]
R \arrow[d, twoheadrightarrow, "\pi"] \arrow[r, "f"] & C \\
S \arrow[r,"id", "\cong"'] & S \arrow[u, hookrightarrow, "\iota"]
\end{tikzcd}
\end{document}
```