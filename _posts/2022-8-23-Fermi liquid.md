---
layout: post
title: "Fermi liquid theory"
date: 2022-8-23
excerpt: "Fermi liquid is a classical theory on interacted electron gas"
tags: [Fermi liquid]
comments: true
---

* toc
{:toc}

# Introduction to Fermi liquid and Fermi liquid theory

Fermi liquid theory is a general theoretical framework (an effective field theory) describing the behavior of interacting fermion systems at low temperature. The random-phase approximation (RPA) and the corresponding excitation spectra are consistent with Fermi liquid behavior. In RPA, the electronic excitation spectrum consists of two pairs: collective and single particle-hole pair excitations. The particle-hole pair excitations spectrum is basically the same as the corresponding spectrum for non-interacting particles. 

Fermi liquid theory is a theoretical framework that justifies this qualitative behavior, at least when the excitation energy is low. The basic assumption of Fermi liquid theory is ==adiabaticity==, meaning that there is a one-to-one correspondence between  the ground state and low-energy excitation spectrum of fermions in the absence and in the presence of (repulsive) interactions. (Attractive interaction is excluded to avoid Cooper instability).

As a consequence of the assumption, __the low-energy particle-hole excitation spectrum can basically be labeled by the same quantum number as for non-interacting fermions and the natures of the excitations are qualitatively similar__. To capture this physics, Landau introduced the concept of quasiparticles.

Landau imagined that the ground state of an interacting fermion liquid can be labeled as filled Fermi gas of non-interacting fermions. __In the presence of interaction, these fermions are not the same as the original fermions in the problem. __ Landau imagined them as __the original free fermions dressed by the interaction and called them quasi-particles__. The energy of the system can be written in terms of the occupation number of quasi-particles $$n_\mathbf k$$. In particular, the ground state energy as a functional of the density distribution is,  

$$
E_G = E[\{n_\mathbf k=\theta(k_F-|k|\}],
$$

which corresponds to a filled Fermi sea. 

Low-energy excitations can be labeled by small changes in the occupation number of quasi-particles, 
$$n_\mathbf k=\theta(k_F - |k|)+\delta n_\mathbf k $$. Assuming that $$\delta n_\mathbf k$$ is small, Landau expanded the energy functional to second order, 

$$
E[n_\mathbf k] \sim E_\mathrm G + \sum_\mathbf k \xi_{\mathbf k}^*\delta n_\mathbf k+\frac{1}{2V}\sum_{\mathbf k\mathbf k ^\prime}f_{\mathbf k\mathbf k^\prime}\delta n_\mathbf k \delta n_{\mathbf k^\prime}
$$

where 

$$
\xi_\mathbf k^*\sim \frac{\hbar k_F}{m^*}(|k|-k_F).
$$

Here $$m^* $$ is called the effectiveness and $$f_{\mathbf k\mathbf k^\prime }$$ are called the __Landau parameters__. The form of $$\xi_\mathbf k^* $$ ensures that the ground states (filled Fermi sea) is stable. It recedes to a free fermi gas with $$m^*=m$$ and $$f_{\mathbf k\mathbf k^\prime}=0$$.

Landau next derived the (low-energy) dynamics of the quasi-particles. This is quite  impossible from a microscopic point of view since the nature of the quasi-particles is not specified. __Landau realized that he could bypass this problem if he interpreted the above energy functional as a local Hamiltonian function for classical particles,__ with 

$$
E[n_\mathbf k] \rightarrow E_\mathrm G+ \sum_{\mathbf k}\xi_{\mathbf k}^* \int \delta n_\mathbf k(\mathbf r ) d^d \mathbf r +\frac{1}{2}\sum_{\mathbf k \mathbf k^\prime} \int \delta n_\mathbf k(\mathbf r ) \delta n_{\mathbf k^\prime}(\mathbf r) d^d \mathbf r,
$$

where the dynamics of the distribution function $$\delta n_\mathbf k(\mathbf r )$$ is determined by the classical equation of motion that followed from the Hamiltonian (essentially a Boltzmann equation).  This assumption is justifiable in the $$\mathbf q, \omega\rightarrow 0$$ limit, where the system should become ‘classical’ like (correspondence principle). Recall that the uncertainty principle forbids simultaneous identification of the position and momentum of particles. Therefore, for this description to be valid, the distribution function $$\delta n_\mathbf k(\mathbf r)$$ should not be changing too rapidly in space so that the uncertainty principle is not violated (ie. $$\Delta r\Delta k \geq 1$$). 

As we shall see later, we shall be interested  in states $$\mathbf k ,\mathbf k^\prime$$ in the vicinity of the Fermi surface. In this regime, we may replace $$f_{\mathbf k \mathbf k^\prime} $$ by $$f_{\mathbf k_F \mathbf k_F^\prime} $$, where $$\mathbf k_F$$ are wave vectors on the Fermi surface. For a rotationally symmetric system, we also expect that $$f_{\mathbf k_F \mathbf k_F^\prime}\rightarrow f(\theta) $$, where $$\theta$$ is the angle between the directions $$\mathbf k_F$$ and $$\mathbf k_F^\prime$$. This form of Landau interaction is assumed in most studies of Fermi liquid theory and will be assumed in the following. 

If a particle with momentum $$\mathbf k$$ is located at $$\mathbf r$$ at $$t$$ then, at time $$t+dt$$, it is located at $$\mathbf r +\delta r=\mathbf r +\mathbf v(\mathbf r) dt$$, with momentum $$\mathbf k+ \delta\mathbf  k =\mathbf k + \mathbf F(t)dt$$,

$$
\begin{align}
& n(\mathbf r +\delta \mathbf r,\mathbf k +\delta \mathbf k ,t+\delta t)=n(\mathbf r ,\mathbf k,t) \\
\Rightarrow &\frac{\partial n}{\partial t}+\mathbf v(\mathbf k)\cdot \nabla_\mathbf r n+\mathbf F \cdot \nabla_\mathbf kn=\frac{dn}{dt}=0
\end{align}
$$

To complete the equation, we have to determine the velocities $$\mathbf v(\mathbf r )$$ and forces $$\mathbf F(t)$$ from the Landau Fermi liquid theory. They are given in classical mechanism by 

$$
\mathbf v(\mathbf k )=\frac{\partial \mathcal E(\mathbf k )}{\partial k_i},\mathbf F_i(t)= - \frac{\partial\mathcal E(\mathbf k)}{\partial r_i},
$$

where $$\mathcal E(\mathbf k ) = \xi_\mathbf k^* +\sum_{\mathbf k^\prime}f_{\mathbf k\mathbf k^\prime}\delta n_{\mathbf k^\prime}(\mathbf r) $$. Therefore,  to leading order where $$f_{\mathbf k \mathbf k^\prime}  \rightarrow f_{\mathbf k_F \mathbf k_F^\prime}  $$,

$$
\mathbf v(\mathbf r) = \frac{\partial \xi_\mathbf k^*}{\partial \mathbf k } =\frac{\hbar \mathbf k_F }{m^*}, \quad \mathbf F(t) = - \sum_{\mathbf k^\prime} f_{\mathbf k_F \mathbf k_F^\prime}\nabla_\mathbf r n_{\mathbf k^\prime }(\mathbf r)
$$

Writing $$n_\mathbf k (\mathbf r, t )=n_F(\mathbf k)+\delta n_\mathbf k(\mathbf r ,t)$$ where $$n_F$$ is the equilibrium Fermi distribution, the Boltzmann equation becomes,

$$
\frac{\partial \delta n_\mathbf k(\mathbf k,t)}{\partial t}+\mathbf v_\mathbf k\cdot \nabla _\mathbf r \delta n_\mathbf k(\mathbf r ,t)+\delta(\xi_\mathbf k^*)\sum_{\mathbf k^\prime} f_{\mathbf k\mathbf k^\prime}\mathbf v_{\mathbf k^\prime}\cdot \nabla_\mathbf r\delta n_{\mathbf k^\prime}(\mathbf r,t)=0
\label{coneq}
$$

To linear order in $$\delta n $$, where we consider $$T\rightarrow 0$$ so that $$n_F(\mathbf k)\sim \theta(-\xi_\mathbf k^*)$$. Note that in this limit, __only states in the vicinity of the Fermi surface are involved in the transport equation. __

> Remark: for the last term in Eq. $$\eqref{coneq}$$, we use 
>
> $$
> \nabla_k n_{\mathbf k}(\mathbf r) =\nabla_\mathbf k n_F(\mathbf k)+\nabla_\mathbf k\delta n_\mathbf k(\mathbf r)\\
> \simeq \nabla_\mathbf k \theta (-\xi_\mathbf k^*)
> =-\mathbf v_\mathbf k(\mathbf r)\delta(\xi_\mathbf k^*)
> $$
>
> Where a $$\delta$$ function emerges because  in the limit $$T\rightarrow 0$$ only electrons at Fermi surface can be excited. 

In this way, Landau derived results that cannot be obtained directly from the quantum energy functional. Note that interactions between quasiparticles represented by the Landau interaction $$f_{\mathbf k\mathbf k^\prime}$$ exist in the transport equation. We shall see later that the interactions are not small and cannot be neglected in general. Therefore, Landau's theory predicts that the low-energy effective theory of Fermi liquids is not a theory of free fermions. Interactions between quasiparticles persist down to zero temperature. The validity and meaning of Landau’s approach were not fully understood until the 1990s when the mathematical techniques of renormalization groups and bosonization mature. 



# Charge and Current carried by quasiparticles

Now we study the charge and current carried by quasi-particles. We expect that the charge carried by a quasiparticle is exactly equal to the charge carried by the original particle because of the basic assumption that there is a one-to-one correspondence between bare particles and quasiparticles and that total charge is conceived. It turns out that the same conclusion cannot be drawn so readily for the current. To see why this is so, we examine the transport equation. Summing the equation over $$\mathbf k$$, we obtain  the continuity equation, 

$$
\frac{\partial \rho(\mathbf r, t)}{\partial t}+\nabla\cdot \mathbf j(\mathbf r,t)=0,
$$

where 

$$
\rho(\mathbf r,t)=\sum_\mathbf k \delta n_\mathbf k(\mathbf r,t).
$$

Is the total charge fluctuation and 

$$
\mathbf j(\mathbf r,t)= \sum_\mathbf k \mathbf v_\mathbf k\delta n_\mathbf k(\mathbf r,t)+\sum_{\mathbf k\mathbf k^\prime}\delta(\xi_{\mathbf k^\prime}^*)f_{\mathbf k^\prime\mathbf k }\mathbf v_{\mathbf k^\prime}\delta n _\mathbf k(\mathbf r,t )=\sum_\mathbf k\mathbf j_\mathbf k\delta n_\mathbf k(\mathbf r,t)
$$

where 

$$
\mathbf j_\mathbf k=\mathbf v_\mathbf k+\sum_{\mathbf k\mathbf k^\prime}\delta (\xi_{\mathbf k ^\prime}^*)f_{\mathbf k^\prime\mathbf k}\mathbf v_{\mathbf k^\prime} 
$$

is by definition the current carried by a quasi-particle. This is quite different from the naive expectation, $$\mathbf j_\mathbf k =\mathbf v_\mathbf k$$ for single quasi-particle. __Note that this result is a consequence of having interaction terms in the transport equation, and is rather independent of quantum mechanics.__ This reason why $$\mathbf j_\mathbf k \neq \mathbf v_\mathbf k$$ is the quasiparticles are never really independent from one another when $$f_{\mathbf k\mathbf k^\prime}\neq 0$$. It is impossible to excite just one quasiparticle without creating a cloud of other quasiparticles surrounding it. You can imagine the situation of a man trying to push his way through a crowd of people, When he pushes through the crowd, people in his way will all be affected and have  to move  away a little bit. This phenomenon is called __backflow__ in the study of fluids. In mathematical terms, one has to distinguish a quasiparticle from an elementary excitation, which is what is physically excited in the system.

> An elementary excitation =  a quasi-particle + crowd of other quasi-particles around it. 

The crowd also contributes to the total current carried by the elementary excitation and is responsible for the $$\sum_{\mathbf k \mathbf k^\prime}\delta(\xi_{\mathbf k^\prime}^*)f_{\mathbf k^\prime \mathbf k}\mathbf v_{\mathbf k^\prime}$$ factor. 

For a translationally invariant system, another interesting result occurs. First, we recall that quasiparticles and bare particles carry the same charge, and __the quasiparticle density $$\rho(\mathbf r ,t)$$ is equal to the density of bare particles. Therefore, the current $$\mathbf j(\mathbf r, t)$$ is equal to the current of the bare particles__. For the fermion system with Hamiltonian, it is easy to show that the expression for the current is 

$$
\mathbf j(\mathbf r ,t )=\sum_\mathbf k \mathbf v_{\mathbf{k}B}^0(\mathbf r, t)=\sum_\mathbf k \mathbf v_\mathbf k^0\delta n_\mathbf k(\mathbf r ,t)
$$

Where $$\mathbf v_\mathbf k^0 =\frac{\hbar \mathbf k}{m}$$ with $$m$$ being the bare mass of particles, and $$\delta_{\mathbf k B}(\mathbf r, t)$$ is the density of bare particles. Thus, we have 

$$
\mathbf v_\mathbf k^0 = \mathbf v_\mathbf k+\sum_{\mathbf k\mathbf k^\prime}f_{\mathbf k\mathbf k^\prime}\mathbf v_{\mathbf k^\prime}.
$$

Note that in this case $$f_{\mathbf k_F\mathbf k_F^\prime}\rightarrow f(\theta)$$, and by symmetry 

$$
\sum_{\mathbf k \mathbf k^\prime}\delta(\xi_{\mathbf k^\prime}^*)f_{\mathbf k^\prime \mathbf k}\mathbf v_{\mathbf k^\prime}=\frac{1}{(2\pi)^3}\int kdk\sin\theta d\theta d\phi\delta(\xi_\mathbf k^*)f(\theta)\frac{\mathbf k_F\cos\theta}{m^*}.
$$

The significant result is often written as a relation between the effective mass $$m^*$$ and the Landau parameter $$F_{1s}$$

$$
\frac{1}{3}F_{1s} =\frac{1}{(2\pi)^3}\int kdk\sin\theta d\theta d\phi\delta(\xi_\mathbf k^*)f(\theta)\mathbf \cos\theta
$$

where 

$$
\frac{1}{m}=\frac{1}{m^*}(1+\frac{F_{1s}}{3})
$$

# Bosonization description of Fermi liquid theory

Landau’s Fermi liquid theory is an effective low-energy theory for fermion systems. It is natural to ask whether the theory can be put into the framework of effective quantum field theory. For example, one may imagine that the wave function of $N$ particle fermion system in Fermi liquid theory is written as 

$$
\Psi(\mathbf r_1,\mathbf r_2,\cdots,\mathbf r_N) = \int D\mathbf x\Phi(\mathbf x_1,\cdots,\mathbf x_M)\Psi_0([\mathbf r]:\mathbf x_1,\cdots,\mathbf x_M)
$$

where $$(\mathbf r_1,\mathbf r_2,\cdots, \mathbf r_N)$$ are the coordinates of the bare fermions and $$(\mathbf x_1,\cdots,\mathbf x_M)$$ are the coordinates of special points in the wave function corresponding to positions of the quasiparticles and there is a one-to-one correspondence between $$(\mathbf x_1,\cdots,\mathbf x_M)$$ and  $$(\mathbf r_1,\mathbf r_2,\cdots, \mathbf r_N)$$ (With $$N=M$$) in Fermi liquid theory. We may imagine that the low-energy properties of the system are characterized by the wave function $$\Phi(\mathbf x_1,\cdots, \mathbf x_M)$$ such that when we apply the principle of least action to the action

$$
S=\int _a^b dt \langle \Psi(t)|[i\hbar \frac{\partial}{\partial t}-H]|\Psi(t)\rangle .
$$

We obtain the Landau transport equation. 

It turns out that the trial wave function approach is not a convenient starting point to understand Fermi liquid theory. __The correct starting point is to realize that the ground state of the system is a filled Fermi sea and low-energy excitations in the system can be viewed as local deformations in the shape of the Fermi surface.__ The shape of the Fermi surface can be labeled by  a wave vector $$\mathbf k(\mathbf x)=(k_F+\delta u(\hat n,\mathbf x))\hat n$$ where  $$\delta u(\hat n ,\mathbf x)$$ labels local small changes in the shape of the Fermi surface in the direction $$\hat n$$. $$\delta u(\hat n, \mathbf x)$$ can be identified with $$\delta n_\mathbf k (\mathbf x)$$ in Fermi liquid theory with $$\mathbf k=k_F\hat n $$. Note that $$\delta u(\hat n, \mathbf x)\hat n $$ is a real number field and a quantum field theory can be constructed by a canonical quantization scheme if the equation of motion for $$\delta u(\hat n, \mathbf x)$$ is known. This is the spirit of bosinzation theory. The Landau energy functional $E[n]$ Represents the energy cost for a small distortion in the shape of Fermi surface in the theory and the Boltzmann equation becomes the quantum equation of motion for the operator $$\delta u(\hat n ,\mathbf x)\hat n $$. The excitations are bosons representing harmonic oscillatory modes of the Fermi surface. The most non-trivial result is perhaps that there is one-to-one mapping between the excitation spectrum obtained in the bosonization theory and the fermionic excitation spectrum. 

# Examples of Applications 

## Thermodynamics and specific heat 

We first have to evaluate the system’s free energy starting from the energy function. 

It is easier to start with the microcanonical ensemble of the system. We consider the system with fixed energy

$$
E= E[n_\mathbf k]\sim E_G +\sum_\mathbf k \xi_\mathbf k^*\delta n_\mathbf k+\frac{1}{2}\sum_{\mathbf k\mathbf k^\prime}f_{\mathbf k\mathbf k^\prime}\delta n_\mathbf k \delta n_{\mathbf k^\prime}
$$

and fixed particle number $N$. The particles are distributed with equal probability to each available state $$\mathbf k$$ provided  that the above constraint is satisfied. To derive the free energy, we first note that for $$N_j$$ particles distributed in $G_j$ states, the total number of possibilities is $$\Gamma_j\frac{G_j!}{N_j!(G_j-N_j)!}$$ and the corresponding entropy is 

$$
\ln G_j \sim G_j \ln G_j - N_j\ln N_j -(G_j-N_j)\ln (G_j-N_j)\\
= -G_j(n_j\ln n_j+(1-n_j)\ln(1-n_j))
$$

Applying this to Fermi liquid theory, we identify $$j$$ as a group of  states with momentum $$p$$ between $$\mathbf k$$ and $$\mathbf k+\Delta \mathbf k$$ with $$\Delta \mathbf k$$ small enough so that $$n_\mathbf p\sim n_\mathbf k $$ and $$G_j\rightarrow \frac{V}{(2\pi)^d} (\Delta k)^d$$. The entropy per unit volume is thus 

$$
S\sim -k \int \frac{d^d k }{(2\pi)^d}(n_\mathbf k \ln n_\mathbf k +(1-n_\mathbf k)\ln (1-n_\mathbf k))
$$

where $$n_\mathbf k$$ can be determined by maximizing the entropy with the energy constraint and $$\sum n_\mathbf k=N$$. The constraints can be handled by introducing Lagrange multipliers $\alpha,\beta$ where we maximize $$S/k-\alpha N -\beta E$$ with respect to $$n_\mathbf k$$. It is easy to obtain 

$$
n_\mathbf k =\frac{1}{1+\exp(\frac{\mathcal E(\mathbf k -\mu)}{kT})}\\
\delta n_\mathbf k = n_\mathbf k-\theta (-\xi_\mathbf k^*)
$$

Where $$ \mathcal E(\mathbf k )=\frac{\delta E[n]}{\delta n_\mathbf k}=\xi_\mathbf k^*+\sum_{\mathbf k^\prime}f_{\mathbf k\mathbf k^\prime}\delta n_{\mathbf k^\prime}$$. In principle, this equation has to be solved self-consistently. At low temperatures, one can perform a Sommerfeld-type expansion of the free energy. To the lowest order in temperature, the specific heat is $$C=\gamma T$$ where 

$$
\gamma =\frac{k_B^2}{3}\frac{m^*k_F}{\hbar^2}=\frac{m^*}{m}{\gamma_0}
$$

where $$\gamma_0T$$ is the corresponding specific heat for the non-interacting Fermi gas. Note that to the lowest order in temperature only effect of interaction on the specific heat is to renormalize the electron mass in Fermi liquid theory. 

## Density-Density response

To determine the density-density response function to an external scalar field, we solve the Boltzmann equation 

$$
\frac{\partial \delta n_\mathbf k(\mathbf k,t)}{\partial t}+\mathbf v_\mathbf k\cdot \nabla _\mathbf r \delta n_\mathbf k(\mathbf r ,t)+\delta(\xi_\mathbf k^*)\sum_{\mathbf k^\prime} f_{\mathbf k\mathbf k^\prime}\mathbf v_{\mathbf k^\prime}\cdot \nabla_\mathbf r\delta n_{\mathbf k^\prime}(\mathbf r,t) + \mathbf F^\mathrm{ext}\cdot \nabla_\mathbf k n_\mathbf k ^\mathrm{(0)}=0
$$

Where we have added an external force term in the equation. For an external scalar potential $$\mathbf F^\mathrm{ext}=e\mathbf E^\mathrm{ext} =-e\nabla\Phi^\mathrm{ext}$$ and $$F^\mathrm{ext}\cdot \nabla_\mathbf k n_\mathbf k ^\mathrm{(0)}\rightarrow e\mathbf v_\mathbf k\cdot \nabla\Phi^\mathrm{ext}\delta(\xi_\mathbf k^*) $$ at $$T\rightarrow 0$$.  

Defining $$\delta n_\mathbf k(\mathbf q,\omega)=\int e^{i(\mathbf q\cdot \mathbf r -\omega t )}\delta n_\mathbf k(\mathbf r, t)d^dr dt$$, we obtain 

$$
(\mathbf q \cdot \mathbf v_\mathbf k-\omega)\delta n_\mathbf k+\mathbf q \cdot \mathbf v_\mathbf k\delta(\xi_\mathbf k^*)\sum_{\mathbf k^\prime}f_{\mathbf k\mathbf k^\prime}\delta n_{\mathbf k^\prime} = -e \mathbf v_\mathbf k \cdot \mathbf q \Phi^\mathrm{ext}\delta(\xi_\mathbf k^*)
$$

For rotationally symmetric systems, we can expand the solutions in terms of spherical harmonics. Here we shall consider a very simple situation $$f_{\mathbf k\mathbf k^\prime}\sim f_0$$ .  In this case, it is easy to see that the solution for $$\delta \rho = \sum_\mathbf k \delta n_\mathbf k$$ is 

$$
\delta\rho(\mathbf q, \omega)=\frac{\chi_{0F}(\mathbf q,\omega)}{1-f_0 \chi_{0F}(\mathbf q,\omega)}e\Phi^\mathrm{ext}(\mathbf q,\omega)
$$

 Where 
 
$$
\chi_{0F} (\mathbf q,\omega) =\sum_\mathbf k \frac{\mathbf v_\mathbf k \cdot \mathbf q}{\omega-\mathbf v_\mathbf k\cdot \mathbf q}\delta(\xi_\mathbf k^*)
$$

Note that this is of the same form as the density-density response function deduced from RPA. More interestingly, it is easy to see that in the small $q$ Limit the Lindblad $$\chi_0(\mathbf q,\omega)$$ has the same  expression as $$\chi_{0F}(\mathbf q ,\omega)$$ except that the bare electron mass $$m$$ is replaced by the effective mass $$m^*$$, indicating that RPA is in fact an example of Fermi liquid theory with un-renormalized mass $$m=m^*$$ and interaction $$f_0=V(q\rightarrow 0)$$.

> It suggests that besides quasi-particle-hole pair excitations, collective excitations can also be produced in Landau’s Fermi liquid theory as in RPA. The limitation of Fermi liquid theory is that it is valid only in the long-wavelength $$\mathbf q\rightarrow 0$$ Limit, where a semi-classical description of the system is valid.




**Ref： Introduction to Classical and quantum field theory by T. K. Ng**
