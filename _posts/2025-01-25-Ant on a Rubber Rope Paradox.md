---
Title: "Ant on a Rubber Rope"
Date: 2025-01-25
---

In the previous post we mercilessly mocked an ant who was condemned to spend its entire life falling and so couldn't distinguish time from height. In this post about the next paradox we similarly toy with an ant, but this time the ant prevails in the end!

An ant starts at one end of a rubber rope of finite length and moves at a constant speed. However as it moves, we stretch the rope as to extend it at any speed we like. The paradox is that no matter how fast the ant is moving and no matter how fast we pull the end of the rope away from it, *the ant will always reach the end of the rope in finite time*. This should seem like a paradox: if we can pull the end of the rope away from the ant faster than it's moving, surely the distance between the two is growing? Let's elucidate.

<img src="/assets/images/Ant.png" alt="Ant" width=300>

The first key insight is that while the rope stretches, the section behind the ant stretches by the same factor as the section in front of the ant. Thus if the ant were stationary then its proportion of the way through the rope would remain unchanged as the rope stretches. This is helpful because the ant moves a constant speed *relative to the rope, not the ground*. Here we're modelling the ant as a point because if it has finite length then it gets stretched and presumably torn apart, a fate I couldn't bear to impose. 

We will represent the ants position (relative to the ground) as a functions $x(t)$ and its velocity relative to the rope as a constant $a$. The rope has initial length $c$ and is stretched a constant speed $v$. Therefore at time $t$, the rope's endpoint is at $c+vt$. Also the speed of any point on the rope, say $X$, increases linearly from $0$ at $X = 0$, i.e. the endpoint of the rope is fixed, to $v$ at $X = c+vt$ so the speed of a point on the rope $X$ at time $t$ is $vX/(c + vt)$. Then using our ~illegal~ Newtonian velocity addition law, the ants velocity $x'(t)$ (relative to the ground) must be 

$$x'(t) = a + vx/(c + vt).$$

Note that here we are considering a non-relativistic regime, so that we can use Newtonian velocity addition.  This is just a linear ordinary differential equation for $x(t)$ which can be solved with an integrating factor! (Wikipedia refers to this as "moderately advanced calculus" which embarassingly admits that Wikipedia didn't do A Level Further Maths.) When we solve we find that $x(t)/(c + vt)$ i.e., the proportion of the ant along the rope, is equal to $a*\log((c + vt)/c)/v$ which is for fixed $c$ and $v$ is unbounded with respect to t so most certainly reaches 1 in finite time! Once it reaches the end of the rope I guess it doesn't continue to accelerate, just moves at speed $v$ riding the end of the rope to infinity and beyond.

There's another solution to thisproblem in which the rope extends by a fixed amount each second and I think it's very pleasing but it relies on the divergence of the harmonic series and that's something I'd like to derive rather than quote so watch this space.

Is there a moral of the story here? Perhaps not in the problem solving sense but the ants are of course always metaphors for humans and although our goals seem unobtainable and evanescent, we do not notice that in the process of chasing them we are growing and accelerating ourselves.
