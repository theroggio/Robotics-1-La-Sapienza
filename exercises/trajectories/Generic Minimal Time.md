# Minimum time for general trajectory

In a general trajectory problem the minimum time motion is given by a trapezoidal profile (symmetric acceleration/deceleration and vmax cruise).
If |delta_pos| >= V^2 / A

Time_acceleration = V/A 

Time = |delta_pos|/V + V/A

Otherway T_a = sqrt(|delta_q|/A)   and T = 2 * T_a

In the case of initial and final velocities differenr from zero this can be helpful (positive velocities, it's faster to arrive to Vmax and to go back) or not (opposite velocities, it takes longer).

If velocities at end and beginning are different also times of acceleration / deceleration will be.

T_a = (V - vi) / A    and   T_d = (V - vf) / A

We know that the area of the trapezoid must be equal to delta_pos; imposing this and solving for T we have our minimum feasible time. 

### delta pos < 0

Formulas remain the same but we add instead of subtracting computing T_a and T_d.
