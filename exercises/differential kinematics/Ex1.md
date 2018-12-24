# Exam 11 July 2018
## Exercise 1

### Find mapping between time derivative of minimal representation and angular velocity of the rigid body. Discuss invertibility of the mapping.

If we interpret the rotation matrix as a current axis rotation (if it was fixed axis just reverse the order of angles) we can compute for every axis its contribution to the angular velocity.

Basically we need to compute a 3-by-3 matrix, the last column is the simplest one because it's in the current axis so it's just ( 0 0 1 ).

The other columns need to be computed from the right column of the rotation matrix eliminating the rotations that follows (so for X velocity, being rotation around X just before rotation around Z, we need to eliminate the rotation around Z multiplying by it).

So X contribution is given by **rotationmatrix('Z', gamma) * ( 1 0 0 )**. 

While Y contribution is **rotationmatrix('Z', gamma) * rotationmatrix('X', beta) * (0 1 0)**.

Obtained the matrix so composed we can consider it's not invertible if has det(M) = 0. If it is the case it means exists a sub-space of angular velocities that cannot be represented by any choice of the differential angular speeds.
