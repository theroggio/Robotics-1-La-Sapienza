# Exam 16 November 2018
## Exercise 3

Provide numerically the transformation matrix between base frame and frame 0. Robot is in the picture below:

<img src='https://github.com/theroggio/Robotics-1-La-Sapienza/blob/master/exercises/Denavit-Hartenberg/images/dhframe.PNG'/>

We cannot use the software to compute the transformation matrix (homogenous) because this frame is not part of the table! We need to compute the rotation matrix and then the shifting between the two frames.

From the pictures we see that: the orientation of the frames are the same, so the rotation matrix is the identity matrix.

Distance along the Z axis it's the height of frame 0 wrt base frame = **0.346**. 

Distance along X axis in *bottom* picture we see it's **0.220**. While distance along Y axis is **0.140** because one frame is at the angle and the other one is at the cneter, so we're halfing the length of that side.
