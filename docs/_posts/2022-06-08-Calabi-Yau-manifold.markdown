---
layout: post
title:  "An Introduction to Calabi-Yau Manifolds"
date:   2022-06-08 10:53:37 -0000
categories: math, physics
---

## Complex manifolds
We first introduce complex manifolds.

### Almost complex structure
 First, the **almost complex structure**, it is a $(1,1)$ tensor field and at a point $p$ on the manifold, it defines a map $J_p : T_p M \to T_pM$. Moreover, it satisfy $J_p^2 = - {\rm id}_{T_p M}$. In complex coordinates, the components of $J_p$ take the canonical form
\begin{equation}
J_p = \begin{pmatrix} i I_m & 0 \\\\ 0 & - i I_m\end{pmatrix}
\end{equation}

### Almost complex manifolds
Let $M$ be a differentiable manifold. The pair $(M,J)$ is called an **almost complex manifold** if there exists a tensor field $J$ of type (1,1) such that at each point $p$ of $M$, $J_p^2 = - {\rm id}_{T_pM}$. The tensor field $J$ is also called the **almost complex structure**.

Let $(M,J)$ be an almost complex manifold. If the Lie bracket of any holomorphic vector fields $X,Y$ is again a holomorphic vector field, the almost complex structure $J$ is said to be **integrable**. We will see that this statement is equivalent to that the Nijenhuis tensor trivially vanishes. An integrable almost complex structure is called a **complex structure**.

### Nijenhuis tensor
Given any linear map $A$ on each tangent space of $M$, the **Nijenhuis tensor** is a tensor field of rank (1,2) given by
\begin{equation}
N_A(X,Y) = - A^2 [X,Y] + A[AX, Y] + A[X, AY] - [AX, AY]
\end{equation}

For the usual case of the almost complex structure $J$, the Nijenhuis tensor is given by
\begin{equation}
N(X,Y) = [X,Y] + J[JX, Y] + J[X, JY] - [JX, JY]
\end{equation}

<span style="color:blue">Exercise: derive the component of Nijenhuis tensor.</span>

### Complex manifold
If $M$ is a complex manifold, the complex structure $J$ is a constant tensor field and the Nijenhuis tensor field vanishes.

A theorem by Newlander and Nirenberg states that: Let $(M,J)$ be a $2m$-dimensional almost complex manifold. If $J$ is integrable, the manifold $M$ is a complex manifold with the almost complex structure $J$.

In summary we have all the following three are equivalent
- Integrable almost complex structure
- Vanishing Nijenhuis tensor field
- Complex manifold


### Hermitian manifolds
If a Riemannian metric $g$ of a complex manifold $M$ satisfies
\begin{equation}
g_p(J_p X, J_p Y) = g_p(X, Y)~.
\end{equation}
at each point $p \in M$ and for any $X, Y \in T_p M$, then $g$ is said to be an **Hermitian metric**. The pair $(M,g)$ is called a **Hermitian manifold**.

The vector $J_p X$ is orthogonal to $X$ with respect to a Hermitian metric,
\begin{equation}
g_p(J_pX, X) = g_p(J_p^2 X, J_p X) = - g_p(J_p X, X) = 0~.
\end{equation}

### Kahler form
Let $(M,g)$ be a Hermitian manifold. Define a tensor field $\Omega$ whose action on $X, Y \in T_p M$ is
\begin{equation}
\Omega_p(X,Y) = g_p(J_p X, Y)
\end{equation}
Note that $\Omega$ is anti-symmetric. Hence it defines a two-form called the **Kahler form** of a Hermitian metric $g$. We may write 
\begin{equation}
\Omega = i g_{\mu \bar{\nu}} dz^\mu \wedge d\bar{z}^\nu
\end{equation}

[comment]: <> ### Covariant derivatives

[comment]: <> ### Ricci form

### Kahler manifolds
A **Kahler manifold** is a Hermitian manifold $(M,g)$ whose Kahler form $\Omega$ is closed $d\Omega = 0$. The metric $g$ is called the **Kahler metric** of $M$.

From the definition
\begin{equation}
\begin{aligned}
(\partial + \bar{\partial}) &i g_{\mu \bar{\nu}}\, dz^\mu \wedge d\bar{z}^\nu \cr
& = i \partial_\lambda g_{\mu \bar{\nu}} \,dz^\lambda \wedge dz^\mu \wedge d \bar{z}^\nu + i \bar{\partial}\_{\bar{\lambda}} g_{\mu \bar{\nu}} \,d\bar{z}^\lambda \wedge dz^\mu \wedge d\bar{z}^\nu = 0
\end{aligned}
\end{equation}

from which we obtain
\begin{equation} 
\partial\_\lambda g\_{\mu \bar{\nu}} = \partial\_\mu g\_{\lambda \bar{\nu}}~, \quad \bar{\partial}\_{\bar{\lambda}} g\_{\mu \bar{\nu}} = \bar{\partial}\_{\bar{\nu}} g\_{\mu \bar{\lambda}}~.
\end{equation}

Suppose that a Hermitian metric $g$ is given on a chart $U_i$ by
\begin{equation} \label{eqn:kahler-potential}
g_{\mu \bar{\nu}} = \partial_\mu \bar{\partial}_{\bar{\nu}} \mathcal{K}_i
\end{equation}
Clearly it is a Kahler metric. Conversely, it can be shown that any Kahler metric is locally expressed as \eqref{eqn:kahler-potential}. It follows that $\Omega = i \partial \bar{\partial} \mathcal{K}\_i$ on $U_i$ 
