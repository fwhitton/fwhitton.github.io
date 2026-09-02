---
Title: Fourier Analysis for abelian Groups Part 1 Motivating Example
Date: 2026-09-02
---

This is the first in a (hopefully) three part series, building up to the Fourier Transform on a (locally compact) abelian group. This first post is purely a motivating example with few technicalities and in later posts we will proceed as per the mathematician's directive: 

>"Go forth and generalise."

There are more details on the torus in <a href="https://fwhitton.github.io/2025/03/21/Topology-I-Snake-on-a-Donut.html">this post</a>, but to recap we build one by gluing together the opposite edges of a square:

<img src="/assets/images/torus.gif" alt="torus" width = 200>

Functions on the torus naturally arise as functions which are periodic in both arguments. We seek solutions to my favourite PDE on the torus:

$$
-(\partial_x^2 + \partial_y^2) u = \lambda u.
$$

Rather than working on the torus, it is easier to solve this equation on the square and then ask that the solution is periodic in both $x$ and $y$ with period $1$. Trusty separation of variables yields

$$
u_k(x,y) = \exp(2\pi i (k_x x + k_y y))
$$

which is an eigenfunction with eigenvalue

$$
-\Delta u_k(x,y) = 4\pi^2(k_x^2 + k_y^2)u_k(x,y).
$$

If we want this to be periodic then we need

$$
u(x,y) = u(x+1,y) = u(x,y+1)
$$

and by the definition of $u$, this means that

$$
\exp(2\pi i k_x) = \exp(2\pi i k_y) = 1 \implies k_x,k_y \in \mathbb{Z}.
$$

Renaming $k_x = m$ and $k_y = n$, we find that

$$
-\Delta u_{m,n} = 4\pi^2 (m^2 + n^2) u_{m,n}.
$$

The points $(m,n)\in\mathbb{Z}^2$ naturally form a lattice. In fact, the isomorphic set of points $\{a+bi:a,b\in\mathbb{Z}\}$ are called the Gaussian integers and the eigenvalues are the modulus of the lattice point $a+bi$.

The spectral theorem tells us that the Laplacian eigenfunctions form a basis for functions on the Torus which are square-integrable:

$$
L^2(\mathbb{T}) = \{f:\mathbb{T} \to \mathbb{C} : \int_{\mathbb{T}} |f|^2 \, dx < \infty \}.
$$

That is, every $f\in L^2(\mathbb{T})$ can be decomposed as

$$
f(x) = \sum_{m,n\in\mathbb{Z}} \hat{f}(m,n) u_{m,n}(x,y),
$$

where

$$
\hat{f}(m,n) = \int_{\mathbb{T}} f(x,y) \exp(2\pi i (mx+ny))\,dxdy.
$$

Philosophically, the spectral theorem says that the Laplacian on a torus is diagonalisable in the sense that

$$
-\Delta f = 4\pi^2 \sum_{m,n\in\mathbb{Z}} (m^2 + n^2) \hat{f}(m,n) u_{m,n}(x).
$$

That's the end of the example. I hope you see that there is fecund ground for abstraction.

