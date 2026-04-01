---
title: "Dogs Chasing One Another Part 2"
date: 2025-01-04
image: /assets/images/Figure_1.png
Following the problem from yesterday, I thought it'd be an insightful activity to model the situation in python. Here is the code I wrote which uses some rudimentary numpy. In no way am I suggesting that my code is optimal.The first block of code is simply importing several packages I'll need to use. Matplotlib is used to generate images, numpy makes it much easier to do operations with lists of numbers and cmath means I can use complex numbers 1 + 2j rather than lists [1,2].

```python
from matplotlib import pyplot as plt
import numpy as np
import cmath
```

Then I define a function "rou(n)" that gives me the coordinates of a regular n-gon i.e. the starting positions of n dogs. I do this in the complex plane, hence they're called roots of unity. 

```python
def rou(n):
    lst = []
    for i in range(n):
        lst.append(cmath.exp(0 - i*6.2832j/n))
    return np.array(lst)
```
'Plotty' is a function that will plot the curves once I figure out what they are.
```python
def plotty(xlst):
    plt.plot(xlst.real, xlst.imag)
```
I then define a few variables: 'eps' is how close the dogs can be before I consider them to be 'basically touching' (a small number, conventionally named epsilon); 'k' is the length of the steps that I'd like the dogs to take (small so the curves look smooth from a distance); and 'n' is the number of dogs. I initially wrote this program for 4 dogs and then challenged myself to generalise it for any number.
```python
eps = 0.01
k = 0.05
n = 4
A, B, C = rou(n), np.zeros(n), np.zeros(n)
lst = [A]
```
Now everything is set up, the while loop says that while the dogs are further than "epsilon" apart, we will repeat the following process. I find the direction each dog must move to reach the next dog (C = B - A) and the each take a small step (of length k) in that direction (A = A + k*C). Then their chase has moved so they need to readjust the direction in which they are moving and the process repeats. After each step the coordinates of the dogs are stored in 'lst' and I end by plotting the paths of each dog.
```python
while abs(A[1] - A[0]) > eps:
    B = np.roll(A, -1)
    C = B - A
    A = A + k * C
    lst.append(A)
lst = np.array(lst)
lst2 = np.transpose(lst)
for i in lst2:
    plotty(i)
plt.gca().set_aspect('equal')
plt.show()
```
This generates the image shown in the last post

<img src="/assets/images/Figure_1.png" alt="spiral" width =200>

There are no crazy operations here: once I have the starting positions, all I need to do is addition, subtraction, multiplication and find a distance. But there's no such thing as a free lunch: the inherent limitation is that the resulting curve is made up of many straight line segments. Ok, to rectify this we could make k smaller? then the curves would definitely look smoother. They'd look smoother and smoother until I made k zero, when there would be no curves at all because the dogs wouldn't move. So somehow we want to consider a theoretical 'limiting' curve with no corners that the curves get closer to as k gets closer to zero, without it actually being 0. This is the arena of calculus. Reframed in calculus terms, we have 4 curves and the tangent vector to each curve is the direction vector between a point on one curve and the corresponding point on the next (normalised to have fixed length). We are looking for 4 curves, each parametrised by time, satisfying initial conditions: 

$$x_1(0) = i, x_2(0) = 1, x_3(0) = -i, x_4(0) = -1.$$

The direction vector from a point to another is the position vector of the destination minus the position vector of the starting point so equating this to the tangent vectors gives:

$$\dot{x}_1 = x_2 - x_1,\cdots,\dot{x}_x = x_1 - x_4$$

This is a coupled system of 4 ordinary differential equations. Is it worth actually solving this system? I'm not sure the solution is all that illuminating. Instead let's focus on two regimes presented above: is either preferable? This problem is fairly mundane but getting into anything spicier such as fluid flow our analytic methods fail and we rely on the numerics of computers. Is this a win for the programmers? A sign that the analytic (myself included) are overreaching with their bag of tricks and ultimately it is the programmers who will instruct the rockets how to evacuate Earth? I think we both have much to learn from each other.
