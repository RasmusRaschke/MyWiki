<div class="topSpace"></div>

Date Created: 09/04/25
References: #Ref/AlgTop 
Tags: #Type/Definition

Proved by: <i>Not Applicable</i>
References: [[chain complex]]
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

``` ad-Definition
title: Definition (Homology).

Let $C_\ast$ be a [[chain complex]]. The abelian group $$H_n(C):=Z_n(C)/B_n(C)$$ is called <ins>$n$-th homology group</ins> of $C_\ast$. The equivalence classes of $c \in Z_n(C)$ are called <ins>homology classes</ins> and denoted $[c] = c + B_n(C)$.
For $c,c'\in C_n$ satisfy $c-c' \in B_n(C)$, we call them <ins>homologous</ins> to each other.
```

We want to check that being homologous defines an [[relation#Equivalence Relation|equivalence relation]]:
 1. Since $c-c=0$ and $d_{n+1}$ is a homomorphism, the relation is reflexive.
 2. If $c$ is homologous to $c'$, we have $c-c'=d_{n+1}y$ and therefore $c'-c=-d_{n+1}y$. This makes the relation symmetric.
 3. Let $c,c',c'' \in C$ with $c-c'=d_{n+1}y$ and $c'-c'' = d_{n+1}z$. Then, $c-c'+c'-c'' = d_{n+1}y+d_{n+1}z = c-c''$. Hence, it is also transitive.

**Examples.**
 1. We consider $$C_n=\begin{cases} \Z \, &\text{if}\, n\in \{0,1\}\\ 0 \, &\text{otherwise} \end{cases}$$ and let $d_1$ be multiplication with $n \in \N$. The kernel of $d_0: \Z \to \{0\}$ is always $\Z$. The image of $d_1$ is $n\Z$. All other homology groups have trivial numerator and are therefore trivial: $$H_n(C)=\begin{cases} \Z /n\Z \, &\text{if}\, n=0\\ \{0\} \, &\text{otherwise.} \end{cases}$$
 2. Now, set $C_n=\Z$ for all $n$ and $$d_n=\begin{cases} \id_\Z \, &\text{if}\, n \, \text{is odd}\\ 0 \, &\text{otherwise.} \end{cases}$$ For even $n$, the kernel of $d_n$ is the whole group $\Z$. The image of $d_{n+1}$ is in this case also the whole group and we obtain trivial homology. If $n$ is odd, the kernel of $d_n$ consists only of $0$,  This is also true for the image of $d_{n+1}$ and we again obtain trivial homology: $$H_n(C) = \{0\}.$$
 3. Reconsider example 2. with $d_n = 0$ for all $n \in \Z$. The image is now $\{0\}$ and the kernel the whole group $\Z$. We obtain non-trivial homology $$H_n(C) = \Z.$$