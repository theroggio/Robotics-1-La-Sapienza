# Trajectory in joint space

When boundaries are given in the joint space it's better to solve it all in joint space.

So, solving inverse kinematics for initial position and terminal position we have delta_pos for both joints. We can find a trajectory for everyone of them and compute the minimum time.

The computation of the minimum time is the same: 

### Traepozoidal  **delta_pos > V^2 / A**

T_a = V / A

Area_trap = delta_pos  -> compute time

### Bang-bang 

T_a = sqrt(|delta_pos| / A)

time = 2 * T_a



Having minimum time for all joints, the real minimum taks time is the max we've computed, then we just need tor rescale the others by k = T_real / T_of_joint.

V_max_rescaled = Vmax / k

A_max_rescaled = A / (k^2)

## Cartesian path characteristic

Knowing direct kinematics and inverse kinematics of points we can understand if the joint path correspond to a linear cartesian path or not, just by inverting formulas and plug them in.
