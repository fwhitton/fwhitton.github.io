---
title: "Maxwell's bright idea"
date: 2026-02-19
---

Our starting point is going to be Maxwell's equations for a magnetic field $\mathbf{B}$ and an electric field $\mathbf{E}$ in the absence of any charges:

$$
\nabla \times \mathbf{E}  = -\frac{\partial \mathbf{B}}{\partial t}

\nabla \times \mathbf{B} = \mu_0 \varepsilon_0 \frac{\partial \mathbf{E}}{\partial t}

\nabla \cdot \mathbf{E} = \nabla \cdot \mathbf{B} = 0
$$

We've got these constants $\mu_0$ and $\varepsilon_0$ baked into the equations and these are known as *vacuum permeability* and *vacuum permittivity* respectively, whatever that means. What's important is that these are features of the universe and all observers can agree on their value. Taking the time derivative of the first equation and commuting it across the curl gives us:

$$
\frac{\partial^2 \mathbf{B}{\partial t^2} = -\nabla \times \frac{\partial \mathbf{E}}{\partial t} = -\frac{1}{\mu_0 \varepsilon_0} \nabla \times (\nabla \times \mathbf{B})
$$

where in the second equality we've used the equation for the time derivative of the electric field. Can we say anything about the curl of a curl? We can and because I find index notation therapeutic, I'll even include the details:

$$
[\nabla \times \nabla \times \mathbf{B}]_i = \varepsilon_{ijk} \partial_j [\nabla \times \mathbf{B}]_k = \varepsilon_{ijk} \varepsilon_{klm} \partial_{jl} B_m = (\delta_{il}\delta_{jm} - \delta_{im}\delta_{jl}) \partial_{jl} B_m = \partial_{im} B_m - \partial_{ll} B_i = [\nabla(\nabla \cdot \mathbf{B}) - \nabla^2 \mathbf{B}]_i.
$$

But we know that the divergence of the magnetic field vanishes so we can replace our curl of curl of $\mathbf{B}$ with just the negative Laplacian leading to

$$
\frac{\partial^2 \mathbf{B}}{\partial t^2} = \frac{1}{\mu_0 \varepsilon_0} \nabla^2 \mathbf{B}
$$

Which says that the components of $\mathbf{B}$ obey the wave equation! And we can go through the same rigmarole to derive an identical equation for $\mathbf{E}$.



