# Exam 11 July 2018
## Exercise 1

### General inverse kinematic problem given a rotation matrix, discussing singular cases. 

Given a rotation matrix we can use formulas to compute the three angles (minimal representation of the rotation); in this case we have a Roll-Pitch-Yaw matrix.

beta = atan2( R32 , +- sqrt(R31^2 + R33^2) )  

We obtain usually two results, for singular case (just one result - second cos(beta) = 0 , beta = pi/2 or -pi/2 depending on R32 value ).

alpha = atan2( - R32, R33) 
alpha' = atan2( R32, - R33)

gamma = atan2( -R12, R22)
gamma' = atan2( R12, - R22) 

When we're in the singular case we cannot provide two distintics solutions, but most of all we cannot provide an angle gamma and alpha, because they are rotation around the same axis; so we can just compute their sum (beta = pi/2) or difference (beta = - pi/2).



