---
layout: post
title:  "Quantum cohomology ring"
date:   2022-04-21 11:11:37 -0000
categories: physics
---

In this article, I want to talk about this paper, [Summing the instantons: Quantum cohomology and mirror symmetry in toric varieties](https://arxiv.org/abs/hep-th/9412236). Witten introduced gauged linear sigma models (GLSMs) in his famous paper [Phases of N=2 theories in two dimensions](https://arxiv.org/abs/hep-th/9301042). We can calculate the instanton expansions for correlation function in topological sigma models with target space
- a toric variety $V$
- a Calabi-Yau hypersurface $M \subset V$

And this will lead to a notion of [quantum cohomology](https://en.wikipedia.org/wiki/Quantum_cohomology).

## $\mathcal{N} = 2$ Nonlinear sigma models
The nonlinear sigma model is given by a map $\Phi: \Sigma \to X$, where $\Sigma$ is a Riemann surface and $X$ is the target manifold. We can perform topological A-twist and **the space of operators in the topological nonlinear sigma model is the total de Rham cohomology $H^*_{dR}(X)$**. 

One can choose representative of these classes dual to homology cycles $H$ on $X$ as having delta-function support on $H$, and denote them by $\mathcal{O}_H$.

The classical action is $S_{\rm cl} = \int_\Sigma \Phi^*(J)$ where $J$ is the Kähler form on $X$. Then the path integral of the correlation function reduces to a sum over homotopoy classes of maps, weighted by $e^{2\pi i S_{\rm cl}}$, of integrals over the finite-dimensional moduli space of holomorphic maps in a given homotopy class.

When $H_1(X, \mathbb{Z}) = 0$, we can label each instanton sector by the homology class $h$ in $H_2(X, \mathbb{Z})$ of the image of any of the corresponding maps. The virtual dimension of the "sector $h$" moduli space $\mathcal{M}\_h$ is $d\_h = d - K \cdot h$ where $K$ is the canonical class of $X$ and $d = {\rm dim}_{\mathbb{C}} X$.

Let us consider a given correlation function
\begin{equation}
\langle \mathcal{O}\_{H\_1}(z\_1) \cdots \mathcal{O}\_{H\_s}(z\_s)\rangle
\end{equation}
for $z_1, \cdots, z_s$ generic points on $\Sigma$ and $H_i$ homology cycles of codimension $q_i$. **The contributions to this correlator from the various instanton sectors are referred to as [_Gromov-Witten invariants_](https://en.wikipedia.org/wiki/Gromov%E2%80%93Witten_invariant)**. The contribution from $\mathcal{M}_h$ vanishes unless $d_h = \sum q_i$.

We can use the three-point functions to define a "**quantum product**" turning the vector space $H^*(X, \mathbb{C})$ into an associative, super-commutative algebra.

We define the product $\mathcal{O}_1 * \mathcal{O}_2$ in this algebra by using the  nondegenerate pairing: it is the unique element satisfying
\begin{equation}
\langle (\mathcal{O}\_1 * \mathcal{O}\_2)(z) \mathcal{O}\_3(w) \rangle = \langle  \mathcal{O}\_1(z_1) \mathcal{O}\_2(z_2) \mathcal{O}\_3(z_3)\rangle
\end{equation}

This algebra has some additional structure which makes it into a **Frobenius algebra**. This means that the algebra (A) has a multiplicative identity element and that there is a linear functional $\epsilon: A \to \mathbb{C}$ such that the induced bilinear pairing $(x,y) \mapsto \epsilon(x * y)$ is nondegenerate. We will call this functional $\epsilon$ an **expectation function**.

The cohomology of a compact manifold $X$ has the structure of a graded Frobenius algebra, with multiplication given by cup product, identity given by the standard generator of $H^0(X)$, and a graded expectation function given by "evaluation on the fundamental class". 

The **quantum cohomology** algebra of $X$ is also a Frobenius algebra, more or less by definition: the correlator gives an expectation function, and the product is defined with the aid of this function. The multiplicative identity is again provided by the standard generator of $H^0(X)$.

The correlator is expected to converge for ${\rm Im}(J)$ deep in the interior of the Kähler cone. Note that for such $J$, ${\rm Im}(S_{\rm cl})$ can be made arbitrarily large for any nontrivial class $h$, so the series collapses in the limit onto its first term, determined by _constant_ maps.

So the quantum cohomology algebra is a deformation of the classical cohomology algebra of $X$, reducing to the latter for appropriate limiting values of $J$.

This deformation however is nontrivial. In general the nilpotent, $\mathbb{Z}$-graded cohomology algebra $H^*(X)$ is deformed into an algebra which is not nilpotent and which has at most a $\mathbb{Z}_p$-grading for some integer $p$. In the Calabi-Yau case, however, where $K = 0$, the quantum cohomology algebra is actually $\mathbb{Z}$-graded and nilpotent.

The correlation functions determine the ring structure. They can also be used to specify a presentation of the ring in terms of generators and relations. For example, if we have a set of generators $\mathcal{O}\_1, \cdots, \mathcal{O}_N$ for the even cohomology of the space $X$ then nondegeneracy of the two-point function implies that the (even part of the) quantum cohomology ring takes the form
\begin{equation}
\mathcal{R} = \mathbb{C}[\mathcal{O}\_1, \cdots, \mathcal{O}\_N]/ \mathcal{J}
\end{equation}
where
\begin{equation}
\mathcal{J} = \\{\mathcal{P} \in \mathbb{C}[\mathcal{O}\_1, \cdots, \mathcal{O}\_N]\, | \,\langle \mathcal{O} \mathcal{P}\rangle = 0 \quad \forall \mathcal{O}\\}
\end{equation}

More generally, given any associative algebra $A$ with multiplicative identity, and any linear functional $\varphi$ on $A$, the kernel of the bilinear form $(x,y) \mapsto \varphi(x * y)$ is an ideal $\mathcal{J}\_\varphi$, and the quotient ring $A/\mathcal{J}\_\varphi$ is a Frobenius algebra with expectation function induced by $\varphi$. 

If $A$ is itself a Frobenius algebra with an expectation function $\epsilon$, then by a theorem of [Nakayama](https://doi.org/10.2307/1968946), $\varphi$ takes the form $\varphi(x) = \epsilon(\alpha * x)$ for some fixed element $\alpha \in A$, and $\mathcal{J}\_\varphi$ coincides with the annihilator of $\alpha$.

Although the correlation functions determine the ring structure, the opposite does not hold in general: there can be many expectation functions on a given algebra. However, **if $A$ is a graded Frobenius algebra of finite length and all elements of $A$ have non-negative degree, then the graded expectation functions on $A$ are in one-to-one correspondence with degree 0 elements of $A$ which are not zero-divisors.

## The linear sigma model for $V$
We will present a GLSM whose low-energy limit is the nonlinear sigma model with target space a toric variety $V$.

### Toric varieties on one leg
A toric variety is a natural generalization of projective space. Just as $\mathbb{P}^d$ can be described in the form
\begin{equation}
\mathbb{P}^d = (\mathbb{C}^{d+1} - \\{0\\})/ \mathbb{C}^*
\end{equation}
A general $d$-dimensional toric variety $V$ can be considered as a quotient space
\begin{equation}
V\_\Delta = (Y - F\_\Delta) / T\_\Delta
\end{equation}
with $Y = \mathbb{C}^n$, $T\_\Delta \sim \mathbb{C}^{*(n-d)}$ acting diagonally on the coordinates of $Y$ as
\begin{equation}
g\_a(\lambda): x\_i \to \lambda^{Q\_i^a} x\_i \quad a = 1, \dots, (n-d), \quad i = 1, \dots, n
\end{equation}

and $F\_\Delta$ a subset of $Y-\mathbb{C}^{*n}$ which is a union of certain intersections of coordinate hyperplanes. We often call this a **holomorphic quotient** construction of $V\_\Delta$ to emphasize the holomorphic nature of the group $T\_\Delta$ and its representation on $Y$. We will restrict to the cases where $V$ is smooth, compact, and irreducible.
<hr>
- Example 1

    The simplest possible example is the complex projective space $\mathbb{P}^4$. Here $Y = \mathbb{C}^5$, $F = \\{0\\}$ and $T = \mathbb{C}^*$ acts on the standard coordinates in $Y$ as
    \begin{equation}
    g(\lambda): (x_1, x_2, x_3, x_4, x_5) \mapsto (\lambda x_1, \lambda x_2, \lambda x_3, \lambda x_4, \lambda x_5)
    \end{equation}

- Example 2

    The second toric variety is obtained by resolving the curve of $\mathbb{Z}_2$ singularities in the weighted projective space $\mathbb{P}\_4^{1,1,2,2,2}$. Each point on the curve is blown up to a $\mathbb{P}^1$. We have $Y = \mathbb{C}^6$,
    \begin{equation}
    F = \\{x_1 = x_2 = 0\\} \cup \\{ x_3 = x_4 = x_5 = x_6 = 0\\}
    \end{equation}
    and $T = (\mathbb{C}^*)^2$ with the action on the coordinates
    \begin{equation}
    \begin{aligned}
    g_1(\lambda) : (x_1, x_2, x_3, x_4, x_5, x_6) &\mapsto (x_1, x_2, \lambda x_3, \lambda x_4, \lambda x_5, \lambda x_6)\cr
    g_2(\lambda) : (x_1, x_2, x_3, x_4, x_5, x_5) &\mapsto (\lambda x_1, \lambda x_2, x_3, x_4, x_5, \lambda^{-2} x_6)
    \end{aligned}
    \end{equation}
    Note that the group element
    \begin{equation}
    g_1^2 g_2(\lambda): (x_1, x_2, x_3, x_4, x_5, x_6) \mapsto (\lambda x_1, \lambda x_2, \lambda^2 x_3, \lambda^2 x_4, \lambda^2 x_5, x_6)
    \end{equation}
    reproduces the familiar weighted projective space action on the first five variables.