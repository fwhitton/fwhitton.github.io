---
title: "Topology I: Snake on a Donut"
date: 2025-03-21
---

I'm of the age where my first phone housed only one game, snake. Snake is played in a rectangular world: if you try to escape out of one edge you are teleported to the opposite edge. It seems that modern iterations of the game have hardened the boundaries of the square, subverting my entire post but cast your mind back to when snake looked like this:

<img src="/assets/images/phone.jpg" alt="phone" width = 200>

 In some sense we can think about one edge being the *same edge* as the opposite edge. In 2 dimensions the only way to visualise this is with the snake crossing one edge to come back out the other side but thankfully we have access to 3 dimensions. I can glue one pair of edges together to form a cylinder and then glue the circular ends of the cylinder together to form a doughnut shape, called a *torus*.

<img src="/assets/images/torus.gif" alt="torus" width = 200>

And so <a href="https://tennessine.co.uk/snake-on-a-torus/">this game</a> which allows you to play snake on a torus and claims to be a fun spin off is in fact identical to the original game.

<img src= "/assets/images/torussnake.png" alt="snakeonadonut" width=200>

Importantly, the square was 2 dimensional and so is the torus. When I talk about the torus I really mean the surface of the hollow doughnut, not the inside. Think of an inflatable ring for swimming rather than a bagel.

Having seen that a torus is a rectangle with its edges identified you can hopefully appreciate that its relatively easy to find the frequencies that can emanate from a torus-shaped drum - just find the frequencies that can exist on a rectangular drum and impose periodic boundary conditions. 

Topology is an area of maths often referred to as rubber-sheet geometry. In geometry we can define quadrilaterals as a class of shapes without caring about their area, side lengths, or angles: only that they have 4 edges. Topology further relaxes the constraints required for two shapes to belong to the same class. In topology we say that two shapes are the same (homeomorphic) if they can be continuously defomed into one another, without any cutting or gluing. For an amazing introduction to topology I direct you to Vsauce's <a href="https://www.youtube.com/watch?v=egEraZP9yXQ">'How many holes does a human have'</a>.

<img src ="/assets/images/cow.gif" alt="cow" width = 200>

Quite quickly it becomes clear that most shapes we distinguish geometrically (cubes, stellated polyhedra, cows) are all topologically homemorphic to the sphere. Topology is the search for quantities which remain unchanged by continuous deformations (topological invariants). We can use these invariants to determine whether two shapes are homeomorphic or not without finding an explicit transformation between them or, even more difficult, showing that no such transformation exists.

It is a powerful result (the Classification theorem) that every (orientable, compact, connected, boundary-less) surface can be classified simply by the number of holes it has (its genus) and so the torus is the 'simplest' shape which isn't homeomorphic to a sphere - it has just 1 hole. After a donut we have a pair of handcuffs and a fidget spinner.

<img src = "/assets/images/genus2.png" alt="genus2" width=200>
<img src = "/assets/images/genus2.png" alt="genus3" width=200>

One fundamental difference between the sphere and the torus is that the latter is not simply connected. If I take a loop on the surface of a sphere, I can shrink it (staying on the surface) to a point on the sphere. Pretty quickly I can image a loop on the surface of a torus which can't be shrunk to a point on the surface: it "gets caught on the hole".

<img src = "/assets/images/simplyconnected.png" alt="sphere" width=200>
<img src = "/assets/images/notsimplyconnected.png" alt="torus" width=200>

Our construction of the torus involving gluing the edges of a square together can be phrased a little more algebraically. We can define an equivalence relation on $\mathbb{R}$ by identify points with the same decimal part, or that differ by an integer. Then every equivalence class has a representative in the interval $[0,1)$, where $1$ and $0$ are identified, so the quotient of $\mathbb{R}$ by $\mathbb{Z}$ is isomorphic to the circle. What about points in the Euclidean plane? Then I can define the same equivalence relation: that a pair of points are equivalent if they differ additively by an element of $\mathbb{Z}^2$ so that all my equivalence classes have a representative in the unit square where I now identify the edges, forming a torus as I described before. In this case I would write something like $\mathbb{T}^2 \cong \mathbb{R}^2/\mathbb{Z}^2 \cong S^1 \times S^1$: a point on the torus can be defined by two angles. This gives us a way to easily define higher dimensional analogues of the torus, as well as classifying any torus as $\mathbb{R}^2$ modulo some lattice.
