# Direct Kinematics on DH frames

<img src='https://github.com/theroggio/Robotics-1-La-Sapienza/blob/master/exercises/Denavit-Hartenberg/images/img2dh.JPG'/>

To compute the direct kinematics from DH table we can just compute the single homogeneous transformation matrices (one for row) and then multiply them in the correct order to have a matrix expressing the end-effector position according to every joint variable.
In the picture we can see that the end effector is rotated with respect to the last frame of DH table (so we need a new matrix, whose rotation is a rotation matrix around Z axis of the angle beta, and whose displacement is zero).

From this matrix (4 by 4) we can extract the displacement and the orientation of the end-effector.

The displacement is the last column minus the last row (equal to 1).

The orientation is the minor 3-by-3 of the first three rows - first three columns. 
