---
title: You can balance a table on a wonky surface
date: 2026-05-29
---
I want to address the claim that, without needing to fold up a napkin to prop up one of the legs, I can always find a way to a balance a table in a level way on a wonky floor. The caveat being that I'm allowed to make the table any size I want. Let's dive in.

Firstly, what am I assuming about the table? This table is rectangular, with legs on the four corners and all four legs the same length. The task is find four points on my surface arranged in a rectangle that have the same height. Is this always possible?

Lets think about contour lines of a hilly region on a map. Contour lines are lines of constant height and so I to balance a giant table in the mountains I just need to find four points on the same contour line that make a rectangle. Well given some wobbly floor surface I can also consider the contour lines of that surface: the lines of constant height. I'm going to have to make a small assumption about the surface which is that it has a peak or a trough: a point at which I can balance a ball (either a stable position for a trough or an unstable one for a peak). If this is the case then a neighbourhood of that peak or trough the contour lines will be closed curves (i.e. loops) rather than lines which shoot off. Diagram.

So is it always possible to find 4 points on a contour line that make a rectangle? This is the famous inscribed rectangle problem and the surprising answer is yes! In fact a variant of this was proven by Andrew Lobb who taught me Geometric Topology at Durham and the precise statement is:
> Given a closed Jordan curve and a rectangle there exist four points on the curve which form the vertices of a similar rectangle to the one give
Here a Jordan curve just
>
this is a step towards the inscribed square problem, proving it in the case that the curve has no corners.
There is a great video by 3blue1brown proving a weaker version of the inscribed rectangle theorem.
