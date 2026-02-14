Following the problem from yesterday, I thought it'd be an insightful activity to model the situation in python. Here is the code I wrote which uses some rudimentary numpy. In no way am I suggesting that my code is optimal.The first block of code is simply importing several packages I'll need to use. Matplotlib is used to generate images, numpy makes it much easier to do operations with lists of numbers and cmath means I can use complex numbers 1 + 2j rather than lists [1,2].

<span style="color: #000000; font-family: Courier; font-size: 1em;">
from matplotlib import pyplot as plt
import numpy as np
import cmath
</span>

Then I define a function "rou(n)" that gives me the coordinates of a regular n-gon i.e. the starting positions of n dogs. I do this in the complex plane, hence they're called roots of unity. 

<span style="color: #000000; font-family: Courier; font-size: 1em;">
def rou(n):
    lst = []
    for i in range(n):
        lst.append(cmath.exp(0 - i*6.2832j/n))
    return np.array(lst)
</span>
