### Given time t and robot configuration and velocity at that time, plus the desired position wrt time. Acceleration command.

First we compute cartesian acceleration from desired position double derivation.

Then we need **direct kinematics**, **jacobian** and the **time derivative of the jacobian**.

So we can apply: **desired_acc = inv(J) * (desired_acc_cartesian - time_der_jacobian * (desired_pos - current_pos))**

### Assuming to be in initial state position , velocity such that position = desired_pos(0) but not equal velocity. Feedback law to recover cartesian error?

pd0 is the position at time zero.

Using inverse kinmeatics we can compute the possible solutions for joint 2 and 1. 

Then we must choose the correct velocity for the joints such that respect the difference between desired velocity.

The law control is as always:

**acc_joint = inv(J) * (acc_cart + Kd * (vel_cart_d - J * vel_joint) + Kp * (pos_d - pos_current) - derived_J * vel_joint)**

