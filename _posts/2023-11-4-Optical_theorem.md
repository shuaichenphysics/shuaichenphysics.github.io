---
layout: post
title: "Optical theorem"
date: 2023-11-04
excerpt: "Optical theorem"
tags: [Quantum mechanics]
comments: true
---

* toc
{:toc}
# Optical Theorem 

We consider Schroedinger equation with the incident $$\vert\psi_{in}\rangle$$ and emergent $$\vert\psi_{out}\rangle$$ states. The scattering matrix
is then defined as

$$
\vert\psi_{out}\rangle=S\vert\psi_{in}\rangle
$$

The incident state $$\vert\psi_{in}\rangle=\vert\mathbf{k}\rangle$$ is an eigenstate of the free Hamiltonian $$H_{0}=-\Delta$$ of energy $$E=k_{0}^{2}$$ that is 

$$
H_{0}\vert\psi_{in}\rangle=E\vert\psi_{in}\rangle
$$

The emergent state $$\vert\psi_{out}\rangle$$ is an eigenstate of the total Hamiltonian $$H=H_{0}+V$$ with the same energy, namely 

$$
H\vert\psi_{out}\rangle=E\vert\psi_{out}\rangle
$$

At infinity, the two states $$\vert\psi_{in}\rangle$$ and $$\vert\psi_{out}\rangle$$ only differ by the scattered wave, whose amplitude tends to zero. As a consequence, the two states are identical up to a phase difference. We then can obtain the relation 

$$
VS=(E-H_{0})(S-I)
$$

by the observation

$$
\begin{align}
H\vert\psi_{out}\rangle-H_{0}\vert\psi_{in}\rangle & =E(\vert\psi_{out}\rangle-\vert\psi_{in}\rangle)\\
HS-H_{0} & =E(S-I)\\
VS & =E(S-I)-H_{0}(S-I)=(E-H)(S-I)
\end{align}
$$

Without interaction $$V=0$$, $$S=1$$. Using the resolvent operator $$G_{0}$$ associated with the free problem $$(E-H_{0})G=1$$, we can have the Dyson equation

$$
S=1+G_{0}VS
$$

Projecting this equation on an incident state $$\vert\mathbf{k}\rangle$$ we have the relation 

$$
\vert\psi_{out}\rangle=\vert\mathbf{k}\rangle+G_{0}V\vert\psi_{out}\rangle
$$

Now we can define the scattering operator 

$$
T=VS
$$

which satisfies the Lippman-Schwinger equation 

$$
S=1+G_{0}T
$$

For the emergent state, we have by taking $$\vert\psi_{in}\rangle=\vert\mathbf{k}\rangle$$

$$
\vert\psi_{out}\rangle=\vert\mathbf{k}\rangle+G_{0}T\vert\mathbf{k}\rangle
$$

whose projection on $$\vert\mathbf{r}\rangle$$ yields

$$
\langle\mathbf{r}\vert\psi_{out}\rangle=e^{i\mathbf{k}\cdot\mathbf{r}}+\int d\mathbf{r}^{\prime}\langle\mathbf{r}\vert G_{0}\vert\mathbf{r}^{\prime}\rangle\langle\mathbf{r}^{\prime}\vert T\vert\mathbf{k}\rangle
$$

 With the asymptotic expansion, 
 
$$
\psi(\mathbf{r})=e^{i\mathbf{k}\cdot\mathbf{r}}+\frac{e^{i\mathbf{k}_{0}\mathbf{r}}}{r}f(\mathbf{k},\mathbf{k}^{\prime})
$$

we have 

$$
f(\mathbf{k},\mathbf{k}^{\prime})=-\frac{1}{4\pi}\langle\mathbf{k}^{\prime}\vert T\vert\mathbf{k}\rangle
$$

To derive the optical theorem, we start with the Lippman-Schwinger equation, 

$$
\langle\mathbf{k}\vert T^{\dagger}\vert\psi_{out}\rangle=\langle\mathbf{k}\vert T^{\dagger}\vert\mathbf{k}\rangle+\langle\mathbf{k}\vert T^{\dagger}G_{0}T\vert\mathbf{k}\rangle
$$

$$
\mathrm{Im}\langle\mathbf{k}\vert T^{\dagger}\vert\mathbf{k}\rangle=-\mathrm{Im}\langle\mathbf{k}\vert T^{\dagger}G_{0}T\vert\mathbf{k}\rangle
$$

To proceed, we can ($$\epsilon(k)=k^{2}$$) 

$$
\begin{align}
\langle\mathbf{k}\vert T^{\dagger}G_{0}T\vert\mathbf{k}\rangle & =\int dk^{\prime}\langle\mathbf{k}\vert T^{\dagger}\vert k^{\prime}\rangle\langle k^{\prime}\vert G_{0}\vert k^{\prime}\rangle\langle k^{\prime}\vert T\vert\mathbf{k}\rangle\\
 & =\pi\int dk^{\prime}\delta(E-H_{0}(\mathbf{k}^{\prime}))\langle\mathbf{k}\vert T^{\dagger}\vert k^{\prime}\rangle\langle k^{\prime}\vert G_{0}\vert k^{\prime}\rangle\langle k^{\prime}\vert T\vert\mathbf{k}\rangle\\
 & =\frac{\pi}{2k_{0}}\int d\mathbf{k}^{\prime}\vert\langle\mathbf{k}\vert T^{\dagger}\vert\mathbf{k}^{\prime}\rangle\vert^{2}\delta(\mathbf{k}^{\prime}-\mathbf{k})
\end{align}
$$

by observing

$$
\begin{align}
\langle k^{\prime}\vert G_
{0}\vert k^{\prime}\rangle & =\langle k^{\prime}\vert\frac{1}{E-H_{0}(k^{\prime})+i0^{+}}\vert k^{\prime}\rangle\\
 & =i\pi\delta(E-H_{0}(k^{\prime})
\end{align}
$$

In general, we have

$$
\langle\mathbf{k}\vert T^{\dagger}G_{0}T\vert\mathbf{k}\rangle=\pi\left[\frac{d\epsilon(k_{0})}{dk_{0}}\right]^{-1}\int d\mathbf{k}^{\prime}\vert\langle\mathbf{k}\vert T^{\dagger}\vert\mathbf{k}^{\prime}\rangle\vert^{2}\delta(\mathbf{k}^{\prime}-\mathbf{k})
$$

With these basic understandings, one may think about the optical theorem in condensed matter systems. Namely, one shall consider a scattering process under the background of a periodic potential.




