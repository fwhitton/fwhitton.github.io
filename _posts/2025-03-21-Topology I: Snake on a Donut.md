---
title: "Topology I: Snake on a Donut"
date: 2025-03-21
---

I'm of the age where my first phone housed only one game, snake. Snake is played in a rectangular world: if you try to escape out of one edge you are teleported to the opposite edge. It seems that modern iterations of the game have hardened the boundaries of the square, subverting my entire post but cast your mind back to when snake looked like this:

<>

 In some sense we can think about one edge being the *same edge* as the opposite edge. In 2 dimensions the only way to visualise this is with the snake crossing one edge to come back out the other side but thankfully we have access to 3 dimensions. I can glue one pair of edges together to form a cylinder and then glue the circular ends of the cylinder together to form a doughnut shape, called a *torus*.

<>

And so <this game> which allows you to play snake on a torus and claims to be a fun spin off is in fact identical to the original game.

Importantly, the square was 2 dimensional and so is the torus. When I talk about the torus I really mean the surface of the hollow doughnut, not the inside. Think of an inflatable ring for swimming rather than a bagel.

Having seen that a torus is a rectangle with its edges identified you can hopefully appreciate that its relatively easy to find the frequencies that can emanate from a torus-shaped drum - just find the frequencies that can exist on a rectangular drum and impose periodic boundary conditions. 

Topology is an area of maths often referred to as rubber-sheet geometry. In geometry we can define quadrilaterals as a class of shapes without caring about their area, side lengths, or angles: only that they have 4 edges. Topology further relaxes the constraints required for two shapes to belong to the same class. In topology we say that two shapes are the same (homeomorphic) if they can be continuously defomed into one another, without any cutting or gluing. For an amazing introduction to topology I direct you to Vsauce's <'How many holes does a human have'>.

<>


Quite quickly it becomes clear that most shapes we distinguish (cubes, stellated polyhedra, cows) are all topologically homemorphic to the sphere. Topology is the search for quantities which remain unchanged by continuous deformations (topological invariants). We can use these invariants to determine whether two shapes are homeomorphic or not without finding an explicit transformation between them or, even more difficult, showing that no such transformation exists.

It is a powerful result that every (orientable, compact, connected, boundary-less) surface can be classified simply by the number of holes it has (its genus) and so the torus is the 'simplest' shape which isn't homeomorphic to a sphere - it has just 1 hole. 
<>
<>

One way the fundamental difference between the sphere and the torus manifests is that it is not simply connected. If I take a loop on the surface of a sphere, I can shrink it (staying on the surface) to a point on the sphere. Pretty quickly I can image a loop on the surface of a torus which can't be shrunk to a point on the surface: it "gets caught on the hole".

<>
<>
I'd like to work a little more abstractly now, requiring a knowledge of quotients in algebra. Let's consider an equivalence relation on the real numbers whereby two numbers are identified if they have the same fractional part. Then every equivalence class has a representative between 0 and 1 so I need only consider the unit interval, the endpoints of which are identified. What a convoluted way to desribe a circle. In the language of algebra I would say that I've taken the real numbers modulo the integers and this is isomorphic to the circle. What about pairs of points in the Euclidean plane? Then I can define the same equivalence relation so that all my equivalence classes have a representative in the unit square where I now identify the edges, forming a torus as I described before. In this case the 2-torus is R^2 modulo the lattice Z^2. It hopefully makes some sense that the space of ordered pairs of points on the circle i.e. the Cartesian product of 2 circles is the torus. And so we can define the n-dimensional torus as R^n modulo Z^n.
