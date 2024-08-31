---
layout: post
title:  "Seiberg-Witten Theory"
date:   2024-08-05 10:39:30 -0000
categories: physics
---

## Overview

We consider a 4d $\mathcal{N}=2$ supersymmetric gauge theory with gauge group $SU(2)$, with or without matter fields, and study its **low energy effective theory**. The fields of the microscopic $SU(2)$ theory can be described as follows.

- There is a **vector multiplet** ($A_\mu, \lambda, \bar{\lambda}, \phi$), with components in the adjoint representation of $SU(2)$. For example, $\phi = \phi_a \sigma_a$. In terms of $\mathcal{N}=1$ supersymmetry, we can group the fields into a vector multiplet $W_\alpha = (A_\mu, \lambda)$, and a chiral multiplet $\Phi = (\phi, \bar{\lambda})$.
- We can also add **hypermultiplets** ($q, \psi, \tilde{q}^\dagger, \tilde{\psi}^\dagger$) with components all in the same representation. In terms of $\mathcal{N}=1$ supersymmetry, we can group the fields into a chiral multiplet $Q = (q, \psi)$ in the given representation, and another chiral multiplet $\tilde{Q} = (\tilde{q}, \tilde{\psi})$ in the conjugate representation. 

In particular, we are interested in the case where there are $N_f$ hypermultiplets, in the fundamental representation of $SU(2)$. The theory is called $SU(2)$ theory with $N_f$ flavors. We will limit ourselves to this case.
There is also a **superpotential** term
\begin{equation}
    W = \sum_i \tilde{Q}^i \Phi Q_i + \sum_i m_i \tilde{Q}^i Q_i,
\end{equation}
where the $SU(2)$ indices are suppressed.

### Supersymmetric vacua

To study the low energy effective theory, let us study the vacua of the $SU(2)$ theory, which is given by the following conditions
\begin{equation}
\begin{aligned}
    &\frac{1}{g^2}[\phi, \phi^\dagger] + (q_i q^{\dagger i} - \tilde{q}_i^\dagger \tilde{q}^i) - \frac{1}{2}\mathrm{tr}(q_i q^{\dagger i} - \tilde{q}_i^\dagger \tilde{q}^i) \mathbb{I}_2 = 0,\\
    &q_i \tilde{q}^i - \frac{1}{2}\mathrm{tr}(q_i \tilde{q}^i) \mathbb{I}_2 = 0,\quad
    (\phi + m_i \mathbb{I}_2) q_i = 0, \quad \tilde{q}^i (\phi + m_i \mathbb{I}_2) = 0.
\end{aligned}
\end{equation}

In general, the theory admits a **Coulomb branch**, where
\begin{equation}
    \langle\phi\rangle = \begin{pmatrix}
        a & 0 \\
        0 & -a
    \end{pmatrix}, \quad \tilde{q}^i = \begin{pmatrix}
        0 & 0 
    \end{pmatrix}, \quad q_i  = \begin{pmatrix}
        0\\0
    \end{pmatrix}.
\end{equation}
On the Coulomb branch, the gauge group $SU(2)$ is broken to $U(1)$ for $a \neq 0$. A gauge invariant way to label the vacua is to use
\begin{equation}
    u = \frac{1}{2}\langle \mathrm{tr}(\phi^2) \rangle = a^2.
\end{equation}

In certain cases, the theory could also admit a **Higgs branch**, where $\phi = 0$, and $q, \tilde{q}$ acquire non-zero vacuum expectation values, and the gauge symmetry is completely broken. Such branches appear when $m_i = 0$ for $N_f \ge 2$. The geometry of the Higgs branch is found by setting to zero the $D$-terms, dividing by the gauge group $SU(2)$, and asking for the superpotential to be stationary. A theory on the Higgs branch does not contain monopoles or dyons. The classical moduli space is a **hyperkähler manifold**, with metric uniquely determined by the symmetries of the theory. Moreover, the metric does not receive quantum corrections.

We will be mainly focusing on the Coulomb branch. On this branch, the low energy effective theory depends on a **prepotential** $\mathcal{F}(a)$ such that
\begin{equation}
    \tau(a) = \frac{\partial^2 \mathcal{F}(a)}{\partial a^2}.
\end{equation}
Defining $a_D = \partial \mathcal{F}/\partial a$, the metric on the moduli can be written as
\begin{equation}
    ds^2 = \mathrm{Im}(d a_D\, d\bar{a}).
\end{equation}
To understand the low energy theory, we just need the information of $\mathcal{F}(a)$.
Classically, we have
\begin{equation}
    \mathcal{F}\_{\mathrm{cl}}(a) = \frac{1}{2}\tau\_{UV} a^2.
\end{equation}
However, the gauge coupling $\tau$ receives quantum corrections, from one-loop renormalization and instantons. Hence, $\mathcal{F}(a)$ would also receive quantum corrections.

### The one-loop renormalization of the gauge coupling

The one-loop renormalization of the gauge coupling is given by
\begin{equation}
    \mu \frac{d}{d\mu} g = - \frac{g^3}{(4\pi)^2} \left[\frac{11}{3} C(\mathbf{adj}) - \frac{2}{3} \sum\_f C(\mathbf{R}\_f) - \frac{1}{3} \sum\_s C(\mathbf{R}\_s)\right] \equiv - \frac{g^3}{(4\pi)^2} \cdot b.
\end{equation}
In an $\mathcal{N}=2$ gauge theory, the vector multiplet contains one vector field, one complex scalar and two Weyl fermions, both in the adjoint representation. Each hypermultiplet contains two scalars and two Weyl fermions, in the same representation. Therefore, we have
\begin{equation}
    b = 2 C(\mathbf{adj}) - 2\sum\_i C(\mathbf{R}\_i).
\end{equation}
For $SU(2)$ with $N_f$ flavors, we have $b = 4 - N_f$.
On the Coulomb branch, the $SU(2)$ gauge theory is generally broken to a $U(1)$ gauge theory and the gauge coupling is related as follows,
\begin{equation}
    \tau\_{U(1)} = 2 \tau\_{SU(2)} = \frac{8\pi i}{g^2} + \frac{\theta}{\pi},
\end{equation}
where $g$ is the gauge coupling in the original $SU(2)$ theory. Let $\tau$ be the $U(1)$ gauge coupling, and we have
\begin{equation}
    \mu \frac{d}{d\mu} \tau = \frac{i}{\pi} \cdot b = \frac{i}{\pi} (4 - N\_f),
\end{equation}
for $SU(2)$ theory with $N_f$ flavors. We will consider the cases where $N_f = 0, 1, 2, 3$, so that the theory is asymptotically free. The theory with $N_f = 4$ is also of great interest because the $\beta$-function vanishes. Integrating this equation, we get
\begin{equation}
    \tau(a)  = \tau\_{UV} + \frac{i}{\pi}\cdot b \ln \left(\frac{a}{\Lambda\_{UV}}\right) = \frac{i}{\pi}\cdot  b \ln \left(\frac{a}{\Lambda\_{N\_f}}\right),
\end{equation}
where
\begin{equation}
    \Lambda_{N\_f}^b = \mu^b \exp(\pi i \tau(\mu)),
\end{equation}
is the **dynamically generated scale**, that is invariant under the change of the energy scale of the theory, and $b= 4-N_f$. Due to $\mathcal{N}=2$ supersymmetry, this does not receive perturbative corrections higher than one-loop. However, we can still add non-perturbative corrections due to instantons.

### Instantons

A configuration of instanton number $k$ is proportional to the $k$-instanton factor
\begin{equation}
    \exp\left(\frac{-8 \pi^2 k}{g^2}\right) = \left(\frac{\Lambda\_{N\_f}}{a}\right)^{bk} = \left(\frac{\Lambda\_{N\_f}}{a}\right)^{k(4-N\_f)}.
\end{equation}
Also with the help of the $U(1)_R$ anomaly as discussed in Seiberg and Witten's original paper, we can write
\begin{equation}
    \tau(a) = \frac{i}{\pi} \cdot b \ln \left(\frac{a}{\Lambda\_{N\_f}}\right) + \sum\_{k=0}^\infty \frac{c\_k}{2\pi i} \left(\frac{\Lambda\_{N\_f}}{a}\right)^{bk}.
\end{equation}
Then integrate it over $a$ twice, we obtain the expansion of the prepotential
\begin{equation}
    \mathcal{F}(a) = - \frac{b}{2\pi i} a^2 \ln \left(\frac{a}{\Lambda\_{N\_f}}\right) + \sum\_{k=1}^\infty \frac{d\_k}{2\pi i} \left(\frac{\Lambda\_{N\_f}}{a}\right)^{bk} \cdot a^2.
\end{equation}
The problem is how to solve for these coefficients $d_k$'s.

One useful identity is called the renormalization group relation.
\begin{equation}
    2\pi i \Lambda\_{N\_f} \frac{\partial}{\partial \Lambda\_{N\_f}} \mathcal{F}(a, \Lambda\_{N\_f}) = bu. 
\end{equation}
One immediate way to justify this is to notice that from the definition of the dynamically generated scale, we have
\begin{equation}
    2\pi i \Lambda\_{N\_f} \frac{\partial}{\partial \Lambda\_{N\_f}} = 2b \cdot \frac{\partial}{\partial \tau\_{UV}}.
\end{equation}
In the ultraviolet, the prepotential is given by
\begin{equation}
    \mathcal{F}\_{\mathrm{cl}} = \frac{1}{2}\tau\_{UV} a^2 = \frac{1}{2} \tau\_{UV} \cdot u. 
\end{equation}
Therefore, we can obtain an expansion of $u$ in terms of $a$,
\begin{equation}
    u = a^2 \left[1 + \sum\_{k=1}^\infty k d\_k \left(\frac{\Lambda\_{N\_f}}{a}\right)^{bk}\right].
\end{equation}
The inverse of this function gives $a$ as a function of $u$. In practice, we can use Seiberg-Witten curve to solve for $a(u)$ in the weak coupling region, and then we can use this formula to recursively solve for $d_k$'s.

### The singularity at infinity

In the weakly coupled regime, where $|a| \gg |\Lambda_{N_f}|$, the perturbative effect dominates, and we have
\begin{equation}
    a \simeq \sqrt{u}, \quad \mathcal{F}(a) \simeq -\frac{b}{2\pi i} a^2 \ln \left(\frac{a}{\Lambda\_{N\_f}}\right)~.
\end{equation}
Then
\begin{equation}
    a\_D = \frac{\partial \mathcal{F}(a)}{\partial a} \simeq - \frac{b}{2\pi i} a \left[ \ln \left(\frac{a^2}{\Lambda^2\_{N\_f}}\right) + 1\right].
\end{equation}
When $u \to e^{2\pi i} u$, we have
\begin{equation}
    a \to -a, \quad  a_D \to -a_D + b a.
\end{equation}
Therefore, the monodromy at infinity is given by
\begin{equation}
    M\_\infty = \begin{pmatrix}
        -1 & b\\\\
        0 & -1
    \end{pmatrix} = \begin{pmatrix}
        -1 & 4 - N\_f\\\\
        0 & - 1
    \end{pmatrix} = - T^{-(4-N\_f)}.
\end{equation}

### Other singularities

Now we would like to determine the other singularities of the theory.
Roughly speaking, as we vary $u$ on the $u$-plane, some massive particles would become massless at certain point, leading to a singularity at that point.

The $N_f = 0$ case is discussed in Michael's talk, and will be briefly reviewed below, where a magnetic monopole becomes massless at $u = \Lambda_0^2$, and a dyon becomes massless at $u = - \Lambda_0^2$, leading to two singularities. For $N_f \neq 0$, the analysis depends the value of the bare masses of the hypermultiplets.

If all bare masses are zero, then there are no other singularities at weak coupling $\|a\| > \|\Lambda_{N_f}\|$. All the singularities lie within the strongly coupled region, governed by the global symmetries. We will discuss this in details, in examples.

The number of singularities can be easily determined if the bare masses are large, $\|m_i\| \ge \|\Lambda_{N_f}\|$. 
There will be other singularities in the weak coupling region $\|a\| > \|\Lambda_{N_f}\|$, more specifically, at $\|a\| = \|m_i\|$, which can be seen as follows. In the effective theory, we can get the physical masses of $q, \tilde{q}$ by expanding the superpotential,
\begin{equation}
    W = \sum\_i \begin{pmatrix}
        \tilde{q}^i\_1 & \tilde{q}^i\_2
    \end{pmatrix} \begin{pmatrix}
        a & 0\\\\
        0 & -a
    \end{pmatrix} \begin{pmatrix}
        q\_i^1\\\\q\_i^2 
    \end{pmatrix} + \sum\_i m\_i \begin{pmatrix}
        \tilde{q}^i\_1 & \tilde{q}^i\_2
    \end{pmatrix}
    \begin{pmatrix}
        q\_i^1\\\\q\_i^2
    \end{pmatrix}.
\end{equation}
We see that the mass is given by $|a \pm m_i|$. So when $a = \pm m_i$ or $u = m_i^2$, one component of $q_i$ and $\tilde{q}^i$ becomes massless. In this case, we expect the other $N_f$ singularities in the weak coupling region. In the strong coupling region, at the energy scale $|a| < |\Lambda_{N_f}| < |m_i|$, the low energy theory contains no hypermultiplets as degrees of freedom, and is a pure $SU(2)$ theory, and we expect two singularities in the strong coupling region.

Moreover, we expect that the singularities for large bare masses will change smoothly into the singularities for massless hypermultiplets, if we change $m_i$'s adiabatically.

The masses separate the energy scale into different regions, hence we have different theories in each region. The dynamically generated scales at two adjacent regions can be related by the matching condition, described as follows.
Recall the one-loop renormalization of the coupling constant is
\begin{equation}
    \tau\_{N\_f}(a) = \frac{i}{\pi} (4-N\_f) \ln \left(\frac{a}{\Lambda\_{N\_f}}\right).
\end{equation}
Now if there are $N_f - N_f'$ hypermultiplets, with bare masses $|m| > |a|$. Then the low energy theory at scale $|a|$ contains only $N_f'$ hypermultiplets as degrees of freedom. From $\tau_{N_f}(m) = \tau_{N_f'}(m)$, we obtain that
\begin{equation}
    \Lambda\_{N\_f'}^{4-N\_f'} = m^{N\_f - N\_f'} \Lambda\_{N\_f}^{4-N\_f}.
\end{equation}