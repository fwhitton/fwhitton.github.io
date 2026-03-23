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
But if $\rho$ is a rotation anti-clockwise by $45^\circ$ then 
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
\rho
\begin{pmatrix}
1/\sqrt{2}\\
1/\sqrt{2}
\end{pmatrix}
$$
