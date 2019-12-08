#MP PRoblem 2 Python!!!

import numpy as np
import pandas as pd

#Input all the variables needed.
x1 = float(input('Input x1: '))
y1 = float(input('Input y1: '))
x2 = float(input('Input x2: '))
y2 = float(input('Input y2: '))
x3 = float(input('Input x3: '))
y3 = float(input('Input y3: '))

#Equations to finds the diameter.
a = (x1-x2)**2 + (y1-y2)**2
b = (x2-x3)**2 + (y2-y3)**2
c = (x3-x1)**2 + (y3-y1)**2
d = 2*(a*b + b*c + c*a) - (a**2 + b**2 + c**2) 

#Standard and General Equations of a Circle.
hn = (a*(b+c-a)*x1 + b*(c+a-b)*x2 + c*(a+b-c)*x3)
kn = (a*(b+c-a)*y1 + b*(c+a-b)*y2 + c*(a+b-c)*y3)
h = float(round( hn/d,3))
k = float(round( kn/d,3))
r = (a**0.5)*(b**0.5)*(c**0.5) / (((a**0.5)+(b**0.5)+(c**0.5))*(-(a**0.5)+(b**0.5)+(c**0.5))*((a**0.5)-(b**0.5)+(c**0.5))*((a**0.5)+(b**0.5)-(c**0.5)))**0.5
Darr=np.array([((x1**2)+(y1**2),y1,1),((x2**2)+(y2**2),y2,1),((x3**2)+(y3**2),y3,1)])
Earr=np.array([((x1**2)+(y1**2),x1,1),((x2**2)+(y2**2),x2,1),((x3**2)+(y3**2),x3,1)])
Farr=np.array([((x1**2)+(y1**2),x1,y1),((x2**2)+(y2**2),x2,y2),((x3**2)+(y3**2),x3,y3)])
Larr = np.array([(x1,y1,1),(x2,y2,1),(x3,y3,1)])
L = np.linalg.det(Larr)
D = -(np.linalg.det(Darr))/L
E = np.linalg.det(Earr)/L
F = -(np.linalg.det(Farr))/L

#Print the results.
print("Radius of the circle: ", float(round(r,3)))
print("Central coordinate of the circle: (",h ,",", k,")")
print(pd.DataFrame({'D':[D],'E':[E],'F':[F]},columns=['D','E','F']))
