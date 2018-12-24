# Exam 16 November 2018
## Exercise 5

### What's the orientation of the last frame?

A rotation matrix expressing the orientation of a frame can be computed with Euler angles or, in the case of DH tables, we can compute the homogeneous matrix expressing the transformation from reference frame and then taking it's 3x3 (first three rows and columns).
It obviously depends on joint variables values, so for different configurations we'll have different orientations. 
