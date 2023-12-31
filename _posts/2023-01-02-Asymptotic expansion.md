---
layout: post
title: "Asymptotic expansion"
date: 2023-1-2
excerpt: "To get short-range or long-range behaviors of integral"
tags: [Math]
comments: true
---

* toc
{:toc}


The solution of a large class of physically important problems can be represented in terms of definite integrals and further can be expressed in terms of special functions. However, exact solutions fail to tell the true content. In order to decipher the main mathematical and physical features of these solutions, it is useful to study their behavior for large $$x$$ and $$t$$. Frequently, one particular class of the integral has a form as 

$$
I(k)= \int_a^b f(t) \exp(t\phi(k)) dt \quad \mbox{with}\quad k \rightarrow \infty.
$$

In this note, we introduce appropriate mathematical techniques for evaluating the behavior of certain integrals containing a large parameter. Historically speaking, the development of these techniques was motivated by concrete physical problems. The main attention is paid to three methods: __Laplace’s method, the method of stationary phase, and the steepest descent method__.

# Fundamental concept

The first step is to make a definition of asymptotic expansion under the condition that the parameter $$\epsilon$$ is real and small.

## Something basic

> ==Def== 
>
> a) The notation
> 
> $$
> f(k)=O(g(k)),\quad k\rightarrow k_0
> $$
> 
> Means that there is a finite constant $$M$$ and a neighborhood of $$k_0$$ where $$|f|\leq M|g|$$.
>        b) THe notation
> 
> $$
> f(k)\leq g(k),\quad k\rightarrow k_0
> $$
> 
> or  $$f(k)=o(g(k)),\quad k\rightarrow k_0$$ means
> 
> $$
> \lim_{k\rightarrow k_0} |\frac{f(k)}{g(k)}|=0
> $$
> 
> c) We shall say that $$f(k)$$ is an approximation to $$I(k)$$ valid to order $$\delta(k)$$ as $$k\rightarrow k_0$$ if
> 
> $$
> \lim_{k\rightarrow k_0}\frac{I(k)-f(k)}{\delta(k)}=0
> $$

A typical purpose is to find a sequence of functions $$\{\delta_j(k)\}$$ such that 

$$
\delta_{j+1}(k)\ll \delta_j(k),\quad k\rightarrow k_0
$$

In the sense of a notation, we claim the following two statements are equivalent.

$$
I(k) \sum_{j=1}^m a_j\delta_j(k)+O(\delta_{m+1}(k)),\quad k\rightarrow k_0, m=1,2,\cdots N
$$

and 

$$
I(k) \sim \sum_{j=1}^N a_j\delta_j(k),\quad k\rightarrow k_0
$$

with $$\sim $$ meaning 

$$
\lim_ {k\rightarrow k_0}\left|\frac{I(k)}{\sum_{j=1}^Na_j\delta_j(k)} \right |=1
$$

## Examples 

The first example given here is to find the value of the integral 

$$
I(\epsilon) =\int_0^\infty \frac{e^{-t}}{1+\epsilon t}d t,\quad \epsilon >0
$$

For a sufficiently small real positive value of $$  \epsilon  $$. Since the value at the boundary is the largest, we can successively apply the partial integral. One integration by parts yields, 

$$
I(\epsilon)= 1- \epsilon\int_0^\infty\frac{e^{-t}}{(1+\epsilon t)^2} 
$$

Repeating this process $$N$$ more times yields,

$$
I(\epsilon) = 1-\epsilon +2!\epsilon^2+\cdots +(-1)^N!\epsilon^N+(-1)^{N+1}(N+1)!\epsilon^{N+1}\int_0^\infty\frac{e^{-t}}{(1+\epsilon t)^{N+2}}dt
$$

Therefore, the aymptotic series are $$\{\epsilon^i,i=1,\cdots N\}$$, which coincides with the Tayler expansion. The validatity of the expansion requires the error $$R_{N+1}$$ term vanishes as $$o(\epsilon^N)$$ as $$\epsilon\rightarrow 0$$,

$$
|R_{N+1}| \leq  (N+1)! \epsilon ^{N+1}\int_0^\infty e^{-t}dt =(N+1)!\epsilon^{N+1}
$$

As a matter of fact, $$R_{N+1}$$ diverges with a fixed $$\epsilon$$ when $$N$$ goes to $$\infty$$. As a consequence, __we cannot take too many terms in the series. In principle, one can find the ‘optimal’ value of $$N$$ for fixed $$\epsilon$$ for which the remainder is smallest__. 

There are cases where no sophisticated asymptotic methods are needed. The first class involves the evaluation of the integral

$$
\int_a^b f(k,t)dt \quad f(k,t)\sim f_0(t), k\rightarrow k_0.
$$

The second class is 

$$
\int_k ^b f(t)dt ,\quad k\rightarrow \infty.
$$

To determine the leading behavior of integrals of the first class, we use the following fact. __Assume that $$ f(k,t) \sim f_0(t) $$ as $$ k\rightarrow k_0 $$ uniformly for $$ t $$ in $$ [a,b] $$, 
and that $$ \int_a^b f_0(t)dt $$ is finite and nonzero__. The limit as $$ k\rightarrow k_0$$ and the integral can be  interchanged, hence 

$$
\int_a^b f(k,t)dt\sim \int_a^b f_0(t)dt,\quad k\rightarrow k_0
$$

One example follows as 

$$
I(k)=\int_0^1 \frac{\sin kt }{t}dt\sim \int_0^1(k-\frac{t^2k^3}{3!}\cdots)=k-\frac{k^3}{3\cdot 3!}.
$$


The second class can be exemplified as with $$k\rightarrow 0$$

$$
I(k)=\int_k^\infty e^{-t^2}dt = \int_0^\infty e^{-t^2}dt-\int_0^k e^{-t^2}dt
$$

The second term can be asymptotically expanded. 

A much nontrivial example is 

$$
E_1(k)=\int_k^\infty \frac{e^{-t}}{t}dt, \quad k\rightarrow 0^+~.
$$

But now the integrand has a logarithmic singularity at $$t=0$$. If we subtract $$\frac{1}{t(t+1)}$$, the difficulty is avoided,

$$
\begin{align}
E_1(k)&=  \int_k^\infty \frac{dt}{t(t+1)}+\int_0^\infty(e^{-t}-\frac{1}{t+1})\frac{dt}{t}-\int_0^k (e^{-k}-\frac{1}{t+1})\frac{dt}{t} \notag \\
 &= -\gamma -log k +k -\frac{k^2}{4}+\cdots
 \end{align}
$$

# Laplace Type Integrals

A Laplace Type Integral is to study the asymptotic behavior as $$k\rightarrow +\infty$$ of the form

$$
I(k)=\int_a^b f(t) e^{-k\phi(t)}dt
$$

A  special case is a Laplace transform, which is why integrals are referred to as Laplace-type integrals. 

## Integration by parts

Suppose that $$\phi(t)$$ is monotonic in $$[a,b]$$, then one needs to analyze the behavior of the integral near the boundaries. __Because integration by parts is based on such an analysis, we expect that it is a useful technique for studying Laplace type integral when $$\phi(t)$$ is monotonic__.

We can look at the first example 

$$
\begin{align}
I(k) & = \int_0^\infty \frac{e^{-kt}}{(1+t^2)^2}dt,\quad k\rightarrow+\infty \notag \\
& = \frac{(1+t^2)^{-2}e^{-kt}}{-k}|_0^\infty +\frac{1}{k}\int_0^\infty (-4t)(1+t^2)^{-3}e^{-kt}dt \notag \\ 
& = \frac{1}{k}+O(\frac{1}{k^3})
\end{align}
$$

The rigorous justification of the integration by parts, in general, follows from the following lemma

> ==Lemma==
>
> Consider the integral
> 
> $$
> I(k)=\int_a ^b f(t)e^{-kt}dt
> $$
> 
> Where the interval $$ [a,b] $$ is a finite segment of the real axis. Let $$ f(m)(t) $$ Denote the $$m$$th derivative of $$f(t)$$. Suppose that $$f(t)$$ has $$N+1$$ Continuous derivatives while $$f^{(N+2)}(t)$$ is piecewise continuous on $$ a\leq t\leq b $$. Then
>  
> $$
> I(k)\sim \sum_{n=0}^N \frac{e^{-ka}}{k^{n+1}} f^{(n)},k\rightarrow +\infty
> $$
>  

The proof is straightforward. 

## Watson’s Lemma

If $$f(t)$$ is not sufficiently smooth at $$t=a$$, then the integration by parts approach for the asymptotic evaluation may not work. Instead, one may resort to Watson’s lemma.

> ==Waston’s Lemma==
>
> Consider the integral
> 
> $$
> I(k)=\int_0^b f(t)e^{-kt}dt, \quad b>0
> $$
> 
> Suppose that $$f(t)$$ is integrable in $$ (0,b) $$ and that it has the asymptotic series expansion
> 
> $$
> f(t)\sim t^\alpha \sum_{n=0}^\infty a_n t^{\beta n},\quad t\rightarrow 0^+,\alpha>-1,\beta>0.
> $$
> 
> Then
> 
> $$
> I(k)\sim \sum_{n=0}^\infty a_n\frac{\Gamma(\alpha+\beta n+1)}{k^{\alpha+\beta n+1}},\quad k\rightarrow \infty
> $$
> 
> __Proof__ We break the integral in two parts, $$ I_1(k) $$ and $$ I_2(k) $$,
> 
> $$
> I_1(k) = \int_0^R f(t)e^{-kt }dt ,\quad I_2(k) = \int_R^b f(t)e^{-kt }dt
> $$
> 
> and $$ R<b $$ is a positive constant.
> The integral is exponentially small as $$ k\rightarrow \infty $$.
> For finite $$ b$$, because $$ f(t) $$ is bounded for $$ t>0 $$,
> there exists a positive constant $$ A $$, such that
>  $$ |f|\leq A $$ for $$ t\geq R $$. Thus,
> 
> $$
> |I_2(k)|\leq A\int_R^b e^{-kt}dt = \frac{A}{k}(e^{-kR}-e^{-kr})~.
> $$
> 
> Thus $$ I_2(k)=O(\frac{e^{-kR}}{k}) $$. Due to the series,
> we have
> 
> $$
> I_1(k)=\int_0^R [\sum_{n=0}^R a_nt^{\alpha+\beta n}+ O(t^{\alpha +\beta (N+1)}) ]e^{-kt}dt,\quad k\rightarrow \infty~.
> $$
> 
> However,
> 
> $$
> \begin{align}
> \int_0^R t^{\alpha+\beta n}e^{-kt }dt & = \int_0^\infty t^{\alpha+\beta n}e^{-kt}dt -\int_R^\infty t^{\alpha+\beta n}e^{-kt}dt \notag \\
> &=\frac{\Gamma(\alpha+\beta n +1)}{k^{\alpha+\beta n +1}} +O(\frac{e^{-k R}}{k})
> \end{align}
> $$
> 

## Example 

The example we present here is 

$$
I(k) = \int_0^5 \frac{e^{-kt}}{\sqrt{t^2+2t}}dt,\quad k\rightarrow \infty
$$

A singularity exists at $$t=0$$, which forbids the partial integral method. Intuitively, the singularity at $$t=0$$ makes the dominant contribution. Thus it would be desirable to expand $$(t^2+2t)^{-1/2}$$ in the neighborhood of the origin. We separate the integral into two parts,

$$
I(k) =I_1(k) +I_2(k)= (\int_0^R  +\int_R^5 )\frac{e^{-kt}}{\sqrt{t^2+2t}}dt
$$

where $$R$$ is sufficiently small but finite to allow expansion of $$\sqrt{t^2+2t}$$ around $$t=0$$, 

$$
(2t+t^2)^{-1/2}\sim (2t)^{-1/2}-\frac{(2t)^{1/2}}{8}
$$

we find

$$
I(k) \sim \int _0^R e^{-kt}(2t)^{-1/2}dt -\frac{1}{8}\int_0^R e^{-kt}(2t)^{1/2}dt
$$

We intuitively relax the integrating region by replacing $$R$$ with $$\infty$$ with an exponentially small error,

$$
I(k) \sim \frac{\Gamma(1/2)}{(2k)^{1/2}}-\frac{\Gamma(3/2)}{2(2k)^{3/2}}.
$$

The error can be estimated 
$$
R_e= \int_R^\infty e^{-kt}t ^\alpha dt = \frac{e^{-kR} R^\alpha}{-k} + \int ^\infty_R\frac{\alpha e^{-kt}t^{\alpha-1}}{-k}dt = O(\frac{e^{-kR}}{k}).
$$


# Laplace’s method

The above discussion is focused on the case with $$\phi(t)$$ being monotonic in $$[a,b]$$. Suppose, the local minimum occurs at an interior point $$c$$ $$a<c<b$$, and $$\phi^\prime(c)=0,\phi^{\prime\prime}(c)>0$$. Further, we assume that $$\phi^\prime (t)\neq 0$$ in $$[a,b]$$ except at $$t=c$$ and $$f,\phi$$  are sufficiently smooth which will be explained below. 

> ==Laplace’s Method==
>
> Consider the integral
> 
> $$
> I(k) = \int _a^b f(t)e^{-k \phi(t)}dt,\quad k\rightarrow +\infty
> $$
> 
> and assume that $$\phi^\prime(c)=0$$, $$\phi^{\prime\prime}(c)>0$$ for some point $$c$$ in the interval $$[a,b]$$ except at $$t=c$$, $$\phi\in C^4[a,b]$$ and $$f\in C^2[a,b]$$. Then if $$c$$ is an interior point, we have the leading term as
> 
> $$
> I(k)\sim e^{-k\phi(c)}f(c)\sqrt{\frac{2\pi}{k\phi^{\prime\prime}(c)}},\quad k\rightarrow \infty
> $$

