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
<i>.</i><span style="float:right;">$\blacksquare$</span>