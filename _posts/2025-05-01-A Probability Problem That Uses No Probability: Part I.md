---
title: "A Probability Problem That Uses No Probability: Part I"
date: 2025-01-05
---

 I'd like to share a problem which was covered in 3blue1brown's lockdown math lecture series and I found particularly delightful. This post is adapted from a talk I've given to year 12 further maths students in my sixth form, as the solution contains only A level maths content and I wanted to give a flavour for the abstractions of university maths. I promised myself not to recycle content from 3B1B as I believe he's the best maths educator on the internet and there's nothing I can add but this problem wasn't covered in full animated detail and I'd like to talk about measure theory. The problem goes as follows:
   
>Two numbers are randomly (independently) chosen between 0 and 1. We divide them and round down the number to the integer below. What is the probability that the resulting integer is even?

Or, for the maths symbol lovers like myself

>Given $X,Y\sim U(0,1]$ find $P\left(\lfloor \frac{Y}{X} \rfloor \equiv 0 \text{ mod }2\right)$.

Firsly I'd like to clarify what I mean when I say "randomly chosen between 0 and 1". The formulation "All numbers are equally likely to be chosen" is unfortunately not strong enough: more precisely, I mean that the probability that I pick a number between $a$ and $b$ is $b-a$. This should make sense though: I throw a dart at a numberline and the probability I land in some interval is just the length of that interval. This is called a *uniform distribtion*, similar to a rod with uniform density where the mass of a section is proportional to its length.

So how could we visualise two numbers being uniformly distributed between 0 and 1? Instead of picturing two points being chosen randomly on a numberline, I could choose a point at random in the unit square! Now the probability I choose a point in a certain region is the area of that region! We know a little bit about probability but we know a lot more about finding areas. So we just need to indentify the set of points in the square with coordinates $(x,y)$ for which $y/x$ rounds down to an even integer.

Maybe we haven't encountered this floor function malarkey before. Can we find an alternative characterisation? Yes: if a number rounds down an integer, that means it's greater than or equal to that integer but strictly less than the next integer. Specifically

A number $x$ rounds down to an integer $k$ if and only if $k \leq x < k+1$.

Now what if $y/x$ rounds down to $k$? Then 

$y/x$ rounds down to $k$ means that $k \leq y/x < k+1$

Now multiplying by $x$ gives

$kx ≤ y < (k+1)x$

There are 3 letters going on so let's keep track of what each one is doing: x and y can be any number between 0 and 1 and (x,y) is the coordinate of a point in the square, while k is any integer. Let's try a few values of k to get a feeling for the regions described. k = 0 corresponds to the region

$0 \leq y < x$

Which describes a triangle in the lower right corner of our square:
image

What about for $k = 1$? This corresponds to the region

$x \leq y < 2x$

Which describes a wedge bounded by the lines $y = x$, $y = 2x$ and $y = 1$:
image

Now what happens as I increase k? I get a family of wedges (an insult I'm reticent to use), becoming steeper and thinner, getting closer to the y axis. But remember I'm asking about rounding down to an *even* number so I only care about the case when k is even. This looks like the collection of triangles
image

I've only drawn the first few but since there are infinitely many even numbers, there's a triangle for each even number and our challenge is to find the shaded area. This means finding the area of each triangle and adding them all (infinitely many of them) together. 

The largest triangle is half the square, corresponding to the case $y<x$, which is equally likely as $x<y$. For the next one we'll use the fact that it has height 1 and try to find the base. The base is the difference between the intersections between the lines $y = 2x$ and $y = 3x$ with the line $y = 1$. Plugging $y = 1$ into each equation gives $x = 1/2$ and $x = 1/3$ respectively, so the length of the base is $1/2 - 1/3$. Then the area is

base $\times$ height / 2 = $(1/2 - 1/3)/2$

The next triangle goes similarly, where we find the intersection of the line $y = 1$ with the lines $y = 4x$ and $y = 5x$, giving a base of $1/4 - 1/5$. Hopefull that is enough to spot the pattern, that the $n$-th triangle which intersects the line $y = 1$ at 2 different points will have base $1/2n - 1/(2n+1)$ and height 1. Then we can write our total area as a sum, factoring out the half:

$$S = \frac{1}{2}\left(1+\frac{1}{2}-\frac{1}{3}+\frac{1}{4}+\cdots\right)$$

Now we just need to figure out what this sum equals... Noticing that it almost alternates plus/minus we're instead going to consider

$$S_2 = 1- \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \cdots$$

Now the ~~massive nerds like me~~ well-versed in series might recognise this one as $ln(2) \approx 0.691$. I normally hate when solutions pull out magic tricks like this but I think, given this solution is in danger of exceeding the length of a coffee, I'm going to save the proof of this one for another post. So how do we relate this number to our original sum and hence the answer to the problem? Multiplying $S_2$ by a half and adding it to $S$, we see that all the terms except the first cancel! This leaves us with

$$S + \frac12 S_2 = 1 \Rightarrow S = 1 - \frac12 \ln(2) \approx 0.65$$

I don't know about you but I find this a delightful result, with the guest appearance of a seemingly unrelated logarithm. This is where 3B1B leaves his solution but I do believe I have something to add in a following post which is an explanation as to why we can saunter so seemlessly between the worlds of probabilities and areas, across the bridge of measure theory. 
