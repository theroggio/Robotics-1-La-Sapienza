# Determine the geometric Jacobian

Given DH tables (or any other way to compute direct kinematics) f(q) we can build the jacobian. 

The geometric Jacobian has three rows equal to the analytic jacobian (just derivation of f(q) for all joint variables). 

For the angular part: every column of a prismatic joint is all zeros (no angular contribution). For all the others joint the column is given by the z axis direction in the reference frame. 

For every column that is not the first it means taking the third column of the rotation matrix derived by the multiplication of Ra * Rb * ... * Rz with a = 01 to z = mn (n is the number of the column / variable joint).


