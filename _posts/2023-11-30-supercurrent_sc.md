---
layout: post
title: "Supercurrent from a mean-field theory in superconductivity"
date: 2023-11-30
excerpt: "Why is supercurrent supercurrent?"
tags: [Superconductivity]
comments: true
---

One of the remarkable features of a superconductor is the Meissner effect, which states that a current can flow through the sample without any dissipation. This phenomenon gives rise to what we call supercurrents, which occur due to a coherent effect.
In contrast to the normal phase, or the Fermi liquid, where the current is more like a local property resulting from electron scattering with disorder or impurities, superconductors exhibit a different behavior. Interestingly, in the case of a simple s-wave superconductor, the normal phase and superconducting phase share the same current operator.

We consider a spinful Fermi gas with density-density interaction,

$$
\begin{align}
H & =\sum_{k\sigma}\xi(k)c_{k\sigma}^{\dagger}c_{k\sigma}-\int drUc_{\uparrow}^{\dagger}(r)c_{\downarrow}^{\dagger}(r)c_{\downarrow}(r)c_{\uparrow}(r)\\
 & =\sum_{k\sigma}\xi(\mathbf{k})c_{\mathbf{k}\sigma}^{\dagger}c_{\mathbf{k}\sigma}-\frac{U}{V}\sum_{kk^{\prime}q}c_{\mathbf{k}\uparrow}^{\dagger}c_{-\mathbf{k}+\mathbf{q}\downarrow}^{\dagger}c_{-\mathbf{k}^{\prime}+\mathbf{q}\downarrow}c_{\mathbf{k}\prime\uparrow}
\end{align}
$$

The interaction is a uniform density-density interaction, and we do
not expect a current from it. Therefore, regardless of the real phase, the current operator for electrons always have the form as

$$
\mathbf{j}(\mathbf{k})=\sum_{\sigma}\nabla\xi(\mathbf{k})c_{\mathbf{k}\sigma}^{\dagger}c_{\mathbf{k}\sigma}
$$

One should not confuse the current of an electron with the current of
a quasiparticle. From the Landau's Fermi liquid theory, we can learn
that the current of quasiparticles can get renormalized by interaction
or orbital hybridization.

We can apply the mean-field theory to obtain an ansatz for a ground
state. We can make a mean-field ansatz by assuming 

$$
\Delta=-\frac{1}{V}\int dr\langle c_{\downarrow}(r)c_{\uparrow}(r)\rangle=-\frac{1}{V}\sum_k\langle c_{-\mathbf{k}\downarrow}c_{\mathbf{k}\uparrow}\rangle
$$

Then we obtain a mean-field Hamiltonian $$H_{MF}$$

$$
H_{MF}(\mathbf{k})=\sum_{\sigma}\xi(\mathbf{k})c_{\mathbf{k}\sigma}^{\dagger}c_{\mathbf{k}\sigma}+\Delta\left[c_{\mathbf{k}\uparrow}^{\dagger}c_{-\mathbf{k}\downarrow}^{\dagger}+c_{-\mathbf{k}\downarrow}c_{\mathbf{k}\uparrow}\right]
$$

where we make a proper gauge choice such that the order parameter
$$\Delta$$ be a real number. We can diagonalize the mean-field Hamiltonian

$$
H_{MF}(\mathbf{k})=E(\mathbf{k})\left[\gamma_{\mathbf{k}\uparrow}^{\dagger}\gamma_{\mathbf{k}\uparrow}+\gamma_{\mathbf{k}\downarrow}^{\dagger}\gamma_{\mathbf{k}\downarrow}\right]
$$

by the Bogoliubov transformation 

$$
\begin{aligned} & \left[\begin{array}{c}
\gamma_{\boldsymbol{k},\uparrow}\\
\gamma_{-\boldsymbol{k},\downarrow}^{\dagger}
\end{array}\right]=\left[\begin{array}{cc}
u_{\boldsymbol{k}} & -v_{\boldsymbol{k}}\\
v_{\boldsymbol{k}} & u_{\boldsymbol{k}}
\end{array}\right]\left[\begin{array}{c}
c_{\boldsymbol{k},\uparrow}\\
c_{-\boldsymbol{k},\downarrow}^{\dagger}
\end{array}\right],\\
 & \left[\begin{array}{c}
c_{\boldsymbol{k},\uparrow}\\
c_{-\boldsymbol{k},\downarrow}^{\dagger}
\end{array}\right]=\left[\begin{array}{cc}
u_{\boldsymbol{k}} & v_{\boldsymbol{k}}\\
-v_{\boldsymbol{k}} & u_{\boldsymbol{k}}
\end{array}\right]\left[\begin{array}{c}
\gamma_{\boldsymbol{k},\uparrow}\\
\gamma_{-\boldsymbol{k},\downarrow}^{\dagger}
\end{array}\right].
\end{aligned}
$$

with the Bogolibov coefficients 

$$
\begin{align}
u(\mathbf{k}) & =\sqrt{\frac{1}{2}\left(1+\frac{\xi(\mathbf{k})}{E(\mathbf{k})}\right)}\\
v(\mathbf{k}) & =\sqrt{\frac{1}{2}\left(1-\frac{\xi(\mathbf{k})}{E(\mathbf{k})}\right)}
\end{align}
$$

and the dispersion of quasiparticle $$E(\mathbf{k})=\sqrt{\xi^{2}(\mathbf{k})+\Delta^{2}}$$.
Accordingly the ground state is 

$$
\vert\mathrm{BCS}\rangle=\prod_{\mathbf{k}}(u(\mathbf{k})+v(\mathbf{k})c_{\mathbf{k}\uparrow}^{\dagger}c_{-\mathbf{k}\downarrow}^{\dagger})\vert0\rangle
$$

It is easy to check $$\gamma_{\mathbf{k}\sigma}\vert\mathrm{BCS}\rangle=0$$.
The BCS ground state represents a condensation of Cooper pairs.
The net momentum of a Cooper pair vanishes and thus we expect the current
vanishes

$$
\begin{align}
\langle\mathrm{BCS}\vert J\vert\mathrm{BCS}\rangle & =\sum_{\mathbf{k}}\langle\mathrm{BCS}\vert\mathbf{j}(\mathbf{k})\vert\mathrm{BCS}\rangle\\
 & =\sum_{\mathbf{k}}v^{2}(\mathbf{k})(\nabla\xi(\mathbf{k})-\nabla\xi(\mathbf{k}))=0
\end{align}
$$


We need an excited state to show the supercurrents. There are two types
of excitations. The first one is the Fermionic Bogolibov quasiparticle
$$\gamma_{\mathbf{k}\sigma}^{\dagger}\vert\mathrm{BCS}\rangle$$ with
an energy $$E=E_{GS}+E(\mathbf{k})$$. It has a finite energy gap. In
fact, we have the second type of excitation, that is the gapless Bosonic
Goldstone mode. By contrast it will cost at least energy $$2\Delta$$ to
create a Cooper pair state $$\gamma_{\mathbf{k}\uparrow}^{\dagger}\gamma_{\mathbf{-k}\downarrow}^{\dagger}\vert\mathrm{BCS}\rangle$$,
which can be taken as local excitations (in momentum space). Instead, to pursue the Goldstone
mode, we can consider a new mean-field ansatz

$$
\Delta_{\mathbf{q}}=\frac{1}{V}\sum_k\langle c_{-\mathbf{k}\downarrow}c_{\mathbf{k}+\mathbf{q}\uparrow}\rangle
$$

or in the real space 

$$
\begin{align}
\Delta_{\mathbf{q}} & =\int dre^{i\mathbf{q}\cdot\mathbf{r}}\langle c_{\downarrow}(\mathbf{r})c_{\uparrow}(\mathbf{r})\rangle
\end{align}
$$

Then we have the mean-field Hamiltonian 

$$
H_{\mathbf{q}}(\mathbf{k})=\xi(\mathbf{k}+\mathbf{q})c_{\mathbf{k}+\mathbf{q}\uparrow}^{\dagger}c_{\mathbf{k}+\mathbf{q}\uparrow}+\xi(\mathbf{k})c_{-\mathbf{k}\uparrow}^{\dagger}c_{-\mathbf{k}\uparrow}+\Delta_{\mathbf{q}}^{*}c_{\mathbf{k}+\mathbf{q}\uparrow}^{\dagger}c_{-\mathbf{k}\downarrow}^{\dagger}+\Delta_{\mathbf{q}}c_{-\mathbf{k}\downarrow}c_{\mathbf{k}+\mathbf{q}\uparrow}
$$

Also we can act the Bogoliubov transformation 

$$
\begin{align}
u_{\mathbf{q}}(\mathbf{k}) & =\sqrt{\frac{1}{2}\left(1+\frac{\xi(\mathbf{k}+\mathbf{q})+\xi(\mathbf{k})}{2\epsilon_{\mathbf{q}}(\mathbf{k})}\right)}\\
v_{\mathbf{q}}(\mathbf{k}) & =\sqrt{\frac{1}{2}\left(1-\frac{\xi(\mathbf{k}+\mathbf{q})+\xi(\mathbf{k})}{2\epsilon_{\mathbf{q}}(\mathbf{k})}\right)}
\end{align}
$$

with a quasiparticle dispersion $$E_{\mathbf{q\pm}}(\mathbf{k})$$

$$
\begin{align}
E_{\mathbf{q\pm}}(\mathbf{k}) & =\sqrt{\left(\frac{\xi(\mathbf{k}+\mathbf{q})+\xi(\mathbf{k})}{2}\right)^{2}+\vert\Delta_{\mathbf{q}}\vert^{2}}\pm\frac{\xi(\mathbf{k}+\mathbf{q})-\xi(\mathbf{k})}{2}\\
 & \equiv\epsilon_{\mathbf{q}}(\mathbf{k})\pm\frac{\xi(\mathbf{k}+\mathbf{q})-\xi(\mathbf{k})}{2}
\end{align}
$$

Similarly, we have the ground state 

$$
\vert\mathrm{BCS}(\mathbf{q})\rangle=\prod_{\mathbf{k}}(u_{\mathbf{q}}(\mathbf{k})+v_{\mathbf{q}}(\mathbf{k})c_{\mathbf{k}+\mathbf{q}\uparrow}^{\dagger}c_{-\mathbf{k}\downarrow}^{\dagger})\vert0\rangle
$$

When $$\mathbf{q}$$ approaches $$0$$, the state $$\vert\mathrm{BCS}(\mathbf{q})\rangle$$
reduces to $$\vert\mathrm{BCS}\rangle$$.Now let us evaluate the current
operator 

$$
\begin{align}
\langle\mathrm{BCS(\mathbf{q})}\vert\mathbf{J}\vert\mathrm{BCS(\mathbf{q})}\rangle & =\sum_{\mathbf{k}}\langle\mathrm{BCS(\mathbf{q})}\vert\mathbf{j}(\mathbf{k})\vert\mathrm{BCS(\mathbf{q})}\rangle\\
 & =\sum_{\mathbf{k}}\langle\mathrm{BCS(\mathbf{q})}\vert\sum_{\sigma}\nabla\xi(\mathbf{k})c_{\mathbf{k}\sigma}^{\dagger}c_{\mathbf{k}\sigma}\vert\mathrm{BCS(\mathbf{q})}\rangle\\
 & =\sum_{\mathbf{k}}\left(\nabla\xi(\mathbf{k}+\mathbf{q})-\nabla\xi(\mathbf{k})\right)v_{\mathbf{q}}^{2}(\mathbf{k})
\end{align}
$$

If the $$\mathbf{q}$$ is vanishingly small, we can assume $$\Delta_{\mathbf{q}}=\Delta$$
or 

$$
\Delta_{\mathbf{q}}(\mathbf{r})=\Delta e^{i\mathbf{q}\cdot\mathbf{r}}
$$

By noting 

$$
\begin{align}
\epsilon_{\mathbf{q}}(\mathbf{k}) & =\sqrt{\left(\frac{\xi(\mathbf{k}+\mathbf{q})+\xi(\mathbf{k})}{2}\right)^{2}+\vert\Delta_{\mathbf{q}}\vert^{2}}\\
v_{\mathbf{q}}^{2}(\mathbf{k}) & =v^{2}(\mathbf{k})+\mathcal{O}(q)
\end{align}
$$

we can approximate 

$$
\langle\mathrm{BCS(\mathbf{q})}\vert J_{a}\vert\mathrm{BCS(\mathbf{q})}\rangle=\sum_{\mathbf{k}}\sum_{b}q_{b}\partial_{b}\partial_{a}\xi(\mathbf{k})v^{2}(\mathbf{k})
$$


$$
\begin{align}
\langle\mathrm{BCS(\mathbf{q})}\vert j_{a}\vert\mathrm{BCS(\mathbf{q})}\rangle & =\sum_{\mathbf{k}}\left(\nabla\xi(\mathbf{k}+\mathbf{q})-\nabla\xi(\mathbf{k})\right)v_{\mathbf{q}}^{2}(\mathbf{k})\\
 & =\frac{q_{a}}{m}\sum_{\mathbf{k}}v^{2}(\mathbf{k})=\frac{q_{a}}{m}n_{s}
\end{align}
$$

where $$n_{s}$$ is the superfluid stiffness, 

$$
n_{s}=\sum_{\mathbf{k}}v^{2}(\mathbf{k})
$$

and the superfluid weight is 

$$
D_{s}=\frac{n_{s}}{m}
$$

The supercurrent in a superconductor is considered global because it involves the integral over all momentum states. In other words, the state represented by $$ \vert \mathrm{BCS}(\mathbf q)\rangle$$, which consists of Bogoliubov quasiparticles, undergoes a change in its wave function throughout the entire system, indicating a global excitation.

In contrast, in a Fermi liquid theory, when an electron is excited from the Fermi surface, it carries charge currents that involve only a single momentum point on the Fermi surface. Therefore, we can consider this type of current as local, as it is confined to a specific region or point in the system.
