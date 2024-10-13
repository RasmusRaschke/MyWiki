<div class="topSpace"></div>

Date Created: [[2024-08-28]]
References: #Ref/LinAlg
Tags: #Type/Definition #Topic/LinearAlgebra

Proved by:<i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Vector Space).

A __vector space over a field__ is a pair $(V,\F)$, consisting of a set $V$ and a field $\F$, called scalar field, with an addition $+$ and a scalar multiplication $\cdot$, that obey the following laws:
1. commutativity: $u+v = v+u$ for all $u,v \in V$
2. associativity: $(u+v)+w = u+(v+w)$ for all $u,v,w \in V$ and $a(bv) = (ab) v$ for all $a,b \in \F, v \in V$
3. additive identitiy: $\exists 0 \in V: \forall v\in V: v+0 = v$
4. additive inverse: $\forall v \in V \exists w \in V: v+w=0$
5. multiplicative identity: $\exists 1 \in V: \forall v \in V: 1v=v$
6. distributive law: $a(u+v)=au+av$ and $(a+b)v=av+bv$ for all $u,v \in V, a,b \in \F$

Elements of $V$ are called __vectors__, elements in $\F$ scalars.
A vector space over $\R$ is called __real vector space__, a vector space over $\C$ __complex vector space__.
```

**Examples.**
1. The simplest vector space is given by $\{0\}$. It containes only one point.
2. The set of sequences of elements of $\F$, given by $$\F^\infty := \{(x_1, x_2, \dots) | \forall k \in \Z: \ x_k \in \F\}$$ is a vector space over $\F$. Addition and multiplication are defined element-wise: $$(x_1, x_2, \dots) + (y_1, y_2, \dots)   = (x_1+y_1, x_2 + y_2, \dots)$$ $$\lambda (x_1, x_2, \dots) = (\lambda \cdot x_1, \lambda \cdot x_2, \dots).$$ The additive identitiy is the zero sequence.
3. The set $\F^S$ of functions $f: S \to \F$ is a vector space over $\F$ if $S \neq \emptyset$ with pointwise addition $$(f+g)(x) := f(x)+g(x)$$ and pointwise multiplication $$(\lambda f)(x):=\lambda \cdot f(x)$$ for all $x \in S$ and $f \in \F^S$. The additive identity is given by the zero function $0: S \to \F$ with $0(x) = 0$ for all $x \in S$. The additive inverse of $f \in \F^S$ is given by $-f: S \to \F$ with $$(-f)(x) = -f(x)$$ for all $x \in S$.
4. The vector space $\F^n$ is a special case of $\F^\infty$ considering that $(x_1, \dots, x_n) = (x(1), \dots, x(n))$ can be thought of as a function $x: \{1, 2, \dots, n\} \to \F$.

# Elementary properties

``` ad-Proposition
title: Proposition (Elementary Properties of Vector Spaces).

Let $V$ be a vector space. Then the following statements are true:
1. $V$ has a unique additive identity.
2. For every $v \in V$ exists a unique additive inverse in $V$, denoted $-v$.
3. $0v = 0$ for all $v \in V$ and $\lambda 0 = 0$ for all $\lambda \in \F$.
4. $(-1)v = -v$ for all $v \in V$.

```
<i>Proof.</i>
1. Let $0, 0' \in V$ be two additive identities. Then we have $$0 = 0 + 0' = 0' + 0 = 0'$$ and therefore $0 = 0'$.
2. Let $v \in V$ and suppose that $w, w' \in V$ are additive identities of $v$. Then we have $$w = w + 0 = w + (v+w') = (w +v) + w'  = 0 + w' = w'$$ and therefore $w = w'$.
3. Let $v \in V$. We have $$0v = (0+0)v = 0v + 0v \iff 0v + (-0v) = 0v + 0v + (-0v) \iff 0 = 0v.$$  Let $\lambda \in \F$. Then, $$\lambda 0 = \lambda (0+0) = \lambda 0 + \lambda 0.$$ By the same argument, $0 = \lambda 0$.
4. Let $v \in V$. We have $$v + (-1)v = 1v + (-1)v = (1+ (-1)) v = 0v = 0 \iff (-1)v = -v.$$
<span style="float:right;">$\blacksquare$</span>