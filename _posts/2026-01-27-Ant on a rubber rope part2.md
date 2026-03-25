---
Title: "Ant on a rubber rope part 2"
Date: 2026-01-27
---

 In the Ant on a Rubber Rope post I mentioned a discrete solution that I found very pleasing and I plan to present it here. I would normally recoil from anything that smells of 'discrete maths' but I think it turns out to be far more enlightening as the gut feeling that the ant *shouldn't* reach the end of the rope is the same feeling that the harmonic series *should* converge.

In this case we'll consider the situtation where instead of the rope stretching continuously, it gains a length of $v$ at the start of every second. So before the ant can even move the rope has length $c+v$. Then after a second it has length $c + 2v$ and so on. Let $p(t)$ be the proportion of the rope that the ant has covered at time $t$, so $p(0) = 0$. Then at $t = 1$, the ant has moved its speed, say $a$, along the $c + v$ length of the rope. Even though the rope stretches at this point, the proportion of the way through the rope is unchanged so 

$$p(1) = \frac{a}{c + v}.$$

Similarly in the next second the ant advances its position by $a$ which is $a/(c + 2v)$ from the starting point so 

$$p(2) = \frac{a}{c+v} + \frac{a}{c+2v}.$$

Hopefully we can see the pattern: 

$$p(n) = \frac{a}{c + v} + \cdots + \frac{a}{c + nv}.$$

Now for any $k$, 

$$\frac{1}{c + kv} > \frac{1}{kc + kv}$$ 

so that 

$$p(n) > \frac{a}/{c+v}\left(1 + \frac12 + \frac13 + \frac14 + \cdots + \frac1n).$$

Now this sum is more commonly known as a partial sum of the harmonic series and in fact it can be made as big as we like by taking enough terms! What that means is that $p(n)$ can be made as large as we like by taking $n$ large enough, so it can definitely reach 1.

So we've determined by another method that for a similar situation, the ant reaches the end of the rope. But what if you don't believe me that these fractions add up to infinity? After all they're getting smaller pretty quickly... Well if we group terms cleverly we see that the first term is one, the second term is a half and the next two terms ($1/3$ and $1/4$) add up to more than $1/2$. Then the next $4$ terms are all greater than or equal to an eighth so their sum must be more than $1/2$. And the next 8 terms are all greater than or equal to a sixteenth so their sum must be more than a half, and so on and so on. But clearly taking the sum of infinitely many halves is infinite and so we are forced to conclude that the harmonic series diverges!

I think that the continuous solution hides some of the revelation here because the ant getting closer to the end but never quite reaching it is the same idea behind a series converging. But since our series counter-intuitively diverges, so too does our ant. In fact the logarithm that comes up in the continuous case is actually similar to the asymptotic behaviour of the partial sums of the harmonic series.
