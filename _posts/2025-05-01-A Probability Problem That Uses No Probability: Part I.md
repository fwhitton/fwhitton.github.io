---
title: "A Probability Problem That Uses No Probability: Part I"
date: 2025-01-05
---

 I'd like to share a problem which was covered in 3blue1brown's lockdown math lecture series and I found particularly delightful. This post is adapted from a talk I've given to year 12 further maths students in my sixth form, as the solution contains only A level maths content and I wanted to give a flavour for the abstractions of university maths. I promised myself not to recycle content from 3B1B as I believe he's the best maths educator on the internet and there's nothing I can add but this problem wasn't covered in full animated detail and I'd like to talk about measure theory. The problem goes as follows:
   
>Two numbers are randomly (independently) chosen between 0 and 1. We divide them and round down the number to the integer below. What is the probability that the resulting integer is even?

Or, for the maths symbol lovers like myself

>Given $X,Y\sim U(0,1]$ find $P\left(\lfoor \frac{Y}{X} \rfloor \equiv 0 \text{ mod }2\right)$z.
