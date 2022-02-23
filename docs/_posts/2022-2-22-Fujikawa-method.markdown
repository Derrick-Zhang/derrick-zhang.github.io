---
layout: post
title:  "Fujikawa Method"
date:   2022-02-22 23:49:00 -0000
categories: math, physics
---

Fujikawa method is used to compute chiral anomaly in quantum field theory. Effectively, it uses the Atiyah-Singer index theorem.

## Definition
Suppose given a Dirac field $\psi$ which transform according to a representation $\rho$ of the compact Lie group $G$, and we have a background connection form of taking values in the Lie algebra $\mathfrak{g}$. The Dirac operator is
\begin{equation}
D\\!\\!\\!\\!/\ = \partial \\!\\!\\!/\ + i A \\!\\!\\!/\
\end{equation}
and the fermionic action is given by
\begin{equation}
\int d^d x\, \bar{\psi} i D \\!\\!\\!\\!/\ \psi
\end{equation}
The partition function is
\begin{equation}
Z[A] = \int \mathcal{D} \bar{\psi} \mathcal{D} \psi\, e^{-\int d^d x\, \bar{\psi} i D\\!\\!\\!/\ \psi}
\end{equation}