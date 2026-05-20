---
title: "Derivatives and linearity"
date: 2026-05-20
---
# Differentiation as a matrix
One of the first things we learn about differentiation is that it is *linear*, which is something we end up using reflexively. If I ask you to differentiate $ex^2 + \pi x + \gamma$ then it doesn't matter that this is a quadratic I'm sure you've never seen before: it's a linear combination of functions you *do* know how to differentiate and so it poses no problem to you. More formally, differention is a linear map from functions with one continuous derivative to continuous functions, i.e. $D:C^1(\mathbb{R})\rightarrow C(\mathbb{R})$. And we know that, after we've picked a basis, linear maps on vector spaces can be represented by matrices. Unfortunately $C^1(\mathbb{R})$ doesn't have a nice basis for me to work with so I'm going to restrict my attention to a finite dimensional vector spaces, specifically polynomials. There is a very natural basis for the polynomials, namely the monomials (shouldn't it be mononomial?) and we know that the columns of a matrix are just the images of the basis elements under the map. Because $D:1\mapsto 0$, $D:x\mapsto 1$, $D:x^2\mapsto 2x$ namely derivatives reduce the order of a monomial by one we see that the matrix has non-zero entries only on the superdiagonal:

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
I am not just saying that *differentiation* is a linear map: I am also saying the output, a derivative, is itself a linear map. For functions of one variable this is subtle. The derivative evaluated at a point gives the 'slope' of the curve at that point which is just a number. Of course in one dimension a linear map is specified by a single number so at this resolution we cannot distinguish. However when we move up to functions of more variables the derivative is the gradient $\nabla f = (\partial_1 f, \partial_2 f,\cdots,\partial_n f)$. If I evaluate this at point $\mathbf{x_0}$ then $\nabla f(\mathbf{x_0})$ is a fixed vector and defines a linear map by acting on a unit vector $\mathbf{n}$ via $\nabla f(\mathbf{x_0}) \cdot \mathbf{n}$ to tell us the rate of change of the function $f$ in the direction $\mathbf{n}$ at the point $\mathbf{x_0}$. Thus when evaluated at the point $\mathbf{x_0}$, $\nabla f(\mathbf{x_0})$ belongs to the dual space of $\mathbb{R}^n$. Differential geometry generalises the hell out of this but we'll only give the definition that a $1$-form is a smooth map from an open set in a vector space (like the domain of our function $f$) to the dual space of that vector space. Given a basis of $\mathbb{R}^n$ like $e_1,e_2,\cdots,e_n$ there is a dual basis $e_1^*,\cdots,e_n^*$ such that $e_i^* (e_j) = \delta_{ij}$ and we can write the derivative in this basis as 

$$\nabla f = \sum_i \frac{\partial f}{\partial x_i} e_i^*$$
