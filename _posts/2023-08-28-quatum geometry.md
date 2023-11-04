---
layout: post
title: "Introduction to quantum geometry"
date: 2023-08-28
excerpt: "ABC about Quantum geometry"
tags: [Quantum Qeometry, math]
comments: true
---


Consider a generic parameter-dependent quantum system described by a Hamiltonian $$H(k)$$ and Schroedinger equation 

$$
H(x) |\psi_\alpha(x)\rangle = \epsilon_\alpha(x)|\psi_\alpha(x)\rangle
$$

With eigenvalue $$\epsilon_\alpha(x)$$ that forms a band structure in parameter space, and corresponding eigenstates $$|\psi_\alpha(x)\rangle $$. 
We remark that $$x$$ indeed represents a general parameter such as momentum, or interaction parameter. As the name geometry indicates, we will define so-called __quantum geometry__ that encodes structural information of the Hilbert spaces $$\{\mathcal H_x\}$$ when the parameter $$x$$ varies. 

It is often the case that perturbation occurs (in reality or thinking experiments) $$x\rightarrow x+\Delta x $$. Then the system shows response to the external perturbation and for weak perturbation, the response can be expressed in the unperturbed Hamiltonian $$H(x)$$. There are two aspects of changes. First, the __shift of the energy__ and we may call it the **spectrum physics** (I cook the name, not serious). More precisely, the information shall be encoded by the velocity 

$$
\mathbf v_\alpha(x)  = \nabla _x \epsilon_\alpha(x).
$$

The second part is the wave function (in parallel, we name it **wavefunction physics**), and similarly the information is encoded in $$|\partial_x \psi_\alpha(x)\rangle$$. While the role of the energy bands and band velocities in such quantities is for the most part well known, considerable attention has in recent decades shifted to the eigenstates. 

>  The quantum geometry works to provide a quantitative theory of the information encoded in the geometry $$x$$ dependence of eigenstates and to describe how this geometry is unveiled in the physical properties of the system of interest. 

# Quantum geometry tensor

We can regard the Hilbert space as a Riemannian manifold and then we can define the curvature and metric. Physically, we can define the quantum geometry tensor 

$$
T_{ij}(x) = \langle \partial_i \psi(x)|[1-|\psi(x)\rangle\langle\psi(x)|]|\partial_j\psi(x)\rangle
$$

It is related to the Berry curvature and quantum metric by

$$
T = g-\frac{i}{2}\Omega
$$

The QGT unifies the quantum metric as the real part and the Berry curvature as the imaginary part in a single complex gauge-invariant tensor field. 

# The origin of quantum geometry

The quantum geometry represents structural information of the Hilbert space. To see its originality, we can consider a variation of parameter for the Hamiltonian 

$$
H(x+\Delta x) = H(x)+\nabla_xH\cdot\Delta x
$$

When the perturbative term does not commute with $$H(x)$$ with

$$
\langle \psi_\alpha|\nabla_xH\cdot\Delta x|\psi_\beta\rangle\neq 0\quad \exist\beta\neq \alpha
$$

This means the eigenstate changes accordingly by means of the interband coupling mediated by the gradients of the Hamiltonian. To make this idea more quantitative, it is instructive to study the evolution of a single eigenstate when the parameters are varied by considering 

$$
\langle \psi(x)|\psi(x+\Delta x)\rangle = \mathcal Fe^{-i\Delta \varphi}
$$

With $$\mathcal F=|\langle \psi(x)|\psi(x+\Delta x)\rangle|$$. Such an overlap is non-zero whenever the states do not form an orthonormal basis in $$x$$-space. Separating into real and imaginary parts, one will find the expression.




