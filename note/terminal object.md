<div class="topSpace"></div>

Date Created: {{date::DD/MM/YYYY}}
References: Riehl/CatCont
Tags: #Type/Definition #Topic/CategoryTheory

Proved By: <i>Not Applicable</i>
Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: <i>Not Applicable</i>

```ad-Definition
title: Definition (Initial and Final Objects).
Let $\mathtt{C}$ be a [[category|category]].
- An object $i \in \ob \mathtt{C}$ is called <u>initial</u> if there is a unique morphism $i \to c$ for all other $c \in \ob \mathtt{C}$.
- An object $f \in \ob \mathtt{C}$ is called <u>final</u> (or terminal) if there is a unique morphism $c \to f$ for all other $c \in \ob \mathtt{C}$.
- An object $o \in \ob \mathtt{C}$ which is both initial and final is called <u>zero object</u>.
```

_Examples_

1. The empty set $\emptyset$ is initial and any singleton $\{\ast\}$ is final in the category of [[set|sets]].
2. In $\Grp$ and $\Mod_R$, the trivial objects are zero objects.
3. In $\Ring$, the zero ring $\{0\}$ is final and $\mathbb{Z}$ is initial.
4. Since there are no homomorphisms between [[field|fields]] of different [[characteristic|characteristic]], $\Fld$ has no initial or final objects.
5. In the [[order#preorder|poset category]] $(\mathbb{Z}, \leq)$, $0$ is initial, but there exist no final objects.
