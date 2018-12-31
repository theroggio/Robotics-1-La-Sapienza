## Trajectory for orientation expressed as rotation matrices

Remember we can express the rotation matrix as a sequence of euler angles and then we can express the angular velocity of the body with a mapping with its angle time derivative. 

For the rotation matrices expressing the initial and final orientation we have, except for singularcases, two solutions.

This means we could have up to four different trajectories. 

Let's consider for now the generic one that is a cubic plynomial as **a(t) = a_in + (a_end - a_in) * (3 * (t/T)^2 - 2 * (t/T)^3)** where a express the three angles.

It's easy to compute the generic velocity and acceleration. AS always the maximum velocity is at T/2. 

We can compute now some important values to use in order to evaluate the max angular veloicty and the minimum feasible time among all possible trajectories.

difference between initial and final angles | cos( beta(T/2) ) | alpha' * gamma' sign

To impose velocity limits (on angular velocity) we can compute the norm(w) at its max t = T/2. Body velocity in the trajcetory is a'(T/2) = (1.5 / T) * norm(a_fin - a_in) = (1.5 / T) * norm(w)

Generic norm(w) = transpose(w) * w = a'^2 + b'^2 + c'^2 + 2 * a' * g' * cos(b)

Plugging this in and then solving for T we can compute minimum time. 





