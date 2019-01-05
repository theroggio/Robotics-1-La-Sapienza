# Exam 11 July 2018
## Exercise 1

Define the orientation of a rigid body through three rotations by angles A, B, C around fixed axes in sequence Y, X, Z. Determine the rotation matrix, its determinant and if it's a possible rotation matrix.

Rotation around fixed axes need the pre-multiplication so:

R = rotationmatrix('Z', C)*rotationmatrix('X', B)*rotationmatrix('Y', A).

In Matlab / Mathematica the computation of determinant is trivial. To be a correct rotation matrix determinant should be 1 or -1. 
