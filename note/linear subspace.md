<div class="topSpace"></div>

Date Created: 
References: 
Tags: #Type/Definition

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[vector space]]
Examples: <i>Not Applicable</i>

# Linear Subspaces 

``` ad-Definition
title: Definition (Linear Subspace).

Let $V$ be a vector space. A subset $U \sub V$ is called __linear subspace__ if the following conditions are satisfied:
1. Additive identity: $0 \in U$
2. Closure under addition: $u, w \in U$ implies $u+v \in U$.
3. Closure under multiplication: $\lambda \in \F$ and $u \in U$ implies $\lambda u \in U$.

This means that a linear subspace is a vector space with the same additive identity, addition and scalar multiplication as $V$.
```

<i>Proof.</i>
We show that a linear subspace is indeed a vector space. If $U$ is a subspace of $V$, $U$ satisfies the three conditions by definition.
If $U$ satisfies the three conditions, the first condition ensures the existence of an additive identity. The second conditions guarantees the well-definedness of addition in $U$. The third condition does the same for scalar multiplication. If $u\in U$, $-u$ is also in $U$ because of the third condition. All other properties are trivially inherited from $V$. Thus $U$ is a vector space.
<span style="float:right;">$\blacksquare$</span>

**Examples.**
1. The set of continous real-valued functions on $[0,1]$ is a subspace of $\R^{[0,1]}$.
2. The set of differentiable real-valued functions on $\R$ is a subspace of $\R^\R$.
3. The set of differentiable real-valued functions $f$ on $(0,3)$ such that $f'(2)=b$ is a subspace of $\R^{(0,3)}$ iff $b=0$.
4. The set of zero sequences of complex numbers is a subspace of $\C^\infty$.
5. The set $\{0\}$ is the smallest subspace of a vector space $V$.


# Sum of Subspaces

``` ad-Definition
title: Definition (Sum of Subspaces).

Let $V$ be a [[vector space]] and $V_1, \dots, V_m$ be linear subspaces of $V$. The __sum of $V_1, \dots, V_m$__ is given by $$V_1 + \cdots + V_m := \{ v_1 + \cdots + v_m | \forall i \in \{1, \dots, m \}: v_i \in V_i\}.$$
```

**Examples.**
1. Define $U:=\{(x,0,0) \in \F^3 | x \in \F\}$ and $W:=\{(0,y,0) \in \F^3 | y \in \F\}$. Then, $$U+W = \{ (x,y,0) \in \F^3 | x,y \in \F \}.$$

``` ad-Proposition
title: Proposition (Sum is smallest containing Subspace).

Let $V_1, \dots, V_m$ be linear subspaces of $V$. Then $V_1 + \cdots + V_m$ is the smallest linear subspace of $V$ containing $V_1, \dots, V_m$.
```

<i>Proof.</i>
The sum $V_1 + \cdots + V_m$ containes the additive identity because $0$ can be obtained trivially by setting all entries of the sum $v_1 + \cdots + v_m$ to zero.  Moreover, it is closed under addition and multiplication. This makes $V_1 + \dots + V_m$ a subspace by definition. The subspaces $V_1, \dots, V_m$ are each contained in the sum which can be seen by setting all terms but one of the sum $v_1+ \cdots + v_m$ equal to $0$. Because subspaces are closed under addition, every subspace of $V$ containing $V_1, \dots, V_m$ also containes $V_1 + \cdots + V_m$. Thus the statement is proven.
<span style="float:right;">$\blacksquare$</span>

**Remark.**
Sums of subspaces are analogous to unions of sets. Given two subsets of a set, the smallest subset containing both subsets is their union.

``` ad-Definition
title: Definition (Direct Sum).

Let $V$ be a [[vector space]] and $V_1, \dots, V_m$ be linear subspaces of $V$. The sum of subspaces is called a __direct sum__, denoted $$V_1 \oplus \dots \oplus V_m,$$ if each $v \in V_1 + \cdots + V_m$ can be __uniquely__ decomposed into a sum $$v = v_1 + \cdots + v_m$$ with $v_i \in V_i$.
```

**Examples.**
1. Let $V_k$ be the subspace of $\F^n$ whose coordinates are all $0$, with exception of the $k$-th entry. Then, $$\F^n = V_1 \oplus \cdots \oplus V_n.$$ 


``` ad-Proposition
title: Proposition (Conditions of the Direct Sum).

Let $V_1, \dots, V_m, U, W$ be linear subspaces of $V$.

1. $V_1 + \cdots + V_m$ is a direct sum iff the equation $$0 = v_1 + \cdots + v_m$$ is only solved by $v_i = 0$ for all $i \in \{1, \dots, m\}$.
2. $U + W$ is a direct sum iff $$U \cap W = \{0\}.$$
```
<i>Proof.</i>
1. Suppose $V_1 + \cdots + V_m$ is a direct sum. Then $v_i = 0$ for all $i$ is implied by definition. Now suppose $0$ can only be written as $v_1 + \cdots + v_m$ if all $v_i = 0$. Let $w \in V_1 + \cdots + V_m$ and assume that it can be expressed in two distinct ways: $$w = w_1 + \cdots + w_m = w_1' + \cdots + w_m'.$$ Subtracting both equations yields $$0 = (w_1 - w_1') + \cdots + (w_m - w_m').$$ But every term $(w_i - w_i') \in V_i$ and therefore $w_i = w_i'$ for all $i$, as desired.
2. Suppose $U+W$ is a direct sum. For $v \in U \cap W$ we have $0 = v +(-v)$ with $v \in U$ and $-v \in W$. Because $0$ can be uniquely represented as a sum, we have $v=0$ and thus $U \cap W = \{0\}$. Now suppose $U \cap W = \{0\}$ and let $u \in U, w \in W$ be two vectors with $$0=u+w.$$ This implies $u = -w \in W$ and hence $u \in U \cap W$ which means $u = 0$. The equation then also implies $w = 0$, completing the proof.
<span style="float:right;">$\blacksquare$</span>