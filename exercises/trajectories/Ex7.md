## Non-linear trajectory

If is given a direction for the end effector at the end of the path and this direction is not along the linear path, it means we cannot use a linear path and have a smooth trajectory.

There are many possibilities, one of them is using a **p(s) = a + bs + cs^2** quadratical trajectory.

Knowing starting point, ending point and ending direction (tangent) we can derive the parameters.

### Parametric trajectory

The s(t) must be computed as a cubic polyonomial as always, for which s(0)=0, s'(0)=0, s(T)=1 and s'(T)=velocity_required

### What's the cartesian velocity at time tx

p'(t) = p'(s(t))*s'(t)

If we want to know solutions in joint space we must solve the inverse problem (for trajectory point) and ivnerse differential problem for the velocity.

This second one starts from the Jacobian that must be computed at trajectory point so that:

q'(t) = inv(J) * p'(t)
