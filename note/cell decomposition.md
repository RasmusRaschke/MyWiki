<div class="topSpace"></div>

Date Created: [[11/05/2025]]
References: #Ref/AlgTop 
Tags: #Type/Definition #Topic/AlgebraicTopology 

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Definition of an $n$-Cell

``` ad-Definition
title: Definition ($n$-Cell).
A [[topological space]] $X$ is called an <ins>$n$-cell</ins> if it is homeomorphic to $\R^n$. 

```

**Examples.**
1. Every point is a $0$-cell.
2. $\mathring{\D}^n \cong \R^n \cong \S^n \setminus N$ are $n$-cells.

**Remark.**
An $n$-cell can never also be an $m$-cell for $n \neq m$ as $\R^n \cancel{\cong} \R^m$.

# Cell Decomposition

``` ad-Definition
title: Definition (Cell Decomposition).
A <ins>cell decomposition</ins> of a [[topological space]] $X$ is a decomposition of $X$ into $n$-cells of some dimensions:
$$
X = \coprod_{i \in I} X_i, \ X_i \cong \R^{n_i}.
$$
This decomposition is a decomposition of [[set|sets]], not of topological spaces.
```

**Examples.**
1. A hollow cube in $\R^3$ can be decomposed into 8 $0$-cells, $12$ $1$-cells (open edges) and $6$ $2$-cells (open faces). 
2. The [[simplex|standard $3$-simplex]] can be decomposed into $4$ $0$-cells, $6$ $1$-cells, $4$ $2$-cells and a $3$-cell.
3. [[sphere|The $n$-sphere]] can be decomposed into its north pole and the complement.