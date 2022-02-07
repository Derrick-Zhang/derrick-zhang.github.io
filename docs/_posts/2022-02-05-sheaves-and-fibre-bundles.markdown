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
Give two sheaves $Sh = (S, \pi, X)$ and $\widetilde{Sh} = (\widetilde{S}, \widetilde{\pi}, X)$