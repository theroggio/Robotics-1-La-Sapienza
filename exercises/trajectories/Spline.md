# Plan trajectory upon samples

### Cubic spline trajectory

t1 = 1    q(t1) = 45°

t2 = 2    q(t2) = 90°

t3 = 2.5  q(t3) = -45°

t4 = 4    q(t4) = 45°

q'(t1) = q'(t4) = 0

A cubic spline is the connections of cubic functions, one for every ti to ti+1 time space. So we need to compute three cubic functions.
Everyone with a set of four dfferent parameters. 

They can be derived from the boundaries conditions (it would be so imposing continuity on velocity and acceleration on intemediate knots), imagine having the velocities at intermediate knots. 

A good way of doing it is imposing time law with normalized time (so time goes from 0 to 1 in every trait) as tau = (t - t1) / (t2 - t1).

Easier if we think about intermediate velocities as knows, to compute in their dependence all parameters. When using these velocities remember to multiply them (because everything's normalized) for (t_big - t_small).

So after comouting the two velocities everything is uniquely defined. 

### Find maximum velocity and acceleration and at which times they occurr

Knowing all the cubic polyoniamls we can easily understand the behaviour of the speed and acceleration. Then te maximum velocities has zero acceleration, from these infos we can compute max(speed) and when it occurres.

Same speech can be done with acceleration after computing the jerk. 



