# Circular trajectory of planar robot

## Specifics:

- Starting and ending point is P1, start and end velocity is zero

- Passing per P2

- Tangent at P2 has to be orthogonal to the segment P1-P2

- Timing law along Cartesian path should be a minimal polynomial

## Solution

The generic formula for a circle in the plane (considering its center as (0,0)) is **(x-x0)^2 + (y-y0)^2 = R^2**.

Imposing its passing for P1 and P2 we obtain two equations (that needs to be equal because they need to be on the same circle, with the same radius).
The third condition is the one that gives us the unique solution: the requirement of orthogonality means that the segment is in reality the diameter of the circle.

We can so compute the center (x0,y0) as the medium point between P1 and P2. The radius is obviously the length from this point to P1 (or P2, it's equal). 

The parametric arc length form is: path(s) = **x0** + **R** * **[ cos(s + theta) ; sin(s + theta) ]**.

Where **s** increase from 0 to 2pi. Theta is basically the starting angle that does not affect in any other way the path or its parametrization. 

The **timing law** can be expressed as a cubic polynomial (a + sb + s^2c + s^3d) imposing the marginal condition as path(0) = 0, path(T) = 2pi, w(0) = 0 and w(T) = 0. 

a = 0

b = 0

c = 6pi/T^2

d = -4pi/T^3

### What to do to make the trajectory safe under disturbs or initial errors?

If we start with a cartesian error at time t = 0 or if a disturbance move the end effector from its nominal trajectory, we need a feedback scheme to reduce the position error. It should be used a control as:

acceleration = inv(J) * position * [ desired acceleration + Kd * ( desired velocity - J(q) * velocity) + Kp * (desired position - end-effector-position) - jacobian_derivative * velocity ]

Where Kd and Kp are two diagonals gain positive matrices, this is good even to avoid problems generated from numerical approximations during the computations. 
