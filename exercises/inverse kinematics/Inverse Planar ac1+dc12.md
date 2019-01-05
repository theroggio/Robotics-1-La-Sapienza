# Inverse kinematics for 2R planar robot

Given the end-effector desired position **pd** and the direct kinematics **f(q)** we need to find the closed form solutions.

f(q) = [ Ac1 + Dc12 ; As1 + Ds12 ]

### First step

If we square and sum the two values and put it equals to the square sum of **pd** components we obtain:

pd_x^2 + pd_y^2 = A^2 + D^2 + 2AD * [c1 * c12 + s1 * s12 ]

pd_x^2 + pd_y^2 = A^2 + D^2 - 2AD * c2

c2 = ( A^2 + D^2 - pd_x^2 - pd_y^2 ) / 2AD

#### CHECK

If the values of the cosine is not in [-1 , 1] it's not a possible value then we're in a singularity. 

### Second step

We can easily compute the two possible s2 from first fundamental law: s2 = +- sqrt(1 - c2^2).

**Q2 = atan2(s2,c2) two results**

### Third step

Now for every result of Q2 we need to compute the value for Q1. This needs a more difficult manipulation of the formulas. 

We need to isolate s1 and c1 (basically we need to avoid the c12 and s12 term because we do not know them).

s1 = (As1 + Ds12) * (A + D * c2) - (Ac1 + Dc12) * D * s2

c1 = (Ac1 + Dc12) * (A + D * c2) + (As1 + Ds12) * D * s2

**Q1 = atan2(s1,c1)**
