<div class="topSpace"></div>

Date Created: {{date::DD/MM/YYYY}}
References: Riehl/CatCont
Tags: #Topic/CategoryTheory #Type/Definition

Proved By: <i>Not Applicable</i>
Specializations: <i>Not Applicable</i>
Generalizations: [[limit]]
Examples: <i>Not Applicable</i>

```ad-Definition
title: Definition (Product and Coproduct).
Let $\mathcal{F}: \mathtt{J} \to \mathtt{C}$ be a [[diagram|diagram]] indexed over a discrete category $\mathtt{J}$.
- The <u>product</u>  of $\mathcal{F}$ is defined as the [[limit|limit]] $$\prod_{j \in \mathtt{J}} \mathcal{F} := \lim_\mathtt{J} \mathcal{F}.$$
- The <u>coproduct</u>  of $\mathcal{F}$ is defined as the [[limit|colimit]] $$\coprod_{j \in \mathtt{J}} \mathcal{F} := \colim_\mathtt{J} \mathcal{F}.$$
```

The product has legs called <u>canonical projections</u>

$$
\left( \pi_k: \prod_{j \in \mathtt{J}} \mathcal{F}_j \to \mathcal{F}_k \right)_{k \in \mathtt{J}}.
$$

The coproduct has legs called <u>canonical injections</u>

$$
\left( \iota_k: \mathcal{F}_k \to \coprod_{j \in \mathtt{J}} \mathcal{F}_j \right)_{k \in \mathtt{J}}.
$$

## Cartesian Product

```ad-Definition
title: Definition (Cartesian Product).
A product in $\Set$ is called <u>cartesian product</u>.
```

The universal property is as follows: Given sets $X,Y$ and their product $X \times Y$ together with another set $Z$ and maps $f: Z \to X$ and $g:Z\to Y$, there is a unique map $f \times g: Z \to X \times Y$ making the following diagram commute:

```tikz
\usepackage{amsmath,amssymb,pgfplots, amstext, amsfonts, tikz-cd}
\usetikzlibrary{decorations.pathreplacing}
\begin{document}
\tikzset{every picture/.style={line width=0.75pt}} %set default line width to 0.75pt
\begin{tikzcd}[x=0.75pt,y=0.75pt,yscale=-0.5,xscale=0.5]
    & Z \ar[d, "f \times g"] \ar[ddl, "f"'] \ar[ddr, "g"]& \\
    & X \times Y \ar[dl, "\pi_X"] \ar[dr, "\pi_Y"']& \\
X & & Y
\end{tikzcd}
\end{document}
```

```

```
