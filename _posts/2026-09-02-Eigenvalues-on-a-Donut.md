---
Title: Eigenvalues on a Donut
Date: 2026-09-02
image: /assets/images/notsimplyconnected.png
---

This is the first in a (hopefully) three part series, building up to the Fourier Transform on a (locally compact) abelian group. This first post is purely a motivating example with few technicalities; in later posts we will proceed as per the mathematician's directive: 

>"Go forth and generalise."

<a href="https://fwhitton.github.io/2025/03/21/Topology-I-Snake-on-a-Donut.html">This post</a> contains more information abouts donuts (*tori* herein), but to recap we build one by gluing together the opposite edges of a square:

<img src="/assets/images/torus.gif" alt="torus" width = 200>

Functions on the torus naturally arise as functions of two real variables which are periodic in both arguments. The specific functions on the torus that we're interested in are the solutions to my favourite PDE:

$$
-(\partial_x^2 + \partial_y^2) u = \lambda u.
$$

Rather than working on the torus, denoted $\mathbb{T}$, it is easier to solve this equation on the square and then ask that the solution is periodic in both $x$ and $y$ with period $1$. Trusty separation of variables yields

$$
u_k(x,y) = \exp(2\pi i (k_x x + k_y y))
$$

which is an eigenfunction with eigenvalue

$$
\lambda = 4\pi^2(k_x^2 + k_y^2).
$$

For $u_k(x,y)$ to be periodic we need

$$
u_k(x,y) = u_k(x+1,y) = u_k(x,y+1),
$$

and by the definition of $u_k$, this means that

$$
\exp(2\pi i k_x) = \exp(2\pi i k_y) = 1 \implies k_x,k_y \in \mathbb{Z}.
$$

Renaming $k_x = m$ and $k_y = n$, we find that

$$
-\Delta u_{m,n} = 4\pi^2 (m^2 + n^2) u_{m,n}.
$$

The points $(m,n)\in\mathbb{Z}^2$ form a *lattice*. Is it a coincidence that the unit square we started out with tiles this lattice? More on that later...

Now we have the eigenfunctions of the Laplacian, the spectral theorem tells us that these form a basis for a friendly bunch of functions on the torus:

$$
L^2(\mathbb{T}) = \left\{f:\mathbb{T} \to \mathbb{C} : \int_{\mathbb{T}} |f(x)|^2 \, dx < \infty \right\}.
$$

That is, every $f\in L^2(\mathbb{T})$ can be decomposed as

$$
f(x) = \sum_{m,n\in\mathbb{Z}} \hat{f}(m,n) u_{m,n}(x,y),
$$

where

$$
\hat{f}(m,n) = \int_{\mathbb{T}} f(x,y) \exp(2\pi i (mx+ny))\,dxdy.
$$

The advantage of the notation $\hat{f}$ over the usual $a_n$ or $c_n$ for a coefficient is to remind us that the coefficient depends directly on the function $f$. While $f$ is a function on $\mathbb{T}$, we'll see later that $\hat{f}$ is a function on $\hat{\mathbb{T}}$.

Philosophically, the spectral theorem says that the Laplacian on a torus is diagonalisable, in the sense that

$$
-\Delta f = 4\pi^2 \sum_{m,n\in\mathbb{Z}} (m^2 + n^2) \hat{f}(m,n) u_{m,n}(x).
$$

That's the end of the example. I hope it's clear that there is fecund ground for abstraction.

