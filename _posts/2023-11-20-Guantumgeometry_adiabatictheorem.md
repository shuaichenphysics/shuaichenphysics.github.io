---
layout: post
title: "Quantum geometry: a view from the adiabatic theorem"
date: 2023-11-20
excerpt: "What is the originality of the quantum geometry? A touch from the adiabatic theorem "
tags: [Quantum Geometry, Adiabatic Theorem]
comments: true
---

* toc
{:toc}

# Riemann structure of Hilbert space

Given a parameter dependent Hamiltonian $$H(\lambda_{a})$$ with $$\lambda_{a},a=1,2,\cdots$$,
we have a family of grand states 

$$
H(\lambda)\vert\psi(\lambda)\rangle=E(\lambda)\vert\psi(\lambda)\rangle.
$$

The manifold is formed by the parameter-dependent ground wave functions. In their seminal paper, the authors introduced a Riemannian differential structure in the Hilbert space. Specifically, the Riemann structure is embedded in the Quantum Geometry Tensor (QGT) denoted as $$\mathfrak{G}$$. This tensor can be expressed using the following formula:

$$
\mathfrak{G}_{ab}(\lambda)=\langle\partial_{a}\psi(\lambda)\vert\partial_{b}\psi(\lambda)\vert-\langle\partial_{a}\psi(\lambda)\vert\psi(\lambda)\rangle\langle\psi(\lambda)\vert\partial_{b}\psi(\lambda)\rangle.
$$

The Quantum Geometry Tensor  captures the structural information of the Hilbert space. It consists of two components: the quantum metric, denoted as $$\mathcal{G}$$, and the Berry curvature, denoted as $$\mathcal{B}$$. The quantum metric corresponds to the real part of the QGT, while the Berry curvature corresponds to its imaginary part. These quantities provide essential geometric properties that describe the quantum system under consideration.

$$
\mathfrak{G}=\mathcal{G}-i\mathcal{B}/2
$$

In differential geometry, the curvature of a manifold provides information about its intrinsic geometric properties, such as how the manifold curves and bends. It is related to the concept of parallel transport and describes how vectors change as they are transported along different paths on the manifold. On the other hand, the metric of a manifold determines the notion of distance and angle between points. It defines the geometric properties of length and angle measurement on the manifold.
The Riemannian structure asserts that the curvature and metric of a manifold are intimately related. Specifically, the metric tensor determines the curvature tensor, which encodes the curvature properties of the manifold. The compatibility between the curvature and metric is captured by the Riemann curvature tensor, which provides a systematic way to measure and quantify the curvature of the manifold. This relationship between curvature and metric is a fundamental aspect of Riemannian geometry.
Further insights and explanations regarding the compatibility between curvature and metric can be found in subsequent blog posts on the topic.


# Quantum geometry tensor and adiabatic theorem

In quantum mechanics, the Berry curvature is closely tied to the Berry phase and can be understood within the framework of the adiabatic approximation.

Consider a time-dependent Hamiltonian $$H(\lambda)$$, which relies on a set of varying parameters. Our goal is to solve the time-dependent Schrödinger equation:

$$
i\frac{\partial}{\partial t}\vert\Psi(t)\rangle = H(\lambda)\vert\Psi(t)\rangle.
$$

In general, solving this equation is challenging compared to the case of a static equation where we can separate time using a dynamical phase. However, the adiabatic theorem comes to our aid. It states that if there exists a significant energy gap between the non-degenerate ground state and the excited states, we can approximately treat the time and spatial coordinates as separate entities. According to the adiabatic approximation, we make an assumption, known as an ansatz, that the ground state only acquires phase factors without undergoing transitions to the excited states.

Thus, we express the wave function in the adiabatic approximation as:

$$
\vert\Psi(\lambda(t))\rangle = e^{-i\gamma(t)}e^{-i\int^{t}E(\lambda)}\vert\psi(\lambda)\rangle,
$$

where $$\vert\psi(\lambda)\rangle$$ represents the simultaneous eigenstate of the Hamiltonian $$H(\lambda)$$:

$$
H(\lambda)\vert\psi(\lambda)\rangle = E(\lambda)\vert\psi(\lambda)\rangle.
$$

The first phase factor, $$e^{-i\gamma(t)}$$, corresponds to the well-known Berry phase. It can be related to the Berry phase by considering the phase factor accumulated along a closed path $$\Omega$$ in the Hilbert space:

$$
e^{-i\gamma_{\Omega}(t)}e^{-i\int_{\Omega}A\cdot d\lambda} = \prod_{\lambda_{i}}\frac{\langle\psi(\lambda(t_{i}))\vert\psi(\lambda(t_{i+1})\rangle}{\vert\langle\psi(\lambda(t_{i}))\vert\psi(\lambda(t_{i+1})\rangle\vert},
\label{eq:Berry}
$$

where $$\lambda_{i}$$ represents the discrete points along the closed path. When no phase is accumulated along a path, it appears featureless. In the definition of the Berry phase, we introduce a normalization factor, specifically the absolute value of the inner product between the states $$\langle\psi(\lambda(t_{i}))\vert\psi(\lambda(t_{i+1})\rangle$$, as shown in Eq.$$~(\ref{eq:Berry})$$. Consequently, the adiabatic theorem captures only the curvature structure. To obtain the complete Riemannian structure, we need to go beyond the adiabatic approximation.


The leading correction to the adiabatic approximation takes into account the rate at which the particle transitions to excited states with a certain probability.

$$
\begin{align}
P & =1-\vert\langle\psi(\lambda(t_{i}))\vert\psi(\lambda(t_{i+1})\vert^{2}=1-2\langle\psi(\lambda(t_{i}))\vert\frac{d}{dt}\vert\psi(t_{i+1})\rangle dt,
\end{align}
$$

which is nothing more than the quantum metric (or the Bures distance
which measures the distance between two quantum states in the sense
of the time evolution). Accordingly, the ground state ansatz shall
be modified 

$$
\vert\Psi(\lambda)\rangle=e^{-\mathbb{g}(t)-i\gamma(t)}e^{-i\int^{t}E(\lambda)}\vert\psi(\lambda)\rangle
$$

For a closed path, we have 

$$
\begin{align}
e^{-\mathbb{g}_{\Omega}-i\gamma_{\Omega}} & =e^{-\int\vert\langle\lambda(t_{i})\vert\frac{d}{dt}\vert\lambda(t_{i})\rangle\vert dt-i\int_{\Omega}A\cdot d\lambda}\\
 & =\prod_{\lambda_{i}}\langle\psi(\lambda_{i})\vert\psi(\lambda_{i+1})\rangle\\
 & =\prod_{\lambda_{i}}\frac{\langle\psi(\lambda_{i})\vert\psi(\lambda_{i+1})\rangle}{\vert\langle\psi(\lambda_{i})\vert\psi(\lambda_{i+1})\rangle\vert}\vert\langle\psi(\lambda_{i})\vert\psi(\lambda_{i+1})\rangle\vert
\end{align}
$$

Currently, it is evident that the amplitude of the term $$e^{-\mathbb{g}{\Omega}-i\gamma{\Omega}}$$ can decay over time or along a given path. The Berry phase, denoted as $$e^{-i\gamma_{\Omega}(t)}$$, relies on the path's homotopy. Conversely, the term $$e^{-\mathbb{g}{\Omega}}$$, which corresponds to the quantum metric, is sensitive to the specific details of the path. For instance, when the particle traverses the same path multiple times, say $$n$$ times, the probability of it remaining in the original state becomes $$P=e^{-n \mathbbf{g}_{\Omega}}$$.


Locally, we can expand the distance for a infinitesimal change of
the parameters 

$$
D=1-\vert\langle\psi(\lambda)\vert\psi(\lambda+d\lambda)\rangle\vert^{2}=\mathcal{G}_{ab}d\lambda_{a}d\lambda_{b}+\mathcal{O}((d\lambda)^{3})
$$

with 

$$
\mathcal{G}_{ab}=\mathrm{Re}[\langle\partial_{a}\psi(\lambda)\vert\partial_{b}\psi(\lambda)\vert-\langle\partial_{a}\psi(\lambda)\vert\psi(\lambda)\rangle\langle\psi(\lambda)\vert\partial_{b}\psi(\lambda)\rangle].
$$

