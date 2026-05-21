---
Title: Sums of Square for kids
Date: 2026-05-20
---

I aim to fully characterise which numbers are expressible as a sum of two perfect squares only through the medium of examples.

We can try to write some numbers as a sum of squares (SoS) e.g. $5 = 2^2 + 1^2$, $13 = 3^2 + 2^2$, but some numbers cannot e.g. $3$, $6$. Currently we have no better method than trial and error for determining whether a number can be written as a SoS \eg is 1079 a SoS? We would like to develop a method for figuring out whether a number can or cannot be written as a SoS and hopefully this method even explains *why*.

>Every number can be written, in a unique way, as a product of prime numbers.

This is taught as factor trees \eg $48 = 3 \times 16= 3\times 2^4$, $49 = 7^2$, $50 = 2\times 5^2$.

>If two numbers can both be written as a SoS then their product can also be written as a sum of squares

This is possible to prove but I'll give an example instead:  $5 = 2^2 + 1^2$, $13 = 3^2 + 2^2$, $5\times 13 = 65 = 8^2 + 1^2 = 7^2 + 4^2$. Notice that I haven't actually told you how we find the sum of squares of $65$ from the sums of squares of $5$ and $13$. The first two facts mean that we can work out which prime numbers are SoS because if all a number's prime factors are SoS then the number must be too.

> Every prime number (other than 2) has remainder 1 or 3 when divided by 4

e.g. $3,7,11,19$ are all remainder $3$ and $5,13,17$ are all remainder 1. If the number had remainder 0 it'd be a multiple of 4 so wouldn't be prime and if it had remainder 2 then it'd be even. Notice that just because a number has remainder 1 that doesn't make it prime \eg $9 = 4\times 2 + 1 = 3^2$.

> 1. A prime number that is remainder 1 can be written as a SoS
> 2. A prime number that is remainder 3 cannot be written as a SoS
> 3. is the only prime number which is remainder 2 and can be written as $2 = 1^2 + 1^2$.

Using the first three facts we can now partially answer whether a number *can* be written as a SoS. \eg $325 = 5\times 65 = 5\times 5\times 13$ and $5$ and $13$ are both prime numbers which are remainder 1 so by the third fact they can be written as a SoS and then by the second fact 325 can be too because it is a product of numbers that can and $325 = 18^2 + 1^2 = 15^2 + 10^2$. Also e.g. $39 = 3\times 13$ and 3 is remainder 3 and so can't be written as a sum of squares so neither can $39$. However $45 = 3^2 \times 5$ which can be written as a sum of squares $45 = 6^2 + 3^2$ even though it has a prime factor which is remainder 3 so our method can tell us which numbers can be written as SoS but it is not yet able to tell us whether a number cannot be written as a SoS. 

> If a number can be written as a SoS then that number multiplied by a square number can still be written as a sum of squares.

e.g. $5 = 2^2 + 1^2$ and $45 = 3^2 \times 5 = 3^2(2^2 + 1^2) = 3^2\times 2^2 + 3^2 \times 1^2= (3\times 2)^2 + (3\times 1)^2 = 6^2 + 3^2$.

The important point is that a number which is a product of prime numbers which are remainder 1 can be written as as sum of squares and multiplying by a square number or a power of 2 doesn't change whether a number can be written as a sum of squares. Now we have all the pieces. 

>    A number can be written as a SoS if and only if when decomposed into prime factors, all the primes which are remainder 3 multiply together to make a square number.

Finally, some examples
1. $234 = 2\times 13 \times 3^2 = (1^2 +1^2)\times (3^2 + 2^2) \times 3^2 = (5^2 + 1^2) \times 3^2 = 15^2 + 3^2$ so 13 is a remainder 1 prime and multiplying by a power of 2 and a square number doesn't change the fact that it can be written as a SoS.
2.  $40 = 8\times 5 = 2^2 (2 \times 5) = 2^2(1^2+1^2)(2^2 + 1) = 2^2(3^2 + 1^2) = 6^2 + 2^2$
3.   $25 = 5 \times 5 = (2^2+ 1^2)(2^2 +1^2) = 3^2 + 4^2$
4.    $98,000 = 98 \times 10^3 = 2\times 7^2 \times 2^3 \times 5^3 = 5 \times (7\times4\times 25)^2 = 5\times 700^2 = (2^2 + 1^2)\times 700^2 = 1400^2 + 700^2$

