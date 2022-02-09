---
layout: post
title:  "Analytic Sheaves"
date:   2022-02-08 10:00:00 -0000
categories: math
---

The discussion here mainly follows [_Lectures on vector bundles over Riemann surfaces_](https://www.amazon.com/Lectures-Bundles-Riemann-Surfaces-Mathematical-ebook/dp/B08D6ZVK6Y) by Robert C. Gunning.

## Sheaves of modules
The definition of a sheaf of rings over a topological space parallels that of a sheaf of abelian groups, except that each stalk now has the structure of a ring. We also need to require that both algebraic operations (addition and multiplication) are continuous. We will simply consider commutative rings with multiplicative identity. There are two canonical sections over any open set, the zero section and the identity section. Considering only the additive structure, a sheaf of rings can be viewed as a sheaf of abelian groups.

Let $\mathcal{R}$ be a sheaf of rings and $\mathcal{S}$ be a sheaf of abelian groups over a topological space $M$, with respective projections $\rho: \mathcal{R} \to M$ and $\pi: \mathcal{S} \to M$. Viewing $\mathcal{R}$ merely as a sheaf of abelian groups, the Cartesian product $\mathcal{R} \times \mathcal{S}$ has the structure of a sheaf of abelian groups over $M \times M$, with the projection $\rho \times \pi: \mathcal{R} \times \mathcal{S} \to M \times M$. The restriction of this sheaf to the diagonal $M \subset M \times M$ is then a sheaf of abelian groups over $M$, which will be denoted by $\mathcal{R} \circ \mathcal{S}$. <span style="color:blue">Essentially we are building a sheaf of abelian groups from a sheaf of rings and another sheaf of abelian groups</span>

<span style="text-decoration:underline">Definition.</span> The sheaf $\mathcal{S}$ of abelian groups over $M$ is called a **sheaf of modules** over the sheaf $\mathcal{R}$ of rings (or more briefly, a sheaf of $\mathcal{R}$-modules) if there is given a sheaf homomorphism $\mathcal{R} \circ \mathcal{S} \to \mathcal{S}$ such that for each point $p \in M$ the induced mappingon stalks $\mathcal{R}\_p \times \mathcal{S}\_p \to \mathcal{S}\_p$ defines on $\mathcal{S}\_p$ the structure of an $\mathcal{R}\_p$-module.

For any open set $U \subset M$, a section $f \in \Gamma(U, \mathcal{R} \circ \mathcal{S})$ is readily seen to be the restriction to the diagonal $U \subset U \times U$ of a section $(r,s) \in \Gamma(U \times U, \mathcal{R} \times \mathcal{S})$; that is, there are sections $r \in \Gamma(U, \mathcal{R})$ and $s \in \Gamma(U, \mathcal{S})$ such that $f(p) = (r(p), s(p))$ for all $p \in U$. The sections $\Gamma(U, \mathcal{R})$ form a ring, and the sections $\Gamma(U, \mathcal{S})$ form an abelian group. The homomorphism $\mathcal{R} \circ \mathcal{S} \to \mathcal{S}$ exhibiting $\mathcal{S}$ as a sheaf of $\mathcal{R}$-modules leads to a mapping $\Gamma(U, \mathcal{R} \circ \mathcal{S}) \cong \Gamma(U, \mathcal{R}) \times \Gamma(U, \mathcal{S}) \to \Gamma(U, \mathcal{S})$, which clearly defines on $\Gamma(U, \mathcal{S}) = \mathcal{S}\_U$ the structure of a $\Gamma(U,\mathcal{R})$-module. Thus $\\{\mathcal{S}_U\\}$ is in the obvious sense a presheaf of modules over the presheaf $\\{\mathcal{R}_U\\}$ of rings. Conversely, whenever $\\{\mathcal{R}_U\\}$ is a presheaf of rings and $\\{\mathcal{S}\_U\\}$ is a presheaf of abelian groups, such that $\mathcal{S}_U$ is an $\mathcal{R}_U$-module and restriction mappings are module homomorphisms, the associated sheaf $\mathcal{S}$ is a sheaf of $\mathcal{R}$-modules.

One additional construction of some importance should be mentioned as well. If $\mathcal{S}$ and $\mathcal{J}$ are sheaves of $\mathcal{R}$-modules, their tensor product $\mathcal{S} \otimes_{\mathcal{R}_U}\mathcal{J}$ is the sheaf defined by the presheaf $\\{\mathcal{S}_U \otimes\_{\mathcal{R}_U} \mathcal{J}_U\\}$. This is also a sheaf of $\mathcal{R}$-modules. For details, please refer to the Wikipedia page of [tensor products of modules](https://en.wikipedia.org/wiki/Tensor_product_of_modules). In particular, for any sheaf $\mathcal{J}$ of $\mathcal{R}$-modules, $\mathcal{R} \otimes\_{\mathcal{R}} \mathcal{J} = \mathcal{J}$.

If
\begin{equation} 0 \to \mathcal{S}_1 \to \mathcal{S}_2 \to \mathcal{S}_3 \to 0\end{equation}
is an exact sequence of sheaves of $\mathcal{R}$-modules, then tensoring with $\mathcal{J}$ yields an exact sequence
\begin{equation} \mathcal{S}_1 \otimes\_{\mathcal{R}} \mathcal{J} \to \mathcal{S}_2 \otimes\_\mathcal{R} \mathcal{J} \to\mathcal{S}_3 \otimes\_\mathcal{R} \mathcal{J} \to 0\end{equation}
Note especially that it is not claimed that the latter sequence is a full short exact sequence; for if $0 \to \mathcal{S}_1 \to \mathcal{S}_2$ is exact, it is not necessarily true that $0 \to \mathcal{J} \otimes \mathcal{S}_1 \to \mathcal{J} \otimes \mathcal{S}_2$ is exact. The sheaf $\mathcal{J}$ is called **flat** if  $0 \to \mathcal{J} \otimes \mathcal{S}_1 \to \mathcal{J} \otimes \mathcal{S}_2$ is exact whenever $0 \to \mathcal{S}_1 \to \mathcal{S}_2$ is exact.

## Free and locally free sheaves
If $\mathcal{S}$ and $\mathcal{J}$ are sheaves of $\mathcal{R}$-modules, their **direct sum** is the sheaf of $\mathcal{R}$-modules defined by the presheaf $\\{\mathcal{S}\_U \oplus \mathcal{J}\_U\\}$, and will be denoted by $\mathcal{S} \oplus \mathcal{J}$; this sheaf can be identified in the obvious manner with the sheaf $\mathcal{S} \circ \mathcal{J}$ considered earlier. A particularly simple example is the sheaf of $\mathcal{R}$-modules $\mathcal{R}^m = \mathcal{R} \oplus \dots \oplus \mathcal{R}$, the direct sum of $m$ copies of the sheaf $\mathcal{R}$; any sheaf of $\mathcal{R}$-modules isomorphic to $\mathcal{R}^m$ will be called a **free sheaf** of $\mathcal{R}$-modules **of rank** $m$.

Note that the stalk $\mathcal{R}^m_p$ at a point $p$ is just the set of $m$-tuples of elements of $\mathcal{R}\_p$; and elements $R \in \mathcal{R}^m_p$ will be considered as column vectors
\begin{equation}R = \begin{pmatrix} r_1\\ r_2\\ \dots\\ r_m\end{pmatrix}\end{equation}
