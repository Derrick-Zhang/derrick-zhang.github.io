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
S=\int d^4 x\, \bar{\psi} i D \\!\\!\\!\\!/\ \psi
\end{equation}
The partition function is
\begin{equation}
Z[A] = \int \mathcal{D} \bar{\psi} \mathcal{D} \psi\, e^{-\int d^4 x\, \bar{\psi} i D\\!\\!\\!/\ \psi}
\end{equation}
The axial symmetry transformation goes as
\begin{equation}
\begin{aligned}
\psi &\to e^{i \gamma_5 \alpha} \psi\cr
\bar{\psi} &\to \bar{\psi} e^{i \gamma_5 \alpha} \cr
S &\to S + \int d^4x \, \alpha(x) \partial_\mu(\bar{\psi} \gamma^\mu \gamma_5 \psi)
\end{aligned}
\end{equation}
Classically, this implies that the chiral current $j^\mu_5 \equiv \bar{\psi} \gamma^\mu \gamma_5 \psi$ is conserved, $\partial_\mu j^\mu_5 = 0$.

Quantum mechanically, the chiral current is not conserved. Fujikawa interpreted this as a change in the partition function measure under a chiral transformation. To calculate a change in the measure under a chiral transformation, first consider the Dirac fermions in a basis of eigenvetors of the Dirac operator
\begin{equation}
\psi = \sum_i \psi_i a^i, \quad \bar{\psi} = \sum_i \psi_i b^i
\end{equation}
where $a^i, b^i$ are Grassmann valued coefficients, and $\psi_i$ are eigenvectors of the Dirac operator
\begin{equation}
D\\!\\!\\!\\!/\ \psi_i = - \lambda_i \psi_i
\end{equation}
The eigenfunctions are taken to be orthonormal with respect to integration
\begin{equation}
\delta^j_i = \int \frac{d^4x}{(2\pi)^4} \psi^{\dagger j}(x) \psi_i(x)
\end{equation}
The measure of the path integral is then defined to be
\begin{equation}
\mathcal{D}\psi \mathcal{D} \bar{\psi} = \prod_i da^i db^i
\end{equation}
Under an infinitesimal chiral transformation, write
\begin{equation}
\begin{aligned}
\psi &\to \psi' = (1 + i \alpha \gamma_5) \psi = \sum_i \psi a'^i\cr
\bar{\psi} & \to \bar{\psi}' = \bar{\psi} (1 + i \alpha \gamma_5) = \sum_i \psi_i b'^i
\end{aligned}
\end{equation}
The Jacobian of the transformation can be calculated as
\begin{equation}
C^i_j \equiv \left(\frac{\delta a}{\delta a'}\right)^i_j = 
\end{equation}