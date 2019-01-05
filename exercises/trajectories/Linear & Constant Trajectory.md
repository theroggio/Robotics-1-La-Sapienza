## Linear trajectory specifications

Given two points and the specific of a straight line trajectory first of all we need to check if it's all in the robot workspace.

The desired initial velocity at t=0 is **p'(0) = const_v * (p_f - p_i) / norm(p_f - p_i)**

To know which is the initial configuration of the robot we need to solve the inverse problem. 

Then we can compute the jacobian in this point and solve for the **vel_joint = inv(J) * vel_cart**

