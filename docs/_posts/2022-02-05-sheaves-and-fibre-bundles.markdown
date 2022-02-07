---
layout: post
title:  "Sheaves and Fibre Bundles"
date:   2022-02-05 10:39:30 -0000
categories: math
---
I will mainly discuss sheaves, sheaf cohomology and fibre bundles, following _topological methods in algebraic geometry_ by Hirzebruch.
## Sheaves (of abelian groups)
A **sheave** (of abelian groups) is a three-tuple $Sh = (S, \pi, X)$ satisfying:
- $S$ and $X$ are topological spaces, the projection $\pi: S \to X$ is onto and continuous
- $\forall \alpha \in X$ has open neighbourhood $N \subset S$ such that $\pi\|_N:N \to \pi(N)$ is a homeomorphism, where $\pi(N)$ is an open neighbourhood of $\pi(\alpha)$ in $X$  
> $\forall x \in X$, preimage $\pi^{-1}(x)$ is called the **stalk** over $x$, denoted by $S_x$    
- Every stalk has the structure of an abelian group, for $\alpha, \beta \in S_x$, we can associate a sum $\alpha + \beta$ and difference $\alpha - \beta$ in $S_x$ and the difference is continuous in $\alpha$ and $\beta$

Usually we can define sheaves of any sets. But to talk about cohomology groups of $X$ with sheaf coefficients, the stalk has to be either a module or an abelian group.

## Sheaf homomorphism
Give two sheaves $Sh = (S, \pi, X)$ and $\widetilde{Sh} = (\widetilde{S}, \widetilde{\pi}, X)$, a homomorphism $h: Sh \to \widetilde{Sh}$ means
- $h: S \to \widetilde{S}$ is continuous
- $\pi = \widetilde{\pi} h$, $h$ maps the stalk $S_x$ to $\widetilde{S}_x$, $\forall x \in X$
- $\forall x \in X$, the restriction $h_x: S_x \to \widetilde{S}_x$ is a homomorphism

$h$ is a monomorphism/epimorphism/isomorphism if at each point $x \in X$, $h_x$ is injective/surjective/bijective.

## Presheaves
A **presheaf** $\mathcal{F}$ of sets over topological space $X$ is constructed as follows,
- associate to each open set $U \subset X$, a set $\mathcal{F}(U)$. Alternatively, we write it as $\Gamma(U,\mathcal{F})$, called the section of $\mathcal{F}$ over $U$
- there are restriction maps $r^U_V: \mathcal{F}(U) \to \mathcal{F}(V)$ for open sets $V \subset U$ such that
    - $r^U_U = {\rm id}_U$, $\forall$ open set $U \subset X$
    - $r^V_W \circ r^U_V = r^U_W$, for open sets $W \subset V \subset U$ of $X$

For presehaves of abelian groups, $\mathcal{F}(U)$ is an abelian group, $r^U_V$ a group homomorphism. Moreover, if $U$ is empty, $\mathcal{F}(U)$ is the zero group.

## Sheaves revisited
A presheaf is a **sheaf** if it satisfies: Given an opne covering $\mathfrak{U} = \\{U_i\\}_{i \in I}$ of $U$,
- (**Locality**) If $s, t \in \mathcal{F}(U)$, $\forall U_i \in \mathfrak{U}$, $s\|\_{U_i} = t\|\_{U_i}$, then $s=t$ 
- (**Gluing**) $\forall U_i \in \mathfrak{U}$, the section $s_i \in \mathcal{F}(U_i)$ is given such that $s_i \|\_{U_i \cap U_j} = s_j \|\_{U_i \cap U_j}$, then there exists a global section $s \in \mathfrak{F}(U)$ such that $s\|\_{U_i} = s_i$

One simple example of sheaves is the **sheaf of sections of a vector bundle**, where $\mathcal{F}(U)$ is a group of sections of the bundle over $U$ and the zero element of the group is given by the zero section.