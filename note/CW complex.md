<div class="topSpace"></div>

Date Created: [[12/05/2025]]
References: #Ref/AlgTop 
Tags: #Type/Definition #Topic/AlgebraicTopology 

Proved by: <i>Not Applicable</i>
References: [[cell decomposition]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Objects

``` ad-Definition
title: Definition (CW Complex).
A [[topological space]] $X$ which is Hausdorff is called a <ins>$CW$ complex</ins> if it has a [[cell decomposition]] with the following properties:
1. For every $n$-cell $\sigma \sub X$ there is a continuous map $$\Psi_\sigma: \D^n \to X,$$ called <ins>characteristic map</ins> of $\sigma$, such that the restriction $\Psi_\sigma|_{\mathring{\D}^n}: \mathring{\D}^n \cong \sigma$ is a homeomorphism and $\Psi_\sigma$ maps $\S^{n-1}$ to the union of cells of dimension not higher than $n-1$. The restriction is called <ins>attaching map</ins>.
2. <ins>Closure finite condition</ins>: For every $n$-cell $\sigma$, the closure $\overline{\sigma} \sub X$ has non-trivial intersection only with finitely many cells of $X$.
3. <ins>Weak topology</ins>: A subset $A\sub X$ is closed iff $A \cap \overline{\sigma}$ is closed for all cells $\sigma \sub X$.

If there are only finitely many cells, $X$ is called <ins>finite</ins>.
```

**Example.**
The unit interval $[0,1]$ can be decomposed into two $0$-cells and one $1$-cell. However, the decomposition $\sigma_0^0=\{0\},$ $\sigma_k^0 = \left\{ \frac{1}{k}\right\}$ for $k >0$ and $\sigma_k^1 = \left( \frac{1}{k+1}, \frac{1}{k}\right)$ does not work. For instance, 
$$
A:= \left\{\frac{1}{2} \left(\frac{1}{k}+\frac{1}{k+1} \right) \mid k \in \N\right\} \sub [0,1]
$$
has intersection $A \cap \overline{\sigma}_k^1 = \frac{1}{2} \left( \frac{1}{k} + \frac{1}{k+1}\right)$ which is a single, closed point, while $A$ is not.

**Remark.**
CW structures are not unique: One can consider $\S^2$ with the CW structure induced by the decomposition $\S^2 = \S^2 \setminus N \sqcup N$, yielding a $0$-skeleton consisting of the north pole $N$ which agrees with the $1$-skeleton, but the $2$-skeleton is equal to $\S^2$. However, one can also take some hollow polyhedron like a tetrahedron or a cube and project them onto $\S^2$, yielding a different CW structure.


## Subcomplexes

``` ad-Definition
title: Definition (Sub-$CW$ Complex and Pairs).
Let $X$ be a CW complex and $Y \sub X$. $Y$ is called <ins>sub-CW complex</ins> if it has a [[cell decomposition]] by cells in $X$ and for any cell $\sigma \sub Y$ we have $\overline{\sigma} \sub Y$.
In general, a subset $A \sub X$ gives rise to a <ins>CW-pair</ins> $(X,A)$.
```

**Remark.**
A sub-CW complex of a CW complex is again a CW complex: The characteristic maps stay the same for the subcomplex. $Y$ is closed in $X$ because of the closure finite condition, guaranteeing that $Y$ has the weak topology. If $\overline{\sigma} \sub X$ and $\sigma \sub Y$, we know that $\overline{\sigma} \sub Y.$ Because $Y$ is closed, axiom 2. is satisfied.

## Skeleta

``` ad-Definition
title: Definition ($n$-Skeleton).
Let $X$ be a CW-complex. We call $$X^n := \bigcup_{\sigma \sub X, \, \dim(\sigma)\leq n} \sigma$$ the <ins>$n$-skeleton</ins> of $X$.
If $X=X^n$ but $X^{n-1} \subset X$ we say $X$ is $n$-dimensional, $\dim(X)=n$.
```

## Weak Topology

Cells do not have to be open in $X$: If $X$ is a CW complex and $\sigma$ is an $n$-cell, $\sigma$ is open in the $n$-skeleton $X^n$ but $X^n$ is closed in $X$. As a set, $X$ is given by $X=\cup_{n \geq 0} X^n$. Since $A$ is closed in $X$ if and only if the intersection with any $\overline{\sigma}$ is closed, $A$ is closed if and only if $A \cap X^n$ is closed for all $n \geq 0$. This is an instance of a [[direct limit|direct limit topology]] $X=\varinjlim X^n$ with the following [[universal properties|universal property]]:
For any family of continuous maps $(f_n: X^n \to Z)_{n \geq 0}$ such that $f_{n+1}|_{X^n}=f_n$ there is a unique continuous map $f:X \to Z$ such that $f_{X^n} =f_n$.
```tikz
\usepackage{tikz-cd}
\usepackage{amsmath, amstext, amssymb, amsfonts}
\begin{document}
\begin{tikzcd}[scale=3]
X \ar[r, "\iota_n"] \ar[dr, "f|_{X^n}"']& X^n \ar[d, "f_n"]\\
& Z
\end{tikzcd}
\end{document}
```


# Morphisms

``` ad-Definition
title: Definition (Cellular Maps).
Let $X$ and $Y$ be CW complexes. A continuous map $$f: X \to Y$$ is called <ins>cellular</ins> if $f(X^n) \sub Y^n$ for all $n\geq 0$.

```

# Category

``` ad-Definition
title: Definition (Category of CW complexes).
The [[category]] $\CW$ consists of CW complexes as objects and cellular maps as morphisms.

```