# Inverse kinematics from orientation and position of end effector 3R planar robot

Having three links we have a redundant robot, so we can eliminate the redundancy to have an easier resolution. 

We assume that the last link lies on the direction from desired position to start-of-robot. This means we can compute the position of the end of link-2 and solve for first two joint variables (from these, the third joint variable is uniquely defined because the complexive angle is given by orientation and is their sum).

So we now consider a two link robot whose desired position is **real_position - [ l3 * cos(fi) ; l3 * sin(fi) ]**.

And the direct kinematic is **[ l1c2 + l2c12 ; l1s1 + l2s12 ]**.

**c2 = (dx^2 + dy^2 - l1^2 - l2^2 ) / (2l1l2)**
**s2 = +- sqrt(1 - c2^2)**

**Q2 = ATAN2(S2,C2)** should provide two different solutions (because s2 has two signs).

**Q1 = ATAN2( dy * (l1 + l2c2) - dx * l2s2 , dx * (l1 + l2c2) + dx * l2s2)**

**Q3 = FI - Q1 - Q2**
