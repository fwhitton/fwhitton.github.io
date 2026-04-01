---
title: "Paradox 1: All horses are the same colour"
date: 2025-01-08
image: \assets\images\Horses.png
---

Before getting into the paradox, lets talk about proof by induction, a handy tool that is great for proving (or verifying) facts that we're told but awful at telling us why they're true. Induction is used to prove a statement about all whole numbers (perhaps after a point) and we start by showing that something is true for the smallest case, usually $n = 1$. Then we show that if the statement is true for some $n = k$, then it must be true for $n = k + 1$. Because it's true for $n = 1$ it must be true for $n = 2$. Now we know it's true for $n = 2$, we can conclude it for $n = 3$, and so on. A simple example is that we can reach any rung on a ladder because we can reach the first rung (the *base case*) and from any rung we can reach the next rung (the *induction step*).

The simplest example I can find is the sum of the first $n$ odd numbers is $n^2$. Firstly it's definitely true for $n = 1$ (and always worth checking for $n = 2$, $1 + 3 = 2^2$). Now suppose for some number $k$, the sum of the first $k$ odd numbers is $k^2$ (our *induction hypothesis*). Then adding the next odd number, which is $2k+1$, we get $k^2 + 2k + 1 = (2k+1)^2$, so if the statement holds for $n=k$ then it holds for $n=k+1$.

Now for an abuse of induction: all horses are the same colour. The argument goes as follows: in a set of one horse, there is only one colour, so the base case holds. Now assume that a set of $n$ horses has only one colour. Taking a set of $n+1$ horses, line them up (or enumerate them) and look at horses $1,\dots,n$. This is set of $n$ horses so by our hypothesis has only one colour. Now looking at horses $2,\dots,n+1$ we use the same reasoning to conclude that they only have one colour. But we can go through the whole set, looking at all $n+1$ subsets of $n$ horses and since each group of $n$ is the same colour, the group of $n + 1$ is the same colour. By induction, all horses are the same colour. QED?

I encourage you try and find the mistake yourself if it doesn't jump out at you immediately. Pause and ponder as 3B1B would say. I even left a hint in the post somewhere. 

<img src="\assets\images\Horses.png" alt="Horses" width=300>

The problem is subtle as the base case is certainly true and the induction step is almost perfect, except for the case $n = 2$. In that case we can look at the 2 subsets of size 1 and conclude that in each subset every horse is the same colour (as there is only one) but it is fallacious to conclude that the 2 are the same colour, since the subsets don't overlap.

