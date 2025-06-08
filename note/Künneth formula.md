<div class="topSpace"></div>

Date Created: [[02/06/2025]]
References: #Ref/AlgTop 
Tags: #Type/Theorem #Topic/Algebra 

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: [[universal coefficient theorem]]

``` ad-Theorem
title: Theorem (Künneth Formula).
Let $\cC_\ast$ be a [[chain complex#Free Complexes|free chain complex]] and $C_\ast'$ be an arbitrary [[chain complex]]. For every $n \in \Z$ there is a [[short exact sequence|split short exact sequence]]
$$
0 \to \bigoplus_{p+q=n} H_p(\cC_\ast) \otimes H_q (C_\ast') \overset{\lambda}\to H_n(\cC_\ast \otimes C_\ast') \to \bigoplus_{p+q=n-1} \Tor(H_p(\cC_\ast), H_q(C_\ast')) \to 0
$$
yielding
$$
H_n(\cC_\ast \otimes C_\ast') \cong \left(\bigoplus_{p+q=n} H_p(\cC_\ast) \otimes H_q (C_\ast')\right) \oplus \left(\bigoplus_{p+q=n-1} \Tor(H_p(\cC_\ast), H_q(C_\ast'))\right).
$$
The map
$$
\lambda: \bigoplus_{p+q=n} H_p(\cC_\ast) \otimes H_q (C_\ast') \to H_n(\cC_\ast \otimes C_\ast')
$$
is given on the summand with index $(p,q)$ as 
$$
\lambda([c_p] \otimes [c_q']) := [c_p \otimes c_q']
$$
for $c_p \in \cC_p$ and $c_q' \in C_q'$.
```
To prove this theorem, we need a lemma:

``` ad-Proposition
title: Lemma (Trivial Chain Isomorphism).
Let $\cC_\ast$ be a [[chain complex#Free Complexes|free chain complex]] with trivial differential and let $C_\ast'$ be any [[chain complex]]. There is an [[isomorphism]]
$$
\lambda: \bigoplus_{p+q=n} H_p(\cC_\ast) \otimes H_q(C_\ast') \overset{\cong}\to H_n(\cC_\ast \otimes C_\ast').
$$
```
 *Proof.*
 