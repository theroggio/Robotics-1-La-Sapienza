## Double task at same time

Considering a planar 4R robot we want the end effector to move with velocity VE and a mid point to move with velociti VM. 

First we compute the jacobian both at the middle point and at the end effector. It's better if the end effector jacobian can be expressed as sum of kinematics until mid-point and then their connection.

If it is the case it measn we can then solve first for mid-point velocity and then correct and add just the right velocity for the end-effector (considering the movement already commanded for midpoint).

This can be done computing a fake Jacobian = [ jacobian_mid_point , 0 ; jacobian_mid_point_in_ee , jacobian_mp_to_ee ].

This means that having Ve and VM we need to solve for joint velocities as usual or in two distinct equations (one for midopint and one for end effector).

**q' = inv(fake_jacobian) * [VM ; VE]**

**q'_midpoint = inv(midpoint_jacobian) * VM** and **q'_ee = inv(J_from_mp_to_ee) * (VE - J_mp_of_ee * q'_midpoint)**

Pay attention to singularities that needs to be treated separately - most of all, a singularities in the second part of the path to the end-effector could not affect the midpoint velocity and its realization. 
