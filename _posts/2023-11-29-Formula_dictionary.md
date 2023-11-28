---
layout: post
title: "Formula reference"
date: 2023-11-29
excerpt: "Summarize the common formula"
tags: [General Physics]
comments: true
---

[toc]

# Bogoliubov transformation


## Basics for bosons

* Bogoliubov transformations are __linear transformation__ of creation/annihilation operators that __preserve the algebraic relations among them__. In the following, we deal with bosons that satisfies canonical communication. 

  As a fact, generally, a Bogoliubov transformation $U$ is not unitary $$U^\dagger\neq U^{-1}$$.  Let us consider a general model with 

  $$
  H= a^\dagger a +b^\dagger b +\gamma a^\dagger b^\dagger +\gamma a b
  $$

  where operators $a$ and $b$ are bosonic operators that satisfy canonical communication relation 

  $$
  [a,a^\dagger]=1,[b,b^\dagger]=1
  $$

  Our aim is to find new quasiparticles $$\alpha,\beta$$ under which $H$ is in a diagonal form. The first piece of requirement is to preserve the bosonic relation. Suppose 

  $$
  \begin{align}
  \alpha& =M_{11}a+M_{12}b^\dagger \\
  \beta^\dagger&=M_{21}a+M_{22}b^\dagger
  \end{align}
  $$

  Then 

  $$
  \begin{align}
  [\alpha,\alpha^\dagger]&=[M_{11}a,M_{11}^*a^\dagger]+[M_{12}b^\dagger,M_{12}^*b]\notag \\
    &=|M_{11}|^2-|M_{12}|^2=1 \\
    [\beta,\beta^\dagger]&=|M_{22}|^2-|M_{11}|^2=1
  \end{align}
  $$

  When formulated into matrix form

  $$
  h=\begin{pmatrix} 
   \epsilon_0 & \Delta \\
   \Delta^* & \epsilon_0
  \end{pmatrix}
  $$
  

The eigenenergy appears as a solution to the equation

$$
\mathrm{Det}\left[\begin{pmatrix}\lambda & 0 \\ 
                                0 & -\lambda    \end{pmatrix} 
                                -h\sigma_z\right]=0
$$

which  yields  the spectrum function for the canonical modes $$\alpha,\beta$$

$$
\lambda_{1,2}= \sqrt{\epsilon^2-|\Delta|^2}
$$

Further, one may write down the Bogoliubov transformation

$$
\begin{align}
\alpha & = \sqrt{\frac{\epsilon_0-\lambda}{2\epsilon_0}} a +e^{-\theta}\sqrt{\frac{\lambda+\epsilon_0}{2\epsilon_0}}b^\dagger \\
\beta & = e^{i\theta}\sqrt{\frac{\lambda+\epsilon_0}{2\epsilon_0}} a + \sqrt{\frac{\epsilon_0-\lambda}{2\epsilon_0}}b^\dagger
\end{align}
$$

where $$\Delta=|\Delta|e^{i\theta}$$. As matter of fact, the case we often meet is that $$a_{k},a_{-k}^\dagger$$ in the original Hamiltonian, in which, we have 

$$
\begin{align}
\alpha_k & = \sqrt{\frac{\epsilon_0-\lambda}{2\epsilon_0}} a_k +e^{-\theta}\sqrt{\frac{\lambda+\epsilon_0}{2\epsilon_0}}a_{-k}^\dagger \\
\alpha^\dagger_{-k} & = e^{i\theta}\sqrt{\frac{\lambda+\epsilon_0}{2\epsilon_0}} a_{k} + \sqrt{\frac{\epsilon_0-\lambda}{2\epsilon_0}}a_{-k}^\dagger
\end{align}
$$


> ==Remark==
>
> For  a quantum field theory, the diagnolization procedures have some sublattices compared with the case above. For example, a scalar field with Hamiltonian 
>
> $$
> \mathcal L = \frac{1}{2}\partial_0 \phi \partial _0\phi-\frac{1}{2}\nabla\phi\nabla\phi
> $$
>
> has a quadratic time derivative. __However, in such a system, a unitary transformation cannot  diagonalize it__. Of course, one may introduce canonical creation and annihilation operators with the time derivative of order 1. We first derive the canonical quantization relation 
>
> $$
> \pi =\frac{\delta\mathcal L}{\delta \partial_0\phi}= \partial_0\phi 
> $$
>
> which the Hamiltonian 
>
> $$
> H=\pi \partial_0\phi-L=\frac{1}{2}(\pi^2+\nabla\phi\nabla\phi)
> $$
>
> We introduce the raising and lowering operators
>
> $$
> \begin{align}
> a^\dagger &=\frac{1}{\sqrt{2|\mathbf k|}}(\pi+i|\mathbf k|\phi)\\
> a &=\frac{1}{\sqrt{2|\mathbf k|}}(\pi-i|\mathbf k|\phi)
> \end{align}
> $$
>
> which gives the Hamiltonian
>
> $$
> H=|\mathbf k|a^\dagger(\mathbf k)a(\mathbf k)+\frac{1}{2}|\mathbf k|
> $$
>
> Another example is the QED for which one has to introduce
>
> $$
> A_i(k)= \frac{\xi_i(k)}{\sqrt{\mathbf k^2}}(a_\mathbf k^\dagger+ia_\mathbf k)
> $$
>
> with $$\xi_i(\mathbf k)$$ being the polarized vector. 
> 

## Basic Fermion

The case for a system of fermions are much simple and we can just apply the unitary transformation which perserves the anticommunication relation. Here we present the transformations.
Consider a BdG Hamiltonian  (__Please double check the sign before the order parameter!!!__)

$$
\begin{align}
\mathcal{H}_{\mathrm{MF}} &=\sum_{k, \alpha} \xi_{k} c_{k, \alpha}^{\dagger} c_{k, \alpha}-\sum_{k}^{\prime}\left[\Delta e^{-i \varphi} c_{k, \uparrow} c_{-k, \downarrow}+\Delta e^{i \varphi} c_{-k, \downarrow}^{\dagger} c_{k, \uparrow}^{\dagger}\right]+\frac{V_{\mathrm{vol}} \Delta^{2}}{g} \\
&=\sum_{k}\left[c_{k, \uparrow}^{\dagger}, c_{-k, \downarrow}\right]\left[\begin{array}{cc}
\xi_{k} & \Delta e^{i \varphi} \\
\Delta e^{-i \varphi} & -\xi_{k}
\end{array}\right]\left[\begin{array}{c}
c_{k, \uparrow} \\
c_{-k, \downarrow}^{\dagger}
\end{array}\right]+\frac{V_{\mathrm{vol}} \Delta^{2}}{g}
\end{align}
$$

Then 

$$
E_{k}=\sqrt{\xi_{k}^{2}+\Delta^{2}}, \quad u_{k}=\sqrt{\frac{1}{2}\left(1+\frac{\xi_{k}}{E_{k}}\right)}, \quad v_{k}=\sqrt{\frac{1}{2}\left(1-\frac{\xi_{k}}{E_{k}}\right)}
$$

with 

$$
\begin{align}
&{\left[\begin{array}{c}
\gamma_{\boldsymbol{k}, \uparrow} \\
\gamma_{-\boldsymbol{k}, \downarrow}^{\dagger}
\end{array}\right]=\left[\begin{array}{cc}
u_{\boldsymbol{k}} & -v_{\boldsymbol{k}} e^{i \varphi} \\
v_{\boldsymbol{k}} e^{-i \varphi} & u_{\boldsymbol{k}}
\end{array}\right]\left[\begin{array}{c}
c_{\boldsymbol{k}, \uparrow} \\
c_{-\boldsymbol{k}, \downarrow}^{\dagger}
\end{array}\right],} \\
&{\left[\begin{array}{c}
c_{\boldsymbol{k}, \uparrow} \\
c_{-\boldsymbol{k}, \downarrow}^{\dagger}
\end{array}\right]=\left[\begin{array}{cc}
u_{\boldsymbol{k}} & v_{\boldsymbol{k}} e^{i \varphi} \\
-v_{\boldsymbol{k}} e^{-i \varphi} & u_{\boldsymbol{k}}
\end{array}\right]\left[\begin{array}{c}
\gamma_{\boldsymbol{k}, \uparrow} \\
\gamma_{-\boldsymbol{k}, \downarrow}^{\dagger}
\end{array}\right] .}
\end{align}
$$


Then we obtain the diagonalized Hamiltonian 

$$
\mathcal H_\mathrm{MF} = \sum_k (E_k\gamma_{k,\uparrow}^\dagger\gamma_{k,\uparrow }-E_k\gamma_{-k,\downarrow}\gamma_{-k,\downarrow}^\dagger)+\frac{V_\mathrm{vol}\Delta^2}{g}
$$

and the according BCS can be constructed as 

$$
|\mathrm{BCS}\rangle = \prod_k\gamma_{k,\uparrow}\gamma_{k\downarrow}|\Omega\rangle\sim\prod_{k}(u_k+v_k c_{k,\uparrow}^\dagger c_{-k\downarrow}^\dagger)|\Omega\rangle
$$

with $$|\Omega\rangle$$ being the vacuum i.g. a Fermi sea with a Fermi surface. 
We can expect it for any $$ k,\sigma$$, with

$$
\gamma_{k,\sigma}|\mathrm{BCS}\rangle =0
$$

With the BCS ground state, one can evaluate the expectation value 

$$
\begin{align}
& \langle c^\dagger_{k,\uparrow}c_{k,\uparrow}\rangle=\langle c^\dagger_{k,\downarrow}c_{k,\downarrow} \rangle = \upsilon_k^2  \\ 
& \langle c^\dagger_{k,\uparrow}c^\dagger_{-k,\downarrow}\rangle = u_k v_k
\end{align}
$$

# Matsubara Summation 

**Pair Correlation function $$\chi_{n,\mathbf q}^c$$**

A building block enters the calculation of the Cooper pair propagator
>
> $$
>\begin{align}
> \chi_{n, \mathbf{q}}^{\mathrm{c}} \equiv-\frac{T}{L^{d}} \sum_{m, \mathbf{p}} G_{0}\left(\mathbf{p}, i \omega_{m}\right) G_{0}\left(-\mathbf{p}+\mathbf{q},-i \omega_{m}+i \omega_{n}\right) \\
> =\frac{1}{L^{d}} \sum_{\mathbf{p}} \frac{1-n_{\mathrm{F}}\left(\xi_{\mathbf{p}}\right)-n_{\mathrm{F}}\left(\xi_{-\mathbf{p}+\mathbf{q}}\right)}{i \omega_{n}-\xi_{\mathbf{p}}-\xi_{-\mathbf{p}+\mathbf{q}}}
>\end{align}
> $$
>
> 

where (around the transition point)

$$
G_0(\mathbf p,i\omega_m)=\frac{1}{i\omega_m-\xi_\mathbf p}
$$

and $$\omega_m = (2m+1)\pi T $$ are **fermionic Matsubara frequencies**,
while $$\omega_n =2\pi nT$$ is a **bosonic Matsubara frequency**. 

**Density-Density response function $$\chi^d_{\mathbf q,\omega_n}$$**

>
> $$
>\begin{align}
>& \chi_{\mathbf{q}, \omega_{n}}^{\mathrm{d}} \equiv-\frac{T}{L^{d}} \sum_{\mathbf{p}, \omega_{m}} G_{0}\left(\mathbf{p}, i \omega_{m}\right) G_{0}\left(\mathbf{p}+\mathbf{q}, i \omega_{m}+i \omega_{n}\right) \\
>= & -\frac{1}{L^{d}} \sum_{\mathbf{p}} \frac{n_{\mathrm{F}}\left(\xi_{\mathbf{p}}\right)-n_{\mathrm{F}}\left(\xi_{\mathbf{p}+\mathbf{q}}\right)}{i \omega_{n}+\xi_{\mathbf{p}}-\xi_{\mathbf{p}+\mathbf{q}}}
>\end{align}
> $$
>
> 

In real calculation, we often take the static limit. That is 
>
> $$
>(\mathbf q,\omega_n)\rightarrow (\mathbf q,0)
> $$
>

It is convenient to change from an explicit matrix representation of the Gorkov Green function to an expression in terms of the Pauli matrices

$$
\mathcal G_{0,p}=\frac{1}{i\sigma_0\omega_n-\sigma_3 \xi_p+\sigma_1\Delta_0}=\frac{-i\sigma_0\omega_n-\sigma_3\xi_p+\sigma_1\Delta_0}{\omega_n^2+\xi_p^2+\Delta_0^2}
$$

where the Gorkov Green function takes the form as 

$$
\mathcal G^{-1}=\begin{pmatrix}-\partial_\tau-i\phi-\frac{1}{2m}(-i\nabla-\mathbf A)^2+\mu & \Delta_0e^{2i\theta} \\
\Delta_0e^{-2i\theta} & -\partial_\tau +i\phi +\frac{1}{2m}(-i\nabla-\mathbf A)-\mu
\end{pmatrix}
$$

On the other hand we have the expansion 

$$
\begin{align}
\mathcal G^{-1} & =-\sigma_0\partial_\tau-\sigma_3 (i\phi+\frac{1}{2m}(-i\nabla-\sigma_3\mathbf A)^2-\mu)+\sigma_1\Delta_0 \\
& =-\sigma_0\partial_\tau -\sigma_3 (-\frac{\nabla^2}{2m}-\mu)+\sigma_1\Delta_0-i\sigma_3\phi+\frac{i}{2m}\sigma_0[\nabla,\mathbf A]_+-\sigma_3\frac{1}{2m}\mathbf A^2
\end{align}
$$

> * Gorkov Green function 
>
>   $$
>   \begin{align}
>   G_{0,p} & =\frac{u_k^2}{\omega - \epsilon_k}+\frac{v_k^2}{\omega+\epsilon_k}\\
>   F_{0,p} & =u_kv_k\frac{2\omega}{\omega^2+\epsilon_k^2}
>   \end{align}
>   $$
>





## Conventions for Fourier transformation

* Fermionic operator (N is the lattice number)
  >
  >$$
  >\begin{align}
  >c(r)&=\frac{1}{\sqrt{N}}\sum_{k}c_{k}e^{ik\cdot r}\\
  >c(k)&=\frac{1}{\sqrt{N}}\sum_{r}c(r)e^{-ik\cdot r}
  >\end{align}
  >$$
  >

* Order parameter formed by two Fermion operator

  > For the superconducting order parameter  $$\Delta(r)=c_\uparrow(r)c_\downarrow(r) $$
  >
  > $$
  > \Delta (k) = \sum_r \Delta(r)e^{ik\cdot r}
  > $$
  >

* Function
  >
  > $$
  > \begin{align}
  > f(r)	&=\sum_{k}f(k)e^{ik\cdot r} \\
  > f(k)	&=\frac{1}{N}\sum_{r}f(r)e^{-ik\cdot r}
  > \end{align}
  > $$
  >
  > 
