## Maximum norm uncertainty

First we compute the encoder resolutions.

Then we solve the inverse kinematics for the current robot configuration.

Remembering the Taylor expansion **p = f(theta) + J(theta) * (theta - theta_s)**  we can assume that the difference is the delta of the resolution (our 'relative error').

We would have four possibilities ( with uncertainrties bot summed, one and one, inverse, both negative).

We should compute the final deltap for them all as **dp = J(theta) * dtheta**

Then compute their norms as usual. 
