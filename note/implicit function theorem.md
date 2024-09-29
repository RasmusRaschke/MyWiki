<div class="topSpace"></div>

Date Created: 16/12/2023 18:21:37
References: #Ref/Ana2
Tags: #Type/Theorem #Topic/RealAnalysis #Topic/DifferentialGeometry 

Proved by: <i>Not Applicable</i>
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: [[constant rank theorem]]

``` ad-Theorem
title: Theorem (Implicit Function Theorem).

Let $U_1 \sub \R^k$ and $U_2 \sub \R^m$ be two open subsets and $$F: U_1 \times U_2 \to \R^m$$ $$(x,y) \mapsto F(x,y)$$ be a continously differentiable function. Let $(a,b) \in U_1 \times U_2$ be a point for which $F(a,b) = 0$ holds.
Let the $m \times m$ matrix $$\frac{\partial F}{\partial y} := \frac{\partial (F_1, \dots, F_m)}{\partial (y_1, \dots, y_m)} := \begin{pmatrix} \frac{\partial F_1}{\partial y_1} & \cdots & \frac{\partial F_1}{\partial y_m} \\ \vdots & \ddots & \vdots \\ \frac{\partial F_m}{\partial y_1} & \cdots & \frac{\partial F_m}{\partial y_m} \end{pmatrix}$$ be invertible at $(a,b)$.
Then there exists an open neighbourhood $V_1 \sub U_1$ of $a$, $V_2 \sub U_2$ of $b$ and a continously differentiable function $$g: V_1 \to V_2 \sub \R^m$$ with $g(a)=b$ such that $$F(x, g(x)) = 0$$ for all $x \in V_1$.
If $F(x,y)=0$ holds for $(x,y) \in V_1 \times V_2$, $y = g(x)$ is implied.
```

<i>Proof.</i> TBD<span style="float:right;">$\blacksquare$</span>
