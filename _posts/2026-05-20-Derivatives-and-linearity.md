---
title: "Derivatives and linearity"
date: 2026-05-20
---
# Differentiation as a matrix
One of the first things we learn about derivatives is that they are *linear*, which is something we end up using reflexively. If I ask you to differentiate $ex^2 + \pi x + \gamma$ then it doesn't matter that this is a quadratic I'm sure you've never seen before: it's a linear combination of functions you *do* know how to differentiate and so it poses no problem to you. More formally, differention is a linear map from functions with one continuous derivative to continuous functions, i.e. $D:C^1(\mathbb{R})\rightarrow C(\mathbb{R})$. And we know that, after we've picked a basis, linear maps on vector spaces can be represented by matrices. Unfortunately $C^1(\mathbb{R})$ doesn't have a nice basis for me to work with so I'm going to restrict my attention to a finite dimensional vector spaces, specifically polynomials. There is a very natural basis for the polynomials, namely the monomials (shouldn't it be mononomial?) and we know that the columns of a matrix are just the images of the basis elements under the map. Because $D:1\mapsto 0$, $D:x\mapsto 1$, $D:x^2\mapsto 2x$ namely derivatives reduce the order of a monomial by one we see that the matrix has non-zero entries only on the superdiagonal:

$$
D=
\begin{pmatrix}
0 & 1 & 0 & \cdots\\
0 & 0 & 2 & \cdots\\
0 & 0 & 3 & \cdots \\
\vdots & \vdots & \vdots & \ddots
\end{pmatrix}
$$

When I first saw this in my first term of undergrad it blew my mind: calculus is curvy and linear algebra is straight and never the twain shall meet. But little did I know this was the beginning of a very happy marriage with a healthy baby called function spaces.

# PDEs as bilinear forms

Fast-forward 3 years I've studied a bit of PDEs and some Hilbert spaces. Consider the Laplacian eigenvalue equation on a domain $\Omega$ with $u=0$ on $\partial\Omega$

$$
-\nabla^2 u = \lambda u
$$

If we multiply by any function $\phi$ and integrate over $\Omega$ we can use integration by parts to move a derivative from $u$ to $\phi$ and the boundary condition to find

$$
\int_\Omega \nabla \phi \cdot \nabla u dx = \lambda \int_\Omega \phi u dx
$$

Any eigenfunction satisfies this equation but we've now formulated it in a way that only asks $u$ to have one derivative. Thus we can loosen the sense in which we ask a function to be an eigenfunction: a *weak solution* of the eigenvalue equation is one that satisfies the above equation for all $\phi\in C^1(\Omega)$.

# Derivatives are linear maps
