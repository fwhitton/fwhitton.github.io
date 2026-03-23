---
Title: "Imaginary numbers aren't imaginary"
Date: 2025-01-26
---

Please enjoy an alternative motivation of the extension from the real numbers to the complex numbers.

To begin with, I'm going to assume we're all happy with the existence and properties of real numbers $\mathbb{R}$: the number line along with its usual operations, distances and ordering. And if we're happy with $\mathbb{R}$ then hopefully we're also happy with the Euclidean plane, $\mathbb{R}^2 := \mathbb{R} \times \mathbb{R}$ and the addition we do with vectors in $\mathbb{R}^2$:

$$
\begin{pmatrix}
a\\
b
\end{pmatrix}
+
\begin{pmatrix}
c\\
d
\end{pmatrix}
:=
\begin{pmatrix}
a + c\\
b + d
\end{pmatrix}
$$

And this obeys all the things we like about addition of real numbers, namely the order of addition doesn’t matter, adding zero changes nothing and adding something to its negative gives us zero. The natural next question is how can we define multiplication for vectors in $\mathbb{R}^2$? The naïve approach would be to define an operation $\star$ such that

$$
\begin{pmatrix}
a\\
b
\end{pmatrix}
\star
\begin{pmatrix}
c\\
d
\end{pmatrix}
:=
\begin{pmatrix}
ac\\
bd
\end{pmatrix}
$$

Here I’ve used the star so I can reserve the multiplication symbol for later. Again, this does some the nice things we like about multiplication of real numbers but there’s a subtle problem: this is not coordinate independent. When we multiply vectors in $\mathbb{R}^2$ the result shouldn’t depend on how we orient the coordinate axes. More generally, the relationship between vectors should be *basis independent*. It shouldn't matter if we rotate our vectors and then multiply or if we multiply and then rotate the result. If $\rho$ is a rotation then

$$
\rho
\left(
\begin{pmatrix}
a\\
b
\end{pmatrix}
\star
\begin{pmatrix}
c\\
d
\end{pmatrix}
\right)
:=
\rho
\begin{pmatrix}
a\\
b
\end{pmatrix}
\star
\rho
\begin{pmatrix}
c\\
d
\end{pmatrix}
$$

But if $\rho$ is a rotation anti-clockwise by $45^\circ$ then for example

$$
\rho
\left(
\begin{pmatrix}
0\\
1
\end{pmatrix}
\star
\begin{pmatrix}
1\\
0
\end{pmatrix}
\right)
\neq
\begin{pmatrix}
-1/\sqrt{2}\\
1/\sqrt{2}
\end{pmatrix}
\star
\begin{pmatrix}
1/\sqrt{2}\\
1/\sqrt{2}
\end{pmatrix}
$$

as the left-hand side is equal to $0$. However rotation of the vectors "respects" the addition between them. Can we cook up a different definition of multiplication of vectors such that rotations "respect multiplication"?  Unfortunately I have no sort of nice way to motivate the following definition but I hope you can tolerate having it be handed down on high and seeing that it in fact does what we want:

$$
\begin{pmatrix}
a\\
b
\end{pmatrix}
\times
\begin{pmatrix}
c\\
d
\end{pmatrix}
:=
\begin{pmatrix}
ac-bd\\
ad + bc
\end{pmatrix}
$$

For this to be any kind of recognisable definition we want it to obey all the familiar nice properties of multiplication. If $z$ and $w$ are vectors in $\mathbb{R}^2$ then we multiplication between them to be *commutative*:

$$ z\times w = w \times z,$$

*distributive*:

$$z \times (w_1  + w_2) = z \times w_1 + z \times w_2,$$

and *associatative*:

$$z_1 \times (z_2 \times z_3) = (z_1 \times z_2) \times z_3.$$

You're welcome to go home and check that the definition for multiplication I've given obeys these properties or you can trust me (I've worked through associativity myself and it's a mess). One feature of our multiplication is that we have a 'copy’ of $\mathbb{R}$ just by taking $b$ and $d$ to be zero:

$$
\begin{pmatrix}
a\\
0
\end{pmatrix}
\times
\begin{pmatrix}
c\\
0
\end{pmatrix}
:=
\begin{pmatrix}
ac\\
0
\end{pmatrix}
$$

So we know the first entry can just be viewed as a familiar real number. But this second entry clearly isn’t totally independent, like in our first attempt. It gets mixed up with the first entry, for example:

$$
\begin{pmatrix}
0\\
1
\end{pmatrix}
\times
\begin{pmatrix}
0\\
1
\end{pmatrix}
:=
\begin{pmatrix}
-1\\
0
\end{pmatrix}
$$

Which looks harmless at first glance. But if $z = (0, 1)$ then $z^2 = (−1, 0)$ and $(−1, 0)$ added and multiplied just like $-1 \in\mathbb{R}$. So we've found some sort of vector square root of $-1$? It feels wrong to simply call this the beginning of a new branch of mathematics: that doesn’t do justice to how important this is. $2$-dimensional vectors are interesting in their own right but the richness that comes from imbuing $\mathbb{R}^2$ with this multiplication is phenomenal. In reality, you'll never see the vectors as I've written them. Instead we adopt a convention

$$
\begin{pmatrix}
a\\
b
\end{pmatrix}
=:a + bi
$$

and $1i$ is just written as $i$ meaning our previous statement can be written succinctly as

$$i^2 = -1.$$

This is usually the first definition in a complex numbers course but I hope this route of motivation has been insightful or at the least refreshing. This may feel artificial but the important fact is that this is the only commutative, associative, distributive multiplication on $\mathbb{R}^2$ which indicates that maybe we discovered this operation and the necessity of defining $i$ dropped out organically rather than making a u-turn and saying that $-1$ now has a defined square root and seeing what follows.



