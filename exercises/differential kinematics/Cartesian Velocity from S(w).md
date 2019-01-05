# Velocity at position p

If angular velocity is computed as differentiation of angles (alpha', beta' and gamma') as w = z * alpha' + R1 * z * beta' ... etc

It can be useful to know the concept of S(w) (matrix used to compute cartesian velocities connected to a rigid body moving with angular velocity w).

**S(w) = [ 0 -wz wy ; wz 0 -wx ; -wy wx 0 ]**

Then having a cartesian position **p** we can compute **p' = S(w) * p** that replace the common **p' = w x p** that can be difficult to evaluate. 
