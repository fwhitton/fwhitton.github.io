---
Title: Sums of Square for kids
Date: 2026-05-21
---

This post arose out of an extended conversation I had with my 13 year old sister. By the end of the conversation she was able to determine which numbers could be written as a sum of squares (SoS) (e.g. $5 = 2^2 + 1^2$, $13 = 3^2 + 2^2$) and which numbers could not (e.g. $3$, $6$) based off some principles I had demonstrated only through the medium of examples. *a priori* we have no better method than trial and error: is $1079$ a SoS? My best bet is subtracting off all $32$ squares less than $1079$ and seeing whether a square remains. We would like to develop a method which is more robust and hopefully even explains *why* a number can or cannot.

We begin with a fact so fundamental it is called the fundamental theorem of arithmetic:

>**(1)** Every number can be written, in a unique way, as a product of prime numbers.

This is taught as factor trees e.g. $48 = 3 \times 16= 3\times 2^4$, $49 = 7^2$, $50 = 2\times 5^2$. Now for another fact

>**(2)** If two numbers can both be written as a SoS then their product can also be written as a sum of squares

for examaple,:  $5 = 2^2 + 1^2$, $13 = 3^2 + 2^2$, $5\times 13 = 65 = 8^2 + 1^2 = 7^2 + 4^2$. Notice that I haven't actually told you how we find the sum of squares of $65$ from the sums of squares of $5$ and $13$, only that it's possible. A formula exists (Brahamgupta's) but I won't include it lest this post stops being kid friendly. The first two facts mean that we can work out which prime numbers are SoS because if all a number's prime factors are SoS then the number must be too.

>**(3)** Every prime number (other than $2$) has remainder $1$ or $3$ when divided by $4$

e.g. $3,7,11,19$ are all remainder $3$ and $5,13,17$ are all remainder $1$. If a number had remainder $0$ it'd be a multiple of $4$ so wouldn't be prime and if it had remainder $2$ then it'd be even. Notice that just because a number has remainder $1$ that doesn't make it prime e.g. $9 = 4\times 2 + 1 = 3^2$. From now on 'remainder $1$' and 'remainder $3$' always mean 'when divided by $4$'.

> **(4a)** A prime number that is remainder $1$ can be written as a SoS

> **(4b)** A prime number that is remainder $3$ cannot be written as a SoS

> **(4c)** $2$ is the only prime number which is remainder $2$ and can be written as $2 = 1^2 + 1^2$.

I have to mention that it is easy to prove the contrapositive of **(4b)** but the proof of **(4a)** requires Legendre symbols. Using the first four facts we can now partially answer whether a number *can* be written as a SoS. e.g. $325 = 5\times 65 = 5\times 5\times 13$ and $5$ and $13$ are both prime numbers which are remainder $1$ so by fact **(4a)** they can be written as a SoS and then by fact **(2)** $325$ can be too because it is a product of numbers that can and indeed $325 = 18^2 + 1^2 = 15^2 + 10^2$. On the other hand e.g. $39 = 3\times 13$ and can't be written as a sum of squares. However $45 = 3^2 \times 5$ which can be written as a sum of squares ($45 = 6^2 + 3^2$) even though it has a prime factor which is remainder $3$ so our current method can tell us which numbers can be written as SoS but it is not yet able to tell us whether a number cannot be written as a SoS. 

> **(5)** If a number can be written as a SoS then that number multiplied by a square number can still be written as a sum of squares.

e.g. $5 = 2^2 + 1^2$ and $45 = 3^2 \times 5 = 3^2(2^2 + 1^2) = 3^2\times 2^2 + 3^2 \times 1^2= (3\times 2)^2 + (3\times 1)^2 = 6^2 + 3^2$.

A number which is a product of prime numbers which are remainder $1$ can be written as as sum of squares and multiplying by a square number or a power of $2$ doesn't change whether a number can be written as a sum of squares. Now we have all the pieces.

> **(6)** A number can be written as a SoS if and only if when decomposed into prime factors, all the primes which are remainder $3$ multiply together to make a square number.

Finally, some examples
1. $234 = 2\times 13 \times 3^2 = (1^2 +1^2)\times (3^2 + 2^2) \times 3^2 = (5^2 + 1^2) \times 3^2 = 15^2 + 3^2$ so $13$ is a remainder $1$ prime and multiplying by a power of $2$ and a square number doesn't change the fact that it can be written as a SoS.
2.  $40 = 8\times 5 = 2^2 (2 \times 5) = 2^2(1^2+1^2)(2^2 + 1) = 2^2(3^2 + 1^2) = 6^2 + 2^2$
3.   $25 = 5 \times 5 = (2^2+ 1^2)(2^2 +1^2) = 3^2 + 4^2$
4.    $98,000 = 98 \times 10^3 = 2\times 7^2 \times 2^3 \times 5^3 = 5 \times (7\times4\times 25)^2 = 5\times 700^2 = (2^2 + 1^2)\times 700^2 = 1400^2 + 700^2$

