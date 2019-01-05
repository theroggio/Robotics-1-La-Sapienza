# Respective orientation

Given the orientation of two frames Ra and Rb, with respect to a reference frame-0 (all sharing same origin); dtermine a R(axis, angle) that express the rotation of Ra wrt Rb.

First we compute relative_orientation(Ra,Rb) that gives us a matrix. Then we have to solve the inverse kinematics on this matrix.

In this particular case (axis, angle) we have no a set of angles, but just one!

**sen(theta) = +- 0.5 * sqrt( (r12 - r21)^2 + (r13 - r31)^2 + (r23 - r32)^2 )**

We can easily compute **cos(theta)**. 

**theta = atan2(s,c)** 

**axis = (1 / 2 * r *sen(theta) ) * [ (r32 - r23) ; (r13 - r31) ; (r21 - r12) ]**

