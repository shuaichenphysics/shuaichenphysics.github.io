---
layout: post
title: "Bound state and Bloch wave, Wannier function"
date: 2023-10-20
excerpt: "How can the Wannier wave influence a bound state "
tags: [Wannier function, Schroedinger equation]
comments: true
---

# Bound states under a periodic potential

## Schroedinger equation and Bloch waves

We first recall the Schroedinger equation with a periodic potential

$$
\left[-\frac{\nabla^{2}}{2m}+V(\mathbf{r})\right]\psi(\mathbf{r})=E\psi(\mathbf{r})\label{eq:bloch}
$$

Here $$V(\mathbf{r})$$ is a periodic potential $$V(\mathbf{r})=V(\mathbf{r}+\mathbf{a})$$.
The system obeys the translation symmetry and the Bloch theorem
tells that a general solution has the form as 

$$
\psi_{n\mathbf{k}}(\mathbf{r})=e^{i\mathbf{k}\cdot\mathbf{r}}u_{n\mathbf{k}}(\mathbf{r})\label{eq:solution}
$$

where $$u_{n\mathbf{k}}(\mathbf{r})$$ is also periodic with $$u_{n\mathbf{k}}(\mathbf{r})=u_{n\mathbf{k}}(\mathbf{r}+\mathbf{a})$$
and $$n$$ is the band index. The wave function $$u_{n\mathbf{k}}(\mathbf{r})$$
satisfies the equation 

$$
\left[\frac{k^{2}}{2m}+V(\mathbf{r})\right]u_{n\mathbf{k}}(\mathbf{r})=Eu_{n\mathbf{k}}(\mathbf{r})\label{eq:uk}
$$

Given a band $$n$$, we can define the Wannier functions

$$
W_{n\mathbf{R}}(\mathbf{r})=\frac{1}{\sqrt{N}}e^{i\mathbf{k}\cdot\mathbf{r}}\sum_{\mathbf{k}}e^{-i\mathbf{k}\cdot\mathbf{R}}u_{n\mathbf{k}}(\mathbf{r})\label{eq:Wannier}
$$

Here $$\mathbf{R}$$ is lattice vector and $$N$$ is the number of primitive
cells in the crystals. The Bloch functions can be written in terms
of the Wannier functions as follows 

$$
u_{n\mathbf{k}}(\mathbf{r})=\frac{1}{\sqrt{N}}\sum_{\mathbf{R}}e^{-i\mathbf{k}\cdot\mathbf{r}}e^{i\mathbf{k}\cdot\mathbf{R}}W_{n\mathbf{R}}(\mathbf{r})\label{eq:unk}
$$

The Wannier functions in Eq. (\ref{eq:Wannier}) constructed by the
waves $$u_{n\mathbf{k}}(\mathbf{r})$$ is not unique due to a gauge
degree of freedom in $$u_{n\mathbf{k}}(\mathbf{r})$$. Namely, when
a phase change in $$u_{n\mathbf{k}}(\mathbf{r})\rightarrow u_{n\mathbf{k}}(\mathbf{r})e^{i\phi_{n\mathbf{k}}}$$
in Eq.~(\ref{eq:solution}), $$\psi_{n\mathbf{k}}(\mathbf{r})$$ stays
as an eigenstate to the Schroedinger equation in Eq.(\ref{eq:bloch}).We
can find the optimally localized Wannier functions by minimizing the
quadratic spread 

$$
\begin{align}
\langle r^{2}\rangle-\langle r\rangle^{2} & \equiv\int_{\mathcal{A}_{uc}}d\mathbf{r}W_{\mathbf{0}}^{*}(\mathbf{r})r^{2}W_{\mathbf{0}}(\mathbf{r})-\left[\int_{\mathcal{A}}d\mathbf{r}W_{\mathbf{0}}^{*}(\mathbf{r})\mathbf{r}W_{\mathbf{0}}(\mathbf{r})\right]^{2}\\
 & \geq\frac{\mathcal{A}_{uc}}{(2\pi)^{d}}\int_{\mathrm{BZ}}d\mathbf{k}\mathrm{Tr}g(\mathbf{k})
\end{align}
$$

with $$\mathcal{A}_{uc}$$ denotes a unit cell. Here $$g(\mathbf{k})$$
is the quantum metric with components

$$
g_{ab}(\mathbf{k})=\mathrm{Re}\langle\partial_{a}u_{n\mathbf{k}}\vert\left(1-\vert u_{n\mathbf{k}}\rangle\langle u_{n\mathbf{k}}\vert\right)\vert\partial_{b}u_{n\mathbf{k}}\rangle
$$

The average quantum metric appears as the lower bound of the quadratic
spread which is gauge-independent. 

## Bound state at impurity

Here we consider an impurity along with the periodic potential. We
focus on one spatial dimensional system The Schroedinger equation
is

$$
\left[-\frac{\hbar}{2m}\frac{d^{2}}{dx^{2}}+V(x)-V_{0}\delta(x)\right]\psi(x)=E\psi(x)
$$

Here $$m_{0}$$ is the mass of the electron and one should not confuse it
with an effective mass of an energy band. 

We are interested in a bound state that is trapped by the impurity.
To solve the bound state, we can consider the Schroedinger equation
in Eq.~(\ref{eq:bloch}) with boundary condition 

$$
\psi(\infty)=0
$$

We assume a wave function ansatz

$$
\psi_{\lambda}(x)=e^{-\lambda x}u_{\lambda}(x)
$$

It is easy to find that $$u_{\lambda}(x)$$ satisfies the equation 

$$
\left[-\frac{\lambda^{2}}{2m}+V(x)\right]u_{\lambda}(x)=E_{n\lambda}u_{\lambda}(x)\label{eq:enl}
$$

which has the same form as in Eq. (\ref{eq:uk}). Therefore, we can
apply the Bloch theorem 

$$
u_{n\lambda}(x)=\frac{1}{\sqrt{N}}\sum_{R}e^{-i\lambda x}e^{i\lambda R}W_{nR}(x)\label{eq:u_l}
$$

Here we also introduce the index $$n$$. We have the one-to-one
correspondence between Eqs. (\ref{eq:u_l}) and (\ref{eq:unk}). The
eigen energy in Eq. (\ref{eq:enl}) is 

$$
\begin{align}
E_{n\lambda} & =-\frac{\lambda^{2}}{2m}+\sum_{\delta}e^{-i\lambda\delta}t(\delta)\nonumber \\
 & =-\frac{\lambda^{2}}{2m}+t(0)+2\mathrm{Re}\left[e^{-i\lambda a}t(a)\right]+2\mathrm{Re}\left[e^{-i2\lambda a}t(2a)\right]+\cdots
\end{align}
$$

with $$\delta=0,\pm a,\pm2a,\cdots$$ and

$$
t(\delta)=\int_{0}^{a}dxW_{R}(x)V(x)W_{R+\delta}^{*}(x)
$$

If the profile of $$W_{R}(x)$$ exponentially decays, the hopping integral
$$t(\delta)$$ decays exponentially as $$\delta$$ increases. Noting that
$$E_{n\lambda=0}>E_{n\lambda>0}$$, we can conclude that the bound states
have the energy lower than $$\sum_{\delta}e^{-i\lambda\delta}t(\delta)$$
while a scattering scattering state is larger than $$\sum_{\delta}e^{-i\lambda\delta}t(\delta)$$
given a band $$n$$.

For the impurity problem, we can construct the wave function 

$$
\begin{align}
\psi_{n\lambda}(x)= & \begin{cases}
\frac{1}{\sqrt{N}}e^{-\lambda x}u_{n\lambda}(x) & x\geq0\\
\frac{1}{\sqrt{N}}Ae^{-\lambda\vert x\vert}u_{n\lambda}(x) & x<0
\end{cases}
\end{align}
$$

At the $$x=0$$, we have the condition 

$$
\begin{align}
\psi_{n}(0^{+}) & =\psi_{n}(0^{-})\\
-\frac{1}{2m}\left[\psi^{\prime}(0^{+})-\psi^{\prime}(0^{-})\right] & =V_{0}\psi(0)
\end{align}
$$

which gives rise to

$$
\begin{align}
\lambda & =mV_{0}\\
A & =1
\end{align}
$$

Therefore we have solution 

$$
\begin{align}
\psi_{n\lambda}(x) & =\frac{1}{\sqrt{N}}e^{-\lambda\vert x\vert}u_{n\lambda}(x)\\
 & =\frac{1}{\sqrt{N}}e^{-\lambda\vert x\vert}e^{-i\lambda\cdot x}\sum_{R}e^{i\lambda R}W_{R}(x)\label{eq:psi_n}
\end{align}
$$

where $$N$$ is the normalization factor and the factor $$e^{-i\lambda\cdot x}$$
is to ensure the orthogonality of the wave functions $$\psi_{n\lambda}(x)$$
of bound states.

The question arises: what Wannier basis should we choose? In fact,
we can take the form in Eq. (\ref{eq:psi_n}) as a wave function ansatz
given a parameter $$\lambda$$. The choice on the Wannier functions
should minimize the energy of the bound state, or the energy $$E_{n0}=\sum_{\delta}e^{-i\lambda\delta}t(\delta)=\sum_{\delta}e^{-i\lambda\delta}\int_{0}^{a}dxW_{R}(x)V(x)W_{R+\delta}^{*}(x)$$.
We can expect that the more localized the Wanner functions are, the
lower energy the ansatz state possesses. As we mention above, the optimal localized
Wannier function is related to the quantum metric which is gauge independent. 

Furthermore, due the to localized property of Wannier function, the
leading contribution to the $$\psi_{n\lambda}(x)$$ in Eq. (\ref{eq:psi_n})
is 

$$
\psi_{n\lambda}(x)=\frac{1}{\sqrt{N}}e^{-\lambda\vert x\vert}e^{-i\lambda\cdot x}W_{0}(x)
$$

with $$\lambda=mV_{0}$$.We can consider a process in which we can adiabatically
weaken the impurity strength $$V_{0}=0$$, the bound state will exclusively
be controlled by the Wannier function. It is consistent with the property
of Wannier functions which can be taken as the bound states that depends
on the local profile of the periodic potential. 

We emphasize that $$m$$ here is the bare mass of the electron. An effective
mass of the band $$n$$ can be extracted as 

$$
\begin{align}
\frac{1}{m_{eff}} & =\frac{d^{2}}{dk^{2}}E_{nk}\vert_{k\rightarrow0}=\frac{1}{m}-\delta^{2}\sum_{\delta}t(\delta)
\end{align}
$$

We can consider the leading orders and for a flat band, we have the
constraint 

$$
\frac{1}{m_{eff}}=\frac{1}{m}-a^{2}\left[t(a)+t(-a)\right]=0
$$
which can be met by tuning the hopping integral $$t(\delta)$$. 
