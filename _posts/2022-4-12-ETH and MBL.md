---
layout: post
title: "Eigenstate thermalization hypnosis and many-body localization"
date: 2022-4-12
excerpt: "How to reconcile between statistics and the quantum mechanism is always elusive"
tags: [Statistics, quantum mechanism]
comments: true
---

* toc
{:toc}



In this note, we concentrate on the thermalization of quantum many-body systems.

# Introduction 

Thermalization can be characterized by the time evolution of local observables $$ \langle O(t)\rangle $$ or entanglement entropy (EE) $$ S(t)=-\mathrm{tr}\rho_A(t)\ln\rho_A(t) $$.   Upon the behaviors of observables or EE, one may categorize quantum many-body systems into different classes: __quantum-ergodic systems__, __quantum many-body localized (MBL) systems__ and __quantum many-body scar__. In the first case, parts of the system act as heat reservoirs for other parts, and an initial non-equilibrium state relaxes to a thermal equilibrium, which is reminiscent of classical chaotic systems and effectively forgets initial conditions in the course of time evolution. An MBL system, in contrast, retains the memory of the initial state for the local observables to reach some stationary value in a non-thermal state to sustain much longer quantum coherence.  One may measure thermalization by EE, 

$$
\begin{align}
S(t)&\sim t \quad \mathrm{quantum\, ergodic} \\
S(t)&\sim \log t\quad \mathrm{MBL} 
\end{align}
$$

The former is attributed to quasiparticles moving at a finite speed and the latter to macroscopic invariants. The last class, __Qantum Many-body scar__, indeed shows weak ergodicity breaking phenomena. A famous example is the AKLT spin chain, which has been rigorously proven to possess non-thermal eigenstates.

As a matter of fact, the classification highlights the famous __Eigenstate Thermalization Hypothesis(ETH)__

> ETH governs the process of thermalization in closed quantum systems in the absence of coupling to a thermal bath. Generally, the following three consequences are the most relevant
>
> 1. The expectation values of physical observables in individual, high-excited eigenstates of ergodic systems are thermal such that they can be intuitively viewed as random vectors in the Hilbert space, and expectation values of local observables in such eigenstates are a smooth function of energy. 
> 2. By postulating the form of the off-diagonal matrix elements, the ETH makes predictions for the temporal fluctuations of local observables: independent of the initial state, an observable approaches its equilibrium value, and then remains near that value most of the time with fluctuations exponentially suppressed by the thermodynamic entropy.
> 3. For a large finite subsystem, $$A$$ of an infinite ETH system, the reduced density matrix $$\rho_A$$ is equal to the thermodynamic density matrix at the effective temperature set by the energy of the corresponding eigenstate.

# Quantum Many-body scar

A famous example is the AKLT state, which is rigorously proved to possess quantum scar, with the Hamiltonian

$$
H=\sum_{j=1}^{L} (\frac{1}{3}+\frac{1}{2} \mathbf{S}_{j} \cdot \mathbf{S}_{j+1}+\frac{1}{6}\left(\mathbf{S}_{j} \cdot \mathbf{S}_{j+1}\right)^{2} )
$$

where $$ \mathbf S$$ is the spin-1 operator, and we assume the periodic boundary condition. The ground state is proven to have an exact MPS representation. Explicitly, 

$$
\begin{align}
|\psi\rangle = &  \sum_{\sigma_1,\sigma_2,\cdots \sigma_L} c_{\sigma_1,\sigma_2,\cdots,\sigma_L}|\sigma_1,\sigma_2,\cdots,\sigma_L\rangle \\
             =&  \sum_{\sigma_1,\sigma_2,\cdots \sigma_L} \mathrm{Tr}(A_1^{[\sigma_1]}A_2^{[\sigma_2]}\cdots A_L^{[\sigma_L]})
\end{align}
$$

with 

$$
A^{[+]}=\sqrt{\frac{2}{3}}\sigma^+, \quad A^{[0]}=-\frac{1}{\sqrt{3}}\sigma^z,\quad A^{[-]}=-\sqrt{\frac{2}{3}}\sigma^-
$$

One may construct the quasiparticle excitations above the ground state with momentum $$\mathbf k$$ on top of a general MPS state as 

$$
| \psi_{A}(B, k)\rangle =\sum_{j=1}^{L} e^{i k j} \sum_{\{\sigma_{j}\}} \mathrm{Tr}(\cdots A^{[\sigma_{j-1}]} B^{[\sigma_{j}]} A^{[\sigma_{j+1}]} \cdots)|\sigma_{1} \sigma_{2} \cdots \sigma_{L}\rangle
$$

In the framework of the Single-Mode approximation, the quasiparticles are usually described in terms of a single-site quasiparticle creation operator $$ \hat O $$, such that 

$$
B^{[\sigma]}=\sum_{\sigma,\sigma^\prime}\hat O_{\sigma,\sigma^\prime}A^{[\sigma^\prime]}.
$$



# PXP model

The PXP model describes a chain of coupled two-level systems, 
where each system can be one of the two possible states $$ |\circ\rangle $$ and $$ |\bullet\rangle $$.  In the Ryderg atom realization, these states correspond to an atom being in its ground state or in the excited Rydberg state. Equivalently, we can view it as a spin model subject to a projector.

$$
H_\mathrm{PXP} =\sum_i P_{i-1}\sigma_i^x P_{i+1} 
$$

where $$ P_i=|\circ\rangle\langle\circ|=\frac{1-\sigma_i^z}{2} $$ 
is projector operator on the site $$ i $$. 
The PXP model constrains spin-flip processes: it allows a spin to flip only both of its nearest neighbors are in $$\circ$$ state. 

$$
\begin{align}
\cdots \circ\circ_i\circ \cdots & \leftrightarrow \cdots \circ\bullet_i\circ\cdots\quad\mathrm{allowed} \\
\cdots \bullet\circ_i\circ \cdots & \leftrightarrow \cdots \bullet\bullet_i\circ\cdots\quad\mathrm{forbidden}
\end{align}
$$

In fact, such a project splits Hilbert space into several __unconnected fragmental blocks__ with states marked by the configurations with adjacent excitations $$\cdots \bullet \bullet\cdots$$  that cannot be changed or removed!) Among all fragmental blocks, the largest connected component of the Hilbert space is one that excludes any configurations of adjacent excitations $$ \cdots \bullet \bullet\cdots $$.  At present, studies are mainly focused on the largest one. 



# Hermitian Chaos

For Hermitian quantum system, the university of quantum chaos can obey the university from the theory of random matrix.  

> * Bohigas, Giannoni, and Schmit conjectured that chaotic quantum systems exhibit spectral correlation as those found in RMT in the same symmetry class (BGS conjecture)
> * Berry and Tabor observed that integral systems follow Poisson statistics of uncorrelated random variables.

## Level statistics

For the ordered sequence of eigenvalues $$\lambda_1<\cdots< \lambda_n <\lambda_{n+1}<\cdots$$, one defines the normalized spacings $$s=(\lambda_{n+1}-\lambda_{n})/\langle s\rangle$$. The probability distribution of the spacing is approximately given by 

$$
P(s) = c_\beta s^\beta e^{-\alpha_\beta  s^2}
$$

with two numerical constants being such that $$P(s)$$ Is normalized 

$$
\int_0^\infty ds P(s)=1
$$

and the mean spacing is 

$$
\int_0^\infty ds s P(s)=1
$$

Specifically, 

> 1. $$c_\beta =\frac{\pi}{2},\alpha_\beta =\frac{\pi}{4}$$ for orthogonal ensemble GOS ($$\beta =1$$), 
> 2. $$c_\beta =\frac{32}{\pi^2}$$, $$\alpha_\beta =\frac{4}{\pi}$$ for unitary ensemble GUE ($$\beta=2$$)
> 3. $$c_\beta = \frac{2^{18}}{3^6\pi^3}$$, $$\alpha_\beta = \frac{64}{9\pi}$$ For symplectic ensemble GSE($$\beta =4$$)

## Bulk statistics 





## Edge statistics: Tracy-Widom distribution

# Non-Hermitian Chaos

## Brief introduction

The study of spectral statistics is of fundamental importance in theoretical physics due to its university and utility as a robust diagnosis of quantum chaos. One of the central problems comes with how classically integrable and chaotic behavior carries over to the quantized world. One simple spectral measure was found in the spacing between  neighboring eigenvalues of the corresponding Hamiltonian $$H$$. 
     In a non-Hermitian system, shortly after BGS conjecture, the spectral distribution between integral was extended by Grobe, Haake, and Sommers (GHS) to Markovian dissipation open quantum systems, followed by a Lindblad master equation,
     
$$
\frac{d\rho}{dt} =L\rho(t)
$$

with $L$ Being the Liouville and $$\rho$$ the density operator. 

* In the integral limit, the agreement between nearest neighbor spacing in radial distance $$s$$ of its complex bulk eigenvalues is found to be Poisson distribution

* In the fully  chaotic limit, the spacing distribution agrees with the corresponding Ginibre ensemble of complex Gaussian non-Hermitian random matrices (GinUE)
  
  $$
  p_{\text {GinUE }}(s)=\left(\prod_{k=1}^{\infty} \frac{\Gamma\left(1+k, s^{2}\right)}{k !}\right) \sum_{j=1}^{\infty} \frac{2 s^{2 j+1} e^{-s^{2}}}{\Gamma\left(1+j, s^{2}\right)}
  $$
  
  with $$\Gamma(1+k,s^2)=\int_0^\infty t^k e^{-t}dt$$ Being the incomplete $$\Gamma$$ function.  Such a result is surprising. The complex Ginibre ensemble does not satisfy the global symmetries of the dissipation open quantum system. Based on the perturbation argument for small distance $s$, the repulsive is universally cubic. 

## Thermolization and Heating Dynamics in Open Many body system

Systems described by statistical mechanics can be divided into three distinct classes: (i) systems in contact with large thermal baths (ii) isolated systems and (iii) systems coupled to nonthermal environments. 

> __Class (i)__ can be described by a phenomenological master equation in which the detailed balance condition ensures that the system always relaxes to the Gibbs ensemble with the temperature of the thermal bath. 
>       __Class (ii)__ believes to be governed by the ETH as a generic mechanism of thermalization under unitary dynamics of isolated quantum systems.  
>       __Class (iii)__ relates to coupling to a nonthermal environment and violates the detailed balanced condition, as it permits arbitrary nonunitary processes such as continuous measurements and engineered dissipation. Thus, the bath temperature does not exist.  

Questions remain for class (iii) systems. Does the system still thermalize and, if yes, in what sense? How are steady states under such situations related to the thermal equilibrium of the system Hamiltinain?

 
