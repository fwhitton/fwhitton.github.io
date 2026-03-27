---
title: "Time Reversibility and How E.Coli Swim"
date: 2025-03-09
---
If I let a ball roll down hill then it'll reach the bottom with some velocity. If I kick it back up the hill with the same velocity it'll reach its original position at rest, just as it started. But what if it reaches the bottom of the plane and rolls along a flat surface subject to friction? Then eventually it'll come to rest but there's no way to tell where the ball started. In some sense we've lost information. This is a matter of time reversibility. In an ideal system (no friction, energy conserved) I can 'run time backwards' and get back to my starting point. What this means in practice is that my governing equations are invariant under mapping $t$ to $-t$. Looking at Newton's 2nd law, if our force is time independent (like gravity) then acceleration picks up 2 minus signs from the chain rule when I swap $t$ to $-t$. On the other hand if I have something like a drag term proportional to velocity then this catches a minus sign from the chain rule so isn't invariant. We can think about this from a thermodynamic perspective: friction produces heat and so increases entropy, a process which won't be reversed.

The same phenomenon occurs in fluid dynamics: looking at the Euler equations (i.e., no viscosity)

$$
\rho \frac{D u}{Dt} = -\nabla p + f
$$

and assuming the force is time independent, then under the change $t\mapsto -t$, $u \mapsto -u$ as it is a time derivative, $d/dt \mapsto -d/dt$ and the advection term in the material derivative (which I've concealed here) has 2 copies of u so the entire equation is invariant. But inviscid fluids are only an approximation and the full Navier-Stokes equations,

$$
\rho \frac{D u}{Dt} = -\nabla p + \mu \nabla^2 u + f
$$

which contain the friction term "upside down triangle squared $u$" which is not invariant under time reversals. What this means is that if we have a solution to the Euler equations then we can run it backwards and it'll still be a solution (i.e., it'll behave like an inviscid fluid should) but a fluid that obeys the Navier-Stokes Equations does not obey them when run backwards. Analogous to the rigid body case, friction diffuses momentum and we lose energy to heat.

It doesn't take particularly long to get to the Navier-Stokes equations in fluids and from there we are famously stuck. We can only proceed through simplification and so we ask when it is valid to ignore certain terms in the Navier-Stokes equations to make them easier to solve. One way we can do this is to ask about the relative size of the viscosity term and see if we can throw it out. The quantity that allows us to do this is the Reynold's number, Re, named after Osborne Reynolds (sick name imho).

It doesn't make much sense to ask whether viscosity is high or low as to whether we can ignore its effects: we have to ask whether it is high or low relative to the other terms appearing. There's a standard method for this (non-dimensionalisation) and we find that we are in fact asking about the size of viscosity relative to typical length and speed scales. In practice, we cannot say whether water is viscous or not: it isn't if you're a boat but it is if you're a microorganism. We refer to situations with short length scales, slow speed scales and high viscosity as a low Reynolds regime. When this is the case we can discard certain terms and we end up with a new system, called the Stokes equations:

$$
\nabla p = \mu \nabla^2 u
$$

But these equations are time-reversible! The reason why is a little subtle: the fact that there are no time derivatives of u means that the flow is instantaneous: any change in the boundary conditions/applied force induces an immediate response from the fluid, there is no propagation of information. Time reversibility is a consequence of instantaneity: if I reverse the boundary conditions then the fluid immediately reverses in response. What does this mean in practice? It means that if I act with a force for some amount of time and then I act with the same force in the opposite direction for the same amount of time, I'll return to the original state. This sounds a lot like kicking and this is why e.coli can't swim front crawl. Instead, they've evolved a way to move that involves returning to the same state without undoing what they've already done: they evolved a tail-like flagellum and they whip that thing around like the propeller of a ship. E. coli don't know that they've developed a non-time-reversible mechanism because they live in a low Reynolds regime in which the Stokes equations govern, but still they persist.

Another lovely example of this is unmixing dye. If you add some drops of dye into water and stir, one couldn't possibly conceive of 'unmixing' them. But in a low Reynolds regime, i.e. an incredibly viscous fluid, what we've learned above tells us that we should be able to unmix. And we can see this in practice: I highly encourage you to watch <a href="https://youtu.be/UpJ-kGII074?si=3xB48AgEKNwqBpqu&t=26">this video<\a> of 3 drops of dye being mixed into some corn syrup and then being unmixed (it's 2 minutes long which I know is a big ask so you can skip through it and get the gist as long as you watch the last 20 seconds).



