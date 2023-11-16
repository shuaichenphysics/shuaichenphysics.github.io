---
layout: post
title: "Peierls Substitution"
date: 2023-11-16
excerpt: "How does gauge field play in a lattice model? Peierls Substitution!"
tags: [Condensed matter, Bloch Theorem, Lattice Gauge Field]
comments: true
---


# Peierls substitution


In condensed matter, we need to solve the Shroedinger equation in
the presence of a periodic potential. One may start with a continuous
model

$$
H=-\frac{\nabla^{2}}{2m}+V(\mathbf{r})
\label{eq:Seq}
$$

with a periodic potential $$V(\mathbf{r}+\mathbf{a}_{i})=V(\mathbf{r})$$.
The periodic potential defines a lattice $$\mathbf{R}\in\{\sum_{i}n_{i}\mathbf{a}_{i}\}$$.
The famous Bloch theorem tells us that a general solution 

$$
H\psi_{\mathbf{k}}(\mathbf{r})=E(\mathbf{k})\psi_{\mathbf{k}}(\mathbf{r})
$$

to the Schroedinger equation in Eq. $$(\ref{eq:Seq})$$ can be written
in the form as 

$$
\begin{align}
\psi_{\mathbf{k}}(\mathbf{r}) & =e^{i\mathbf{k}\cdot\mathbf{r}}u_{\mathbf{k}}(\mathbf{r}),
\end{align}
$$

where $$N$$ is the number of unit cells and $$\mathbf{k}$$ is the crystal
momentum related to the lattice. To consider the minimal coupling
to the gauge field, it is better to separate the crystal momentum
dependence from $$u_{\mathbf{k}}(\mathbf{r})$$.It can be achieved by
by the Wannier function $$W_{\mathbf{R}}(\mathbf{r})$$ that appears
as the Fourier transformation of the periodic part of the Bloch wave,

$$
\psi_{\mathbf{k}}(\mathbf{r})=\frac{1}{\sqrt{N}}\sum_{\mathbf{R}}e^{i\mathbf{k}\cdot\mathbf{R}}W_{\mathbf{R}}(\mathbf{r}).\label{eq:Wann}
$$

Then we can calculate the eigenvalue $$E(\mathbf{k})$$ , by calculating
the matrix element

$$
\begin{align}
E(\mathbf{k}) & =\int d\mathbf{r}\psi_{\mathbf{k}}^{*}(\mathbf{r})H\psi_{\mathbf{k}}(\mathbf{r})=\int d\mathbf{r}\frac{1}{N}\sum_{\mathbf{R}^{\prime}\mathbf{R}}e^{i\mathbf{k}\cdot(\mathbf{R}^{\prime}-\mathbf{R})}W_{\mathbf{R}}^{*}(\mathbf{r})HW_{\mathbf{R}^{\prime}}(\mathbf{r})\\
 & =\frac{1}{N}\sum_{\mathbf{R}^{\prime}\mathbf{R}}e^{i\mathbf{k}\cdot(\mathbf{R}^{\prime}-\mathbf{R})}t(\mathbf{R}^{\prime}-\mathbf{R})
\end{align}
$$

with $$t(\mathbf{R}^{\prime}-\mathbf{R})$$ is the hopping integral

$$
\begin{align}
t(\mathbf{R}^{\prime}-\mathbf{R}) & =\int d\mathbf{r}W_{\mathbf{R}}^{*}(\mathbf{r})HW_{\mathbf{R}^{\prime}}(\mathbf{r}).
\end{align}
$$

Therefore, we can have a tight-binding model corresponding to the
continuous model in Eq.~$$(\ref{eq:Seq})$$

$$
\begin{align}
H_{\mathrm{tb}} & =\frac{1}{N}\sum_{\mathbf{R}^{\prime}\mathbf{R}}e^{i\mathbf{k}\cdot(\mathbf{R}^{\prime}-\mathbf{R})}t(\mathbf{R}^{\prime}-\mathbf{R})c_{\mathbf{R}}^{\dagger}c_{\mathbf{R}^{\prime}}\\
 & =\sum_{\mathbf{k}}E(\mathbf{k})c_{\mathbf{k}}^{\dagger}c_{\mathbf{k}}.
\end{align}
$$

One of the most striking features of Eq.$$~(\ref{eq:Wann})$$ is the independence
of Wannier function on the crystal momentum. With the preparation
above, we can proceed to consider a minimal coupling to a gauge field,
with the Hamiltonian

$$
H(\mathbf{A})=\frac{(-i\mathbf{\nabla-\mathbf{A}}(\mathbf{r},t))^{2}}{2m}+V(\mathbf{r}).
$$

Our aim is to obtain the guiding principles directing minimal coupling
in the tight-binding model to the gauge field. That is, we want to
express physical quantities in terms of the crystal momentum. We can
consider the modified Wannier functions by the gauging principle for
a continuous model

$$
W_{\mathbf{R}}(\mathbf{r},\mathbf{A})=\exp\left(i\int_{\mathbf{R}}^{\mathbf{r}}\mathbf{A}(\mathbf{r}^{\prime},t)\right)W_{\mathbf{R}}(\mathbf{r}).
$$

Obviously, $$W_{\mathbf{R}}(\mathbf{r})=W_{\mathbf{R}}(\mathbf{r},\mathbf{A}\rightarrow0)$$.
We then have a new solution to $$H(\mathbf{A})$$

$$
\psi_{\mathbf{k}}(\mathbf{r},\mathbf{A})=\frac{1}{\sqrt{N}}\sum_{\mathbf{R}}e^{i\mathbf{k}\cdot\mathbf{R}}W_{\mathbf{R}}(\mathbf{r},\mathbf{A})
$$

We can check this by

$$
\begin{align}
& H(\mathbf{A})\psi_{\mathbf{k}}(\mathbf{r},\mathbf{A})  \\
=& \left[\frac{(-i\mathbf{\nabla-\mathbf{A}}(\mathbf{r},t))^{2}}{2m}+V(\mathbf{r})\right]\frac{1}{\sqrt{N}}\sum_{\mathbf{R}}e^{i\mathbf{k}\cdot\mathbf{R}}W_{\mathbf{R}}(\mathbf{r},\mathbf{A})\\
 =& \frac{1}{\sqrt{N}}\sum_{\mathbf{R}}e^{i\mathbf{k}\cdot\mathbf{R}}\left[\frac{(-i\mathbf{\nabla-\mathbf{A}}(\mathbf{r},t))^{2}}{2m}+V(\mathbf{r})\right]\left[\exp\left(i\int_{\mathbf{R}}^{\mathbf{r}}\mathbf{A}(\mathbf{r}^{\prime},t)\right)W_{\mathbf{R}}(\mathbf{r})\right]\\
 =& \frac{1}{\sqrt{N}}\sum_{\mathbf{R}}\exp\left(i\int_{\mathbf{R}}^{\mathbf{r}}\mathbf{A}(\mathbf{r}^{\prime},t)\right)e^{i\mathbf{k}\cdot\mathbf{R}}\left[\frac{(-i\mathbf{\nabla-\mathbf{A}}(\mathbf{r},t)+\mathbf{A}(\mathbf{r},t))^{2}}{2m}+V(\mathbf{r})\right]W_{\mathbf{R}}(\mathbf{r})\\
 =& \frac{1}{\sqrt{N}}\sum_{\mathbf{R}}\exp\left(i\int_{\mathbf{R}}^{\mathbf{r}}\mathbf{A}(\mathbf{r}^{\prime},t)\right)e^{i\mathbf{k}\cdot\mathbf{R}}\left[\frac{(-i\nabla)^{2}}{2m}+V(\mathbf{r})\right]W_{\mathbf{R}}(\mathbf{r})
\end{align}
$$

When calculating the hopping integral, we have 

$$
\begin{align}
t_{\mathbf R\mathbf R^{\prime}}(\mathbf{A}) & =\int d\mathbf{r}W_{\mathbf{R}}^{*}(\mathbf{r},\mathbf{A})HW_{\mathbf{R}^{\prime}}(\mathbf{r},\mathbf{A})\\
 & =\exp\left[i\int_{\mathbf{R}^{\prime}}^{\mathbf{R}}\mathbf{A}\cdot d\mathbf{r}^{\prime}\right]\int d\mathbf{r}e^{i\Phi_{R^{\prime}rR}}HW_{\mathbf{R}^{\prime}}(\mathbf{r})
\end{align}
$$

where $$\Phi_{R^{\prime}rR}=\oint_{R^{\prime}\rightarrow r\rightarrow R\rightarrow R^{\prime}}\mathbf{A}(\mathbf{r}^{\prime})\cdot d\mathbf{r}^{\prime}$$, is
the flux through the triangular made by three position arguments.Since
the $$\mathbf{A}$$ is approximately uniform at the lattice scale,---
the scale at which the Wannier states are localized to the positions
$$\mathbf{R}$$, we can than approximate $$\Phi_{R^{\prime}rR}=0$$, yielding
the desired result.

$$
t_{RR^{\prime}}(\mathbf{A})=\exp\left[i\int_{\mathbf{R}^{\prime}}^{\mathbf{R}}\mathbf{A}\cdot d\mathbf{r}^{\prime}\right]t(\mathbf{R}^{\prime}-\mathbf{R})
$$

Therefore, the matrix elements are the same as in the case without
magnetic field, apart from the extra phase factor picked up, which
is denoted by the Peierls phase factor. 

One can generalize the Peierls substitution in a multi-band system.
