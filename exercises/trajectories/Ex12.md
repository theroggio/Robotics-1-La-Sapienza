## Periodic trajectory 

Having two points A and B it's requested a trajectory starting from A, passing throught B and then going back to A (like a forever loop).

After solving the inverse kinematics to have joint space coordinates (not cartesian ones), a path can be expressed as:

**q(t) = q_i + A * (1 - cos(2 * pi * lambda(t))**

With lambda(0) = 0 and lambda(T)=1.

It's clear to see that q(0) = q_i and q(T/2) = q_i + 2 * A that we can properly choose to have q_i + 2 * A = q_f.

If the two configuration q_i an q_f are of the same type (elbow-up,elbow-down, etc) the trajectory does not encounter any singularity.

An alternative which follows the same joint path but with zero velocities at crucial points and also zero acceleration when it comes back to A is:

the usual cubic polynomial (also continuous up acceleration) **lambda(t) = 3 * (t/T)^2 - 2 * (t/T)^3**

