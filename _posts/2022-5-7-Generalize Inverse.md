---
layout: post
title: "Generalized Inverse"
date: 2022-05-07
excerpt: "Generalized inverse, or Moore-Penrose inverse"
tags: [Math]
comments: true
---

* toc
{:toc}

## Generalized Inverse

In practice, I come across a problem with taking a derivative of an eigenvector. Mathematically,  with  a matrix $$H(\alpha)$$ and its eigenvector $$\mathbf v(\alpha)$$, 

$$
H(\alpha )\mathbf v(\alpha )=E(\alpha)\mathbf v(\alpha),
\label{eigeneq} 
$$

a question comes how to calculate the derivative $$\partial_\alpha\mathbf v(\alpha )$$ efficiently. One naive method is to find $$v(\alpha+\delta \alpha )$$, such that $$\partial_\alpha \mathbf v(\alpha)=[\mathbf v(\alpha+\delta\alpha)-\mathbf v(\alpha)]/\delta\alpha$$ is obtained directly by the definition. Such a scheme generates errors and we have to determine which eigenvector is targeted for 
$$H(\alpha+\delta\alpha)$$. When the $$H(\alpha)$$ depends on plenty of parameters $$\alpha_1,\alpha_2,\cdots$$, much effort is needed. 
As a matter of fact, we can reach our purpose by means of __generalized inverse__. We set out to take a derivative on both sides of Eq.~$$(\ref{eigeneq})$$

$$
\partial_\alpha H(\alpha)\mathbf v(\alpha)+H(\alpha)\partial_\alpha\mathbf v(\alpha)=\partial_\alpha E(\alpha)\mathbf v(\alpha)+E(\alpha) \partial_\alpha\mathbf v(\alpha),
$$

or equivalently,

$$
[E(\alpha)-H(\alpha)]\partial_\alpha\mathbf v(\alpha) = [\partial_\alpha H(\alpha)-\partial_\alpha E(\alpha)] \mathbf v(\alpha).
$$

The matrix $$E(\alpha)-H(\alpha)$$ is singular for  $$E(\alpha)$$ is just the eigenvalue, such that we fail to obtain $$\partial_\alpha\mathbf v(\alpha)$$ by taking an inverse. 
In the sense of numerics, both $$\partial_\alpha H(\alpha)$$ and $$\partial_\alpha E(\alpha)$$ are more friendly to calculate. 

Further, by observing 

$$
\partial_\alpha E(\alpha) = \mathbf v^\dagger (\alpha )\partial_\alpha H(\alpha)\mathbf v(\alpha).
$$

The remained thing is to ‘Take inverse’ $$[E(\alpha)-H(\alpha)]^-$$.

$$
\partial_\alpha \mathbf v(\alpha) = [E(\alpha)-H(\alpha)]^-[\partial_\alpha H(\alpha)-\mathbf v^\dagger (\alpha )\partial_\alpha H(\alpha)\mathbf v(\alpha)]\mathbf v(\alpha).
$$

A way out is to the [concept](https://en.wikipedia.org/wiki/Generalized_inverse) __generalized inverse__(g-inverse, pseudoinverse) or __Moore-Penrose inverse__.

### Definition

>  **Definition** 
>
>  A matrix $$A^g\in \mathbb R ^{n\times m }$$ is a generalized inverse of a matrix $$A\in \mathbb R^{m\times n }$$ if $$A A^gA=A$$. 

The purpose of constructing a generalized inverse of a matrix is to obtain a matrix that can serve as an inverse in some sense of a wider class of matrices than invertible matrices. A generalized inverse exists for an arbitrary matrix, and when a matrix has a regular inverse, this inverse is its unique generalized inverse. 

With the generalized inverse, we can find a solution to a linear system $$Ax=y$$. Take $$G$$ as a generalized inverse of $$A$$. Then 

$$
AGy=AGAx=Ax=y,
$$

which yields $$x=Gy$$ as a solution. 

### Construction

Given a matrix $$A\in \mathbf R^{m\times n }$$, we can singular-value decompose it as 

$$
A= U \begin{pmatrix}
\Sigma_1  & 0 \\ 0& 0
\end{pmatrix} V
$$

then there exist matrices $$X, Y,Z$$ such that 

$$
A^g = V \begin{pmatrix} \Sigma_1^{-1}  & X \\ Y & Z \end{pmatrix} U^T
$$

Conversely, any choice of $$X,Y$$, and $$Z$$ for the matrix of this form is a generalized inverse of $$A$$. In particular, the __pseudoinverse__ is given by $$X=Y=Z=0$$

$$
A^+ = V \begin{pmatrix} \Sigma_1^{-1}  & 0 \\ 0 & 0- \end{pmatrix} U^T
$$


> One can obtain pseudoinverse by a command [__PseudoInverse__](https://reference.wolfram.com/language/ref/PseudoInverse.html) in Mathematica software. 

