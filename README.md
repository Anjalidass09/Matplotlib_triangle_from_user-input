# Matplotlib_triangle_from_user-input
The following are the features of this project: 1. The user must input any two values (Eg: Base and Perpendicular) 2. The code must locate the third value (Eg: Hypotenuse) 3.You will be prompted to re-enter these values by the code. 4. In a few seconds, your triangle should appear.

import numpy as np
import matplotlib.pyplot as plt
from matplotlib.patches import Polygon
import math

RED = '\033[31m'
GREEN = '\033[32m'
BLUE = '\033[34m'
PURPLE = '\033[35m'
YELLOW = '\033[1;33m'

print(RED+"----WELCOME TO TRIANGLE GENERATOR----")
s = input(GREEN+"Please write\na to find perpendicular\nb to find base\nc to find hypotenuse")
if s == "a":
    b = float(input(PURPLE+"Please write the base: "))
    c = float(input(PURPLE+"Please write the hypotenuse : "))
    a= math.sqrt(c ** 2 - b ** 2)

elif s== "b":
    a = float(input(PURPLE+"Please write the perpendicular: "))
    c = float(input(PURPLE+"Please write the hypotenuse : "))
    b = math.sqrt(c ** 2 - a ** 2)


elif s == "c":
    a = float(input(PURPLE+"Please write the perpendicular: "))
    b = float(input(PURPLE+"Please write the base: "))
    c = math.sqrt(a ** 2 + b ** 2)

    print(GREEN+"THE PERPENDICULAR IS\t",a,"\nTHE BASE IS\t ",b,"\nTHE HYPOTENUSE IS\t",c)



p=input(BLUE+"Enter value of perpendicular:\n")
b=hypotenuse=input(BLUE+"Enter value of base:\n")
h=input(BLUE+"Enter value of hypotenuse:\n")
print(GREEN+"LOADING---------------------------------------------------------------")


pts = np.array([[1,1],[b,1],[1,p]])
pe = Polygon(pts,closed=False)
ax = plt.gca()
ax.add_patch(pe)
#BELOW COORDINATES CAN BE CHANGED ACOORDING TO THE SIZE OF YOUR TRIANGLE
ax.set_xlim(1,20)
ax.set_ylim(1,20)
plt.show()
