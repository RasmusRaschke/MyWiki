<div class="topSpace"></div>

Date Created: 20/09/24
References: 
Tags: #Type/Definition #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[smooth mapping]]

``` ad-Definition
title: Definition (Immersion, Submersion, Embedding).

Let $F: M \to N$ be a [[smooth mapping]] between [[manifold|smooth manifolds]] $M$ and $N$. $F$ is called
1. __immersion__ if $F_{\ast, p}: T_pM \to T_{F(p)}N$ is injective for all $p \in M$. This is equivalent to $$\text{rank \ } F = \dim M.$$ 
2. __submersion__ if $F_{\ast, p}: T_pM \to T_{F(p)}N$ is surjective for all $p \in M$. This is equivalent to $$\text{rank \ } F = \dim N.$$
3. __embedding__ if $F$ is an immersion and $F: M \to F(M) \sub N$ is a [[homeomorphism]].
```
**Remark.**
Embedding implies injective immersion, but injective immersion doesn't imply embedding.

**Examples.**
1.  Let $F: \R \to \R^2$ be defined as $F(t) := (\sin t, \sin 2t)$. $F$ is an immersion and injective on $(0,2\pi)$, but no embedding. However, for $\epsilon > 0$ $F$ is an embedding on (\epsilon, 2\pi - \epsilon)$ .
2.  Let $M = \Z$ and $N = \S^1 \cong \R \diagup \Z$. For $\alpha \in \R, \Q$ is $F_\alpha: \Z \to \S^1$, $k \mapsto \alpha k \mod 1$ an injective immersion, but no embedding because $F_\alpha (\Z) \sub \S^1$ lacks the [[discrete topology]].
3.  Any projection $\pi: \R^n \to L \sub \R^k$ onto a linear subspace of $\R^n$ along the orthogonal complement $L^\perp \sub \R^n$ is a submersion. All linear embeddings $A: \R^k \to \R^n$ are immersions.
4.  $F: \R^{n+1} \setminus \{0\} \to \R$ with $F(x) := \| x\|^2$ is a submersion because $\cD F_x(v) = 2 \langle x,v \rangle$.
5.  $G: \R^{n+1} \setminus \{0\} \to \S^n$ with $G(x) := \frac{x}{\|x\|^2}$ is also a submersion.