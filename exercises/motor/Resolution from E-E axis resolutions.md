## Resolution on robot configuration partially assigned

Given a planar 2R robot with known link length and variable q2. Two motors drive the joints and they have an incremental encoder with pulses per turn r1 and r2. Motors have reduction ratios equal to N1 and N2.

It's requested a end effector resolution of delta_p. 

We know that **delta_p = J * delta_q**. To obtain delta_q from the incremental encoders info we must use the reduction ratios.

In this particular case it's required to use a rotation and compute it all from joint 2 because we have no info about first joint. 

- From direct kinematics we compute jacobian matrix.

- We rotate the jacobian matrix to frame attached to joint 2 -> J_2 = R12 * J (we obtain a matrix depending only on q2)

- We compute J_2 dividing each column for its reduction ratio.

- WE solve equations **delta_theta = [ N1 , 0 ; 0 , N2 ] * inv(J) * [delta_p ; 0]** and this same for a delta_p on y instead of x.

- We'll obtain a set of constraints about delta_theta (that is our resolution) it is 2pi/r. So we just need to explicity the constraints about r.
