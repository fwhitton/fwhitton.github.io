---
Title: A Probability Problem That Uses No Probability: Part II
Date: 2025-01-06
---

In the previous post I deprived you of a derivation and I now plug that hole. On reflection, I much prefer the method of maths youtuber Michael Penn who spends sometimes half a video arming himself with a set of 'tools' before facing the task in hand, deploying his arsenal where necessary. This feels more pedagogically elegant and in future I hope posts 'like this' will precede posts 'like the previous one'.

We are trying to prove that a certain alternating series is equal to the natural logarithm of 2. The following derivation (I won't use the word proof as to address issues of convergence would detract from the plot) contains some, for lack of a better phrase, magic tricks.

Firstly we'll do a clever rewriting: the feeling of adding and subtracting fractions might trigger a memory of computing the definite integral of a polynomial.

$$1 - \frac12 + \frac13 - \frac14 + \cdots = \left[x- \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4] + \cdots\right]_0^1$$

Then the Fundamental Theorem of Calculus allows us to write this back in terms of an integral:

$$=\int_0^1 (1- x + x^2 - x^3 + \cdots)\,dx$$

If we've encountered one infinite series then it's the geometric series and we notice this fits the bill with first term 1 and common ratio $-x$!

$$= \int_0^1 \sum_{n=0}^\infty (-x)^n\,dx = \int_0^1 \frac{1}{1-(-x)}\,dx = \ln(1_x)|_0^1 = \ln(2)$$

And this is an integral that hopefully looks familiar! We can integrate directly, substitute the bounds and voila! While the first steps might have felt a little out the blue, let's review the structure of the argument. We had an infinite series, but we only know about the geometric series. So we transform this series into a geometric series inside an integral, apply our trusty formula then pull it out of the integral by computing an antiderivative. But if we're going to go to the effort of learning a trick, what's the fun in only using it once. I hear you scream "But Fin, can we calculate the values of any other series with this method?!" I'm so glad you ask. I include below a similar use, going the other direction this time and the explanations of the steps are identical to the above. I haven't set up the align environment in markdown yet.

$$\pi/4 = \tan^{-1}(1) - \tan^{-1}(0) = \int_0^1 \frac{d}{dx} tan^{-1}(x)\,dx = \int_0^1 \frac{1}{x^2 + 1}\,dx$$

Fundamental theorem of calculus invoked, now for the geometric series:

$$\pi/4 = \int_0^1 \sum_{n=0}^\infty (-x^2)^n = \sum_{n=0}^\infty (-1)^n \int_0^1 x^{2n}\,dx = \sum_{n=0}^\infty \frac{(-1)^n}{2n+1}$$

These results feel like 2 sides of the same coin: is there any way we could have derived both in one fell swoop? We can, using complex numbers. It feels a little circular since we need the Taylor series of the natural logarithm, something we haven't used here, but we can derive this by calculating the complex logarithm of the number $1 + i$ in 2 different ways. Firstly we use Euler's formula to write $1 + i$ as $\sqrt(2)\e^{i\pi/4}$ and then we use the Taylor expansion and compare real and imaginary parts: like a wise and economic professor, I leave this as an exercise.

This post has been a bit more technical than previous ones but I promise something more philosophical about measure theory in the next post.

