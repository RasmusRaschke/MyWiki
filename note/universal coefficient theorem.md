<div class="topSpace"></div>

Date Created: [[02/06/2025]]
References: #Ref/AlgTop 
Tags: #Type/Theorem #Topic/Algebra 

Proved by: [[Künneth formula]]
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

# Algebraic Version

``` ad-Theorem
title: Theorem (Universal Coefficient Theorem - Algebraic Version).
Let $C_\ast$ be a [[chain complex#Free Complexes|free chain complex]] and $G$ be an abelian group. For all $n \in \Z$, we have a [[short exact sequence#Of Abelian Groups|split short exact sequence]]
$$
0 \to H_n(C_\ast) \otimes G \to H_n(C_\ast \otimes G) \to \Tor(H_{n-1}(C_\ast), G) \to 0.
$$
Hence,
$$
H_n(C_\ast \otimes G) \cong H_n(C_\ast) \otimes G \oplus \Tor(H_{n-1}(C_\ast), G).
$$
```

# Topological Version

``` ad-Theorem
title: Theorem (Universal Coefficient Theorem - Topological Version).
For every [[topological space]] $X$ there is a [[short exact sequence|split short exact sequence]]
$$
0 \to H_n(X) \otimes G \to H_n(X;G) \to \Tor(H_{n-1}(X), G) \to 0.
$$
Hence,
$$
H_n(X;G) \cong H_n(X) \otimes G \oplus \Tor(H_{n-1}(X), G).
$$
```
**Example.**
Consider $X=\R P^2$. We obtain
$$
H_n(\R P^2; G) \cong H_n(\R P^2) \otimes G \oplus \Tor(H_{n-1}(\R P^2), G).
$$
This yields several statements:
$$
H_0(\R P^2; G) \cong H_0(\R P^2) \otimes G \oplus \Tor(0, G) \cong G
$$
and
$$
H_1(\R P^2; G) \cong H_1(\R P^2) \otimes G \oplus \Tor(H_0(\R P^2), G) \cong G/2G \oplus 0 \cong G / 2G
$$
as well as
$$
H_2(\R P^2; G) \cong H_2(\R P^2) \otimes G \oplus \Tor(H_1(\R P^2), G) \cong \Tor(\Z / 2\Z, G).
$$