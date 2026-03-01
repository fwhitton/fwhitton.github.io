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
>A number $x$ rounds down to an integer $k$ if and only if $k \leq x < k+1$.

Now what if $y/x$ rounds down to $k$? Then 

>$y/x$ rounds down to $k$ means that $k \leq y/x < k+1$

Now multiplying by $x$ gives

$kx ≤ y < (k+1)x$

There are 3 letters going on so let's keep track of what each one is doing: x and y can be any number between 0 and 1 and (x,y) is the coordinate of a point in the square, while k is any integer. Let's try a few values of k to get a feeling for the regions described. k = 0 corresponds to the region

0 ≤ y < x

Which describes a triangle in the lower right corner of our square:
