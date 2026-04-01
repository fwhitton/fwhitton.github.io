---
title: "Three Proofs of The Infinitude of The Primes"
date: 2025-11-04
---

A friend recently asked me "Have you seen the topological proof that there are infinitely many primes?" and I'm possibly in sparse company being excited by this sentence. It reminded me that I'd seen another insanely overpowered proof that there are infinitely many primes a while ago and so I'd like to present both of these along with Euclid's megaclassic proof.

Paul Erdős, the most published mathematician of all time, though agnostic, referred to god as the Supreme Fascist and believed that he held a book of the perfect proof of every theorem in maths. He would exclaim "This one's from The Book" when he saw a particularly elegant proof and the first of our proofs is undoubtedly one of these.

Suppose, for contradiction, that there are a finite number of primes. I'm going to consider the resulting number when I multiply all these finitely many primes together and add 1. This new number is not divisible by any of the primes. Indeed it leaves remainder 1 when divided by any prime, and so its only factors can be itself and 1, meaning I've generated a new prime. This contradicts the assumption that I could collect the finitely many primes. This proof is certainly from the book. But why stop there?

Goldilocks stumbled across that proof and decided it didn't require enough machinery. She tried the next one out for size. 

The Riemann zeta function is a bit of a holy grail in mathematics, its zeros having a million dollar bounty, but we can still handle it with elementary methods. The harmonic series (the subject of the sequel to the ant on the rope post) and the Basel problem are both examples of the Riemann zeta function:

$$
1 + \frac12 + \frac13 + \cdots = \infty
$$

$$
\frac1{1^2} + \frac1{2^2} + \frac1{3^2} + \cdots = \frac{\pi^2}{6}
$$

We can generalise the exponent in the sum and define the so-called Riemann zeta function:

$$
\zeta(s) = \sum_{n=1}^\infty \frac{1}{n^s} = \frac{1}{1^s} + \frac1{2^s} + \frac{1}{3^s}
$$

There is an intimate link between this sum and the prime numbers. Consider the following method, analogous to the sieve of Eratosthenes. Multiply the sum by $1/2^s$:
