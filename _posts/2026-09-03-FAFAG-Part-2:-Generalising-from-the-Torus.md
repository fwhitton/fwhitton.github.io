---
Title: FAFAG Part 2 Generalising from the torus
Date: 2026-09-03
---
Mathematically, what were we doing in the last post when we identified the opposite edges of a square to form a torus? We were really saying that two points in space are considered to be the same if they differ by $1$ horizontally or vertically. This defines an equivalence relation on the whole plane:

$$
(x,y) \sim (x+m,y+n)
$$

for any $m,n\in\mathbb{Z}$. Every point in space can be identified with a point in the unit square. We've identified points which differ by an element of the lattice $\mathbb{Z}^2$. In terms of groups, a lattice is an abelian (hence normal) subgroup and so we can take the quotient group $\mathbb{R}^2/\mathbb{Z}^2$. In fact, we can extend this to any number of dimensions and any (full rank) lattice $\Lambda$ to define the torus $\mathbb{T} = \mathbb{R}^n/\Lambda$.

A lattice is a generalisation of $\mathbb{Z}^n$ and any lattice can be written $\Lambda = A \mathbb{Z}^n$ for some (non-degenerate) matrix $A$. We call a function on $\mathbb{R}^n$ "$\Lambda$-periodic if $f(x+\lambda) = f(x)$ for any point $x\in\mathbb{R}^n$ and any lattice point $\lambda\in\Lambda$. We naturally identify $\Lambda$-periodic functions on $\mathbb{R}^n$ with functions on the torus.

Once again we seek Laplacian eigenfunctions on the torus. They take the form

$$
u_\xi(x) = \exp(2\pi i \langle \xi, x\rangle)
$$

and our job is to find $\xi\in\mathbb{R}^n$ that makes this $\Lambda$-periodic.
