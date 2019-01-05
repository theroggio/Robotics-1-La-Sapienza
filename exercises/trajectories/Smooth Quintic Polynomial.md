# RP robot smooth - trajectory

Given initial position and terminal position, to be achieved in time T. We want a smooth trajectory with zero velocity and acceleration at beginning and ending. 

To have smoothness we require a quintic polynomial function. Computing the displacement dQ = q_end - q_init we can use the normalize form of the function as:

**q(t/T) = q(0) + dQ * (a * (t/T)^5 + b * (t/T)^4 + c * (t/T)^3)**

Imposing velocity, acceleration and positions as boundary condition we find the trajectory as:

**q(t/T) = q(0) + dQ * ( 6 * (t/T)^5 - 15 * (t/T)^4 + 10 * (t/T)^3 )**

### Compute max velocity and acceleration

To compute max velocity we need to put acceleration = 0 and find the time, then using that time we can compute the velocity value. Same for acceleration putting jerk = 0. 

If these values are not the maximum achievable we can speed up the motion of a scaling factor. The maximum scaling factor is computed separately for every joint and then is taken the minimum (because it's the one every joint can achieve).

To compute the scaling factor, for every joint: **min( Vmax / Vmax_reached , sqrt( Amax / Amax_reached) )**

