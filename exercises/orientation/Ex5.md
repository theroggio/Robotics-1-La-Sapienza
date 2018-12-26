# Orientation and Position from other references

### Given two robots, one has a certain position and orientation specified in the joint spaces. We want the other robot to start in the same position but with orthogonal orientation. Considering frame displacements and rotation.

First we compute with direct kinematic the position of the end-effector in the reference frame. Then displacement and rotation matrix between the two frames.

The position of the robot-2 in his frame can be computed as pr2 = T * pr1. Where T is the transformation matrix computed from rotation and displacement.

For the orientation we first compute the Jacobian (in reference frame), so we know that the speed of first robot in cartesian space is J * q' (q' given). 
Easy to compute cartesian speed for robot-2 as rotation_between_frames * speed_robot1_cartesian.

So the orientation, as complessive angle of last frame wrt first frame is **fi = atan2( speed_y, speed_x) (-+ constant values if specified).

Remember that this orientation is basically the anlge between last and first frame! so it's not last angle (last joint variable)!

For inverse kinematics on this problem: <a href='https://github.com/theroggio/Robotics-1-La-Sapienza/blob/master/exercises/inverse%20kinematics/Ex5.md'> here </a>.
