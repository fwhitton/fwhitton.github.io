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
def plotty(xlst):\n
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
