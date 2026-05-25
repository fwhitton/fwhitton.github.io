---
Title: Top 7 types of derivative
Date: 2026-05-22
---

## 7. Ordinary

Got to start where it all started. You're on a hike and you know what the elevation is at each point but you want to know how steep it is at each point i.e. what is the gradient? This is precisely the question ``What is the (ordinary) derivative of the elevation as a function of distance?". Alternative to the usual slope interpretation, the derivative also measures the degree to which each point gets stretched or squashed when squeezing the domain into the co-domain.

## 6. Partial

I can look at how one location and compare how it changed over time: call this history. Alternatively I can look at a fixed point in time and compare different places: call this geography perhaps. What about something like the Roman empire which spread over time: I could follow the path of a Roman legion as it moves through space and time and measure something along its path: this would be called a directional derivative. As I said in the post on **partial** differential equations, *most things depend on more than one thing* and so it's important we know how something responds to changes in the various things it depends on.

## 5. Material

Imagine a bear sitting on the bank of a river with a fishing rod. It looks at the river and wonders how fast it's flowing at each point. It could take a snapshot in time and look at how the flow of the river changed from point to point. It could also look at a point in the flow and see how the flow changes over time, say by attaching a detector to the river bed. However this is only one perspective (called the Eulerian one). If I were a fish being carried along in the flow, hoping to avoid the bear's fishing rod, (whaling, fishing, crabbing are the only examples I can think of where turning an animal's name into a verb means to hunt that animal) I would experience speeding up, slowing down and changing direction. This is a more natural way to phrase the laws of fluid mechanics. A point that is carried along in the flow is affected by its neighbouring points which are carried along in the same flow. This idea is encapsulated by the material derivative. I talk about this in more depth in my Navier-Stokes post.

## 4. Weak

Suppose I want to loosen the sense of what it means for a function to have a derivatve. I can only differentiate some functions but I can integrate *way* more functions. Therefore it makes sense to ask for functions that satisfy conditions in integrals: integrals are blind to finite sets of points (and even sets of measure zero) and so is more lenient to functions with pesky discontinuities in their derivative like the absolute value $f(x) =|x|$. The way we phrase this is that a function is weakly differentiable if we can do integration by parts on it. Specifically, $u$ has weak derivative $v$ if for all smooth functions $\phi$, 

$$
\int u(x)\phi'(x) = -\int v(x)\phi(x).
$$

A small problem: by broadening the class of possible solutions to an equation, we've exchanged uniqueness for existence. Two different functions can satisfy the above condition which disagree on a set of measure zero. The boundary of a domain is a set of measure zero so what does it even mean for a weak solution to satisfy a boundary condition?

## 3. Radon - Nikodym

I want to assign sizes to parts of a material in a consistent way. Two possible ways for me to do this are by measuring the volume or the mass of a chunk. Volume might seem like the natural choice but mass is just as good and they are related by the fact that if I know the density of the material (a positive function) $\rho$ then the mass of a subset, denoted $M(E)$, is related to the volume of that subset, denoted $V(E)$, by

$$
m(E) = \int_E fdV.
$$

So in a sense we can build new measures (ways of assigning size to sets) out of old ones using a density function. The Radon-Nikodym theorem goes the other way and states that if I have two measures $\mu$ and $\nu$ with the property that $\nu(E)$ is $0$ whenever $\mu(E)$ is $0$ (specifically $\nu$ is absolutely continuous with respect to $mu$ which is written $\nu \ll \mu$) then there is a non-negative density function $f$ so that 

$$
\mu(E) = \int_E f d\nu
$$

and the density is called the Radon-Nikodym derivative and even denoted $f = \frac{d\mu}{d\nu}$.

## 2. Exterior


## 1. covariant
