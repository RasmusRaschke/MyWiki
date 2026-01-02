<div class="topSpace"></div>

Date Created: {{date::DD/MM/YYYY}}
References: Riehl/CatCont
Tags: #Type/Definition #Topic/CategoryTheory

Proved By: <i>Not Applicable</i>
Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>
Examples: [[homotopy#homotopy group]]

```ad-Definition
title: Definition (Functor).
Let $\mathtt{C}, \mathtt{D}$ be [[category|categories]]. A <u>covariant functor</u> $$\mathcal{F}: \mathtt{C} \to \mathtt{D}$$ assigns to every $a \in \ob \mathtt{C}$ an object $\mathcal{F}a \in \ob \mathtt{D}$ and to every morphism $f: a \to b$ in $\mathtt{C}$ a morphism $\mathcal{F}f: \mathcal{F}a \to \mathcal{F}b$ in $\mathtt{D}$ such that:
- For any $a \overset{f}\to b \overset{g}\to c$ in $\mathtt{C}$, we have $$\mathcal{F}(gf)=\mathcal{F}g \mathcal{F}f.$$
- For any $x \in \ob \mathtt{C}$, we have $\mathcal{F}1_x = 1_{\mathcal{F}x}$.

A <u>contravariant functor</u> $\mathcal{G}: \mathtt{C} \to \mathtt{D}$ is a covariant functor $\mathtt{C}^\op \to \mathtt{D}$, hence any morphism $a \overset{f}\to b$ is assignd to a morphism $\mathcal{G}b \overset{\mathcal{G}f}\to \mathcal{G}a$ and the composition rule is given by $$\mathcal{G}(gf)=\mathcal{G}f \mathcal{G}g.$$

A functor $\mathcal{F}: \mathtt{C} \to \mathtt{C}$ is called <u>endofunctor</u>.
```

_Examples_

1. The <u>forgetful functor</u> is a functor $$U: (-) \to \Set$$ whose codomain is $\Set$. It takes some [[category|category]] as domain, e.g. $\Grp$ or $\Ring$, and forgets any additional structure defined on it. Intermediate forgetful functors just forget some part of a given structure, e.g. $U: \Mod_R \to \AGrp$.
2. Given a [[set|set]] $S$, there is a functor $\mathcal{F}: \Set \to \Grp$ assigning a set $S$ to its [[free group|free group]] $\mathcal{F}S$.
3. There is a covariant endofunctor $\mathcal{P}: \Set \to \Set$ which assigns any set $S$ to its [[power set|power set]] $\mathcal{P}S$ and any function $f: X \to Y$ to its direct-image function $\overline{f}: \mathcal{P}X \to \mathcal{P}Y$ that sends $X' \subseteq X$ to $Y' \subseteq Y$. Similarly, there is a contravariant functor $\mathcal{P}: \Set^\op \to \Set$ sending $f: X \to Y$ to the inverse-image function $f^{-1}: \mathcal{P}Y \to \mathcal{P}X$ that sends $Y' \subseteq Y$ to $f^{-1}(Y') \subseteq X$.

# Representation

```ad-Definition
title: Definition (Represented Functor).
Let $\mathtt{C}$ be a [[category|locally small category]]. For any $c \in \ob \mathtt{C}$, we define a <u>covariant functor represented by $c$</u> by $$\mathtt{C}(c,-): \mathtt{C} \to \Set$$ $$(x \overset{f}\to y) \mapsto \mathtt{C}(c,x) \overset{f_\ast}\to \mathtt{C}(c,y)$$ where $f_\ast$ is post-composition with $f$.
Similarly, we define a <u>contravariant functor represented by $c$</u> by $$\mathtt{C}(-,c): \mathtt{C}^\op \to \Set$$ $$(x \overset{f} y) \mapsto \mathtt{C}(x,c) \overset{f^\ast}\gets \mathtt{C}(y,c)$$ where $f^\ast$ is pre-composition with $f$.
```
