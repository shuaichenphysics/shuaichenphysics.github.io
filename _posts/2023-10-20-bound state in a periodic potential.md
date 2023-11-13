---
layout: post
title: "Wanner waves, tight-binding model and quantum geometry"
date: 2023-11-13
excerpt: "Construct tight-binding model with a periodic potential"
tags: [Quantum geoemtry, Bloch theorem]
comments: true
---

* toc
{:toc}

# Wanner waves, tight-binding model and quantum geometry

## Wannier waves
We begin with the single-particle Schroedinger equation in $$d$$ spatial dimensions

$$
H\vert\psi\rangle=\left[-\frac{(\hbar\nabla)^{2}}{2m}+V(\mathbf{r})\right]\vert\psi\rangle, 
\label{eq:Hcont}
$$

where $$V(\mathbf{r}+\mathbf{a}_{i})=V(\mathbf{r})$$ represents a periodic potential, and $$\mathbf{a}_{i}$$ ($$i=1,\cdots,d$$) defines a lattice system. According to the Bloch theorem, the solutions, known as Bloch waves, for an energy band $$n$$ can be expressed as:

$$
\psi_{n\mathbf{k}}(\mathbf{r})=e^{i\mathbf{k}\cdot\mathbf{r}}u_{n\mathbf{k}}(\mathbf{r}),
$$

where $$u_{n\mathbf{k}}(\mathbf{r})$$ is a periodic Bloch function satisfying $$u_{n\mathbf{k}}(\mathbf{r})=u_{n\mathbf{k}}(\mathbf{r}+\mathbf{a}_{i})$$, and $$\mathbf{k}$$ is the Bloch wavevector. The normalization condition for $$u_{n\mathbf{k}}(\mathbf{r})$$ is given by:

$$
\int_{\text{u.c.}}d^{d}\mathbf{r} \vert u_{n\mathbf{k}}(\mathbf{r})\vert^{2}=1,
$$

where the integral is taken over one unit cell.
Here, u.c. represents the unit cell with volume $$\mathcal{A}_\mathrm{uc}$$. The energy $$\epsilon_n(\mathbf{k})$$ satisfies periodicity with respect to the reciprocal lattice vectors $$\mathbf{G}_i$$, given by the condition $$\mathbf{a}_i \cdot \mathbf{G}_j = 2\pi \delta_{ij}$$. In other words, the energy is invariant under translations by the reciprocal lattice vectors.

We consider composite bands labeled by the band index $$n$$ in a specific subset $$\mathcal{V}$$, which is separated from other bands by sufficiently large band gaps. In this case, we can construct a set of Wannier basis states $$\{\vert\mathbf{r}_i\alpha\rangle\}$$ that span the same sub-Hilbert space as the Bloch waves corresponding to the bands with indices $$n\in\mathcal{V}$$.
The Wannier basis states can be expressed as follows:

$$
\begin{align}
\vert\mathbf{r}_i\alpha\rangle &= \frac{\mathcal{A}_\mathrm{uc}}{(2\pi)^d}\int_\mathrm{BZ} d^d\mathbf{k}\, e^{i\mathbf{k}\cdot(\mathbf{r}-\mathbf{r}_i)} \sum_{n\in\mathcal{V}} (\mathcal{U}_\mathbf{k})_{n,\alpha} \vert u_{n\mathbf{k}}\rangle, \label{eq:wannier_Bloch1} \\
\vert u_{n\mathbf{k}}\rangle &= \sum_{\mathbf{r}_i}\sum_\alpha e^{-i\mathbf{k}\cdot(\mathbf{r}-\mathbf{r}_i)} (\mathcal{U}_\mathbf{k}^\dagger)_{\alpha,n} \vert\mathbf{r}_i\alpha\rangle. \label{eq:wannier_Bloch2}
\end{align}
$$

Here, $$\mathcal{A}_\mathrm{uc}$$ is the volume of the unit cell, and $$\mathbf{r}_i$$ represents a lattice site spanned by the lattice vectors $$\mathbf{a}_i$$ $$(i=1,\cdots,d)$$. The integration over momentum is performed over the first Brillouin zone (BZ). The unitary matrix $$\mathcal{U}_\mathbf{k}$$ is chosen to optimize the localization of the Wannier functions.
The Wannier function $$\langle\mathbf{r}\vert\mathbf{r}_i\alpha\rangle \equiv w_\alpha(\mathbf{r}-\mathbf{r}_i)$$ is localized around the lattice site $$\mathbf{r}_i$$. It turns out to be the Fourier transformation of the corresponding Bloch wave, and thus inherits the orthonormality properties of the Bloch functions.

## Quantum metric: lower bound of quadratic spread

The unitary matrix $$\mathcal{U}_{\mathbf{k}}$$ is chosen to maximize the localization of Wannier functions by minimizing a localization functional, as introduced by _Marzari and Vanderbilt in their seminal work_ [^1]. The localization functional is given by

$$
\begin{align}
F & =\sum_{\alpha\in\mathcal{V}}\left[\langle\mathbf{0}\alpha\vert r^{2}\vert\mathbf{0}\alpha\rangle-\vert\langle\mathbf{0}\alpha\vert\mathbf{r}\vert\mathbf{0}\alpha\rangle\vert^{2}\right]  =F_{I}+\delta F~. 
\end{align}
$$

Both parts, $$F_I$$ and $$\delta F$$, are non-negative, where

$$
\begin{align}
F_{I} & =\sum_{\alpha\in\mathcal{V}}\left[\langle\mathbf{0}\alpha\vert r^{2}\vert\mathbf{0}\alpha\rangle-\sum_{\mathbf{r}_{i}}\sum_{\beta}\vert\langle\mathbf{r}_{i}\beta\vert\mathbf{r}\vert\mathbf{0}\alpha\rangle\vert^{2}\right],\\
\delta F & =\sum_{\mathbf{r}_{i}(\neq\mathbf{0})}\sum_{\beta(\neq\alpha)}\vert\langle\mathbf{r}_{i}\beta\vert\mathbf{r}\vert\mathbf{0}\alpha\rangle\vert^{2}.
\end{align}
$$

The optimization of the unitary matrix $$\mathcal{U}_{\mathbf{k}}$$ aims to minimize the localization functional $$F$$, leading to the construction of maximally localized Wannier functions.
The term $$F_I$$ is independent of the unitary transformation $$\mathcal{U}_{\mathbf{k}}$$ and therefore gauge invariant. This allows us to choose $$\mathcal{U}_{\mathbf{k}}$$ as an identity matrix with components $$(\mathcal{U}_{\mathbf{k}})_{\alpha,n}=\delta_{\alpha,n}$$ when calculating $$F_I$$.
Then from the relation in Eqs.$$~(\ref{eq:wannier_Bloch1})$$ and $$(\ref{eq:wannier_Bloch2})$$, we have

$$
\begin{align}
\langle u_{n\mathbf{k}}\vert u_{m\mathbf{k+q}}\rangle & =\sum_{\mathbf{r}_{i}}e^{-i\mathbf{k}\cdot\mathbf{r}_{i}}\langle\mathbf{r}_{i}n\vert e^{-i\mathbf{q}\cdot\mathbf{r}}\vert\mathbf{0}m\rangle ,\label{eq:uuq}
\end{align}
$$

By taking the derivative with respect to $$\mathbf{q}$$ on both sides of Eq.~$$(\ref{eq:uuq})$$, we obtain a series of relations in the limit $$q\rightarrow 0$$. For example, taking the first and second derivatives with respect to $$\mathbf{q}$$ gives

$$
\begin{align}
\langle u_{n\mathbf{k}}\vert\nabla_{\mathbf{k}}u_{m\mathbf{k}}\rangle & =-i\sum_{\mathbf{r}_{i}}e^{-i\mathbf{k}\cdot\mathbf{r}_{i}}\langle\mathbf{r}_{i}n\vert\mathbf{r}\vert\mathbf{0}m\rangle ,\\
\langle u_{n\mathbf{k}}\vert\nabla_{\mathbf{k}}^{2}u_{m\mathbf{k}}\rangle & =-\sum_{\mathbf{r}_{i}}e^{-i\mathbf{k}\cdot\mathbf{r}_{i}}\langle\mathbf{r}_{i}n\vert\mathbf{r}^{2}\vert\mathbf{0}m\rangle,
\end{align}
$$

Similarly, we can establish the converse relations

$$
\begin{align}
\langle\mathbf{r}_{i}n\vert\mathbf{r}\vert\mathbf{0}m\rangle & =i\frac{\mathcal{A}_{\mathrm{uc}}}{(2\pi)^{d}}\int_\mathrm{BZ} d^{d}\mathbf{k}e^{i\mathbf{k}\cdot\mathbf{r}_{i}}\langle u_{n\mathbf{k}}\vert\nabla_{\mathbf{k}}u_{m\mathbf{k}}\rangle ,\\
\langle\mathbf{r}_{i}n\vert\mathbf{r}^{2}\vert\mathbf{0}m\rangle & =\frac{\mathcal{A}_{\mathrm{uc}}}{(2\pi)^{d}}\int_\mathrm{BZ} d^{d}\mathbf{k}e^{i\mathbf{k}\cdot\mathbf{r}_{i}}\langle\nabla_{\mathbf{k}}u_{n\mathbf{k}}\vert\nabla_{\mathbf{k}}u_{m\mathbf{k}}\rangle.
\end{align}
$$

Therefore, we can simplify $$ F_{I} $$ as 

$$
\begin{align}
F_{I} & =\sum_{\alpha\in\mathcal{V}}\left[\langle\mathbf{0}\alpha\vert r^{2}\vert\mathbf{0}\alpha\rangle-\sum_{\mathbf{r}_{i}}\sum_{\beta}\vert\langle\mathbf{r}_{i}\beta\vert\mathbf{r}\vert\mathbf{0}\alpha\rangle\vert^{2}\right]\\
 & =\frac{\mathcal{A}_{\mathrm{uc}}}{(2\pi)^{d}}\int_\mathrm{BZ}d^{d}\mathbf{k}\sum_{n\in\mathcal{V}}\mathrm{Re}\langle\nabla_{\mathbf{k}}u_{n\mathbf{k}}\vert(\mathbb{I}_{\mathcal{V}}-\vert u_{n\mathbf{k}}\rangle\langle u_{n\mathbf{k}}\vert)\vert\nabla_{\mathbf{k}}u_{n\mathbf{k}}\rangle~,
\end{align}
$$

where $$\mathbb{I}_{\mathcal{V}}$$ is the identity operator in the sub-Hilbert space spanned by bands carrying indices in $$\mathcal{V}$$. This expression clearly shows that $$F_{I}$$ is expressed in terms of the quantum metric.
Since $$\delta F\geq 0$$, we have the inequality relation,

$$
F\geq F_{I}~.
$$

Hence, we can conclude that the quantum metric characterizes an obstruction to finding a complete set of exponentially localized Wannier functions. 
When $$F_{I}$$ is finite, it indicates that more bands need to be included in the composite bands in order to construct a complete set of exponentially localized Wannier functions.

## Second perspective: quantum metric from multi-band models

Another perspective on the quantum metric arises from considering a multiband tight-binding model. Assuming we have already obtained a complete set of exponentially localized Wannier functions constructed from composite bands, 
we can approximate the continuum Hamiltonian in Eq.$$~(\ref{eq:Hcont})$$ with a tight-binding model. In the language of second quantization, the continuum model in Eq.$$~(\ref{eq:Hcont})$$ can be expressed as

$$
H=\int d^{d}\mathbf{r}\psi^{\dagger}(\mathbf{r})\left[-\frac{(\hbar\nabla)^{2}}{2m}+V(\mathbf{r})\right]\psi(\mathbf{r})~. \label{eq:2ndH}
$$

We then expand the field operator $$\psi(\mathbf{r})$$ in the basis
of Wannier functions 

$$
\psi(\mathbf{r})=\sum_{\mathbf{r}_{i}}\sum_{\alpha\in\mathcal{V}}w_{\alpha}(\mathbf{r}-\mathbf{r}_{i})a_{i\alpha}+\sum_{\mathbf{r}_{i}}\sum_{\beta\in\mathcal{V}^{\perp}}w_{\beta}^{\perp}(\mathbf{r}-\mathbf{r}_{i})b_{i\beta}~,
$$

where $$w_{\beta}^{\perp}(\mathbf{r}-\mathbf{r}_{i})$$ denotes Wannier
functions associated with the complementary band set $$\mathcal{V}^{\perp}$$. 
By substituting the expansion into the Hamiltonian in Eq.~$$(\ref{eq:2ndH})$$, we can derive a tight-binding model defined on the lattice $$\{\mathbf{r}_{i}\}$$

$$
\begin{align}
H & =\sum_{\alpha\beta\in\mathcal{V}}\sum_{\mathbf{r}_{i},\mathbf{r}_{j}}\langle\mathbf{r}_{i}\alpha\vert H\vert\mathbf{r}_{j}\beta\rangle a_{i\alpha}^{\dagger}a_{j\beta}^{}+\sum_{\alpha^{\prime},\beta^{\prime}\in\mathcal{V}^{\perp}}\sum_{\mathbf{r}_{i},\mathbf{r}_{j}}\langle\mathbf{r}_{i}\alpha^{\prime}\vert H\vert\mathbf{r}_{j}\beta^{\prime}\rangle b_{i\alpha^{\prime}}^{\dagger}b_{j\beta^{\prime}}^{}\nonumber \\
 & =\sum_{\alpha\beta\in\mathcal{V}}\sum_{\mathbf{r}_{i},\mathbf{r}_{j}}t_{ij,\alpha\beta}a_{i\alpha}^{\dagger}a_{j\beta}^{}+\sum_{\alpha^{\prime},\beta^{\prime}\in\mathcal{V}^{\perp}}\sum_{\mathbf{r}_{i},\mathbf{r}_{j}}t_{ij\alpha^{\prime}\beta^{\prime}}^{\perp}b_{i\alpha^{\prime}}^{\dagger}b_{j\beta^{\prime}}^{}~, \label{eq:tbhfull}
\end{align}
$$

where no mixing term between indices from $$\mathcal{V}$$ and $$\mathcal{V}^{\perp}$$.
Up to this point, all the derivations have been rigorous, and the expression in Eq.~$$(\ref{eq:tbhfull})$$$ includes all bands. However, since our interest lies solely in the bands belonging to $$\mathcal{V}$$, we can utilize a complete set of exponentially localized Wannier functions to approximate the Hamiltonian in Eq.$$~(\ref{eq:Hcont})$$ with a multi-band tight-binding model $$H_{\mathrm{tb}}$$ by disregarding the $$t^\perp$$ terms

$$
\begin{align}
H_{\mathrm{tb}} & =\sum_{\alpha\beta\in\mathcal{V}}\sum_{\mathbf{r}_{i},\mathbf{r}_{j}}t_{ij,\alpha\beta}a_{i\alpha}^{\dagger}a_{j\beta} =\sum_{\alpha\beta\in\mathcal{V}}\sum_{\mathbf{k}}h_{\alpha\beta}(\mathbf{k})a_{\mathbf{k}\alpha}^{\dagger}a_{\mathbf{k}\beta}^{{}},
\label{eq:tb}
\end{align}
$$

where $$t_{ij,\alpha\beta}$$ exponentially decays with the distance $$\vert\mathbf{r}_{i}-\mathbf{r}_{j}\vert$$. In Eq.~$$(\ref{eq:tb})$$, we have further introduced the Fourier transformation $$a_{\mathbf{k}\alpha}^{\dagger}=\frac{1}{\sqrt{N}}\sum_{\mathbf{r}_{i}}a_{i\alpha}^{\dagger}e^{i\mathbf{k}\cdot\mathbf{r}_{i}}$$, where $$N$$ represents the total number of lattice sites.
In our specific setup, where there is a significant gap between the targeted band and the others, we can project onto the targeted band using the following expressions

$$
a_{i\alpha}\rightarrow\frac{1}{\sqrt{N}}\sum_{\mathbf{k}}e^{i\mathbf{k}\cdot\mathbf{r}_{i}}g_{\mathbf{k}}^{*}(\alpha)c_{\mathbf{k}}~,
$$

or 

$$
\psi({\mathbf r})\rightarrow\frac{1}{\sqrt{N}}\sum_{\mathbf{k}}e^{i\mathbf{k}\cdot\mathbf{r}_{i}}g_{\mathbf{k}}^{*}(\alpha)c_{\mathbf{k}}~,
$$

where $$g_{\mathbf{k}}$$ represents an eigenvector of $$h_{\alpha\beta}(\mathbf{k})$$, and $$c_{\mathbf{k}}$$ annihilates an electron in the targeted band. It is important to note that the index $$\alpha$$ appearing in both $$a_{i\alpha}$$ and $$g_{\mathbf{k}}(\alpha)$$ arises from the realization of a multiband tight-binding model, which accounts for the nontrivial quantum metric or Wannier obstruction. This can be inferred from the quantum metric associated with $$g_{\mathbf{k}}$$.


[^1] Nicola Marzari and David Vanderbilt, Maximally localized generalized Wannier functions for composite energy bands, [Phys. Rev. B 56, 12847](https://journals.aps.org/prb/abstract/10.1103/PhysRevB.56.12847)
