# Exam 16 Novembre 2018
## Exercise 4

A revolute joint is actuated by a DC motor driven by voltage Va. We know the armature resistance = 0.309 [Ohm], viscous friction 5 * 10^-2 [mNm/rad/s] and current-to-torque gain 7.88 [mNm/A].
A harmonic drive reduced with flexspline of 256 externa teeth is used as transmission element. At steady state the output is moving at speed w = 180°/s in counterclock wise direction.

### What is the value of the applied voltage Va? And the rotation speed of the motor?

We know electrical and mechanical laws for DC motor:

L * di/dt = Va - R * i - kv * wm

Im * wm/dt = kt * i - Fm * wm - Tl

We have no infos about Tl so we can assume it's zero. If we're at setady state we have no di/dt, so first law can be expressed as:

Va = R * i + kv * wm

and for second lawis the same, with no wm/dt:

kt * i = Fm * wm 

We know that kt and kv are equal (expect for unit measure), we use the SI units to obtain kv = 7.88 * 10^-3 V/(rad/s). 

The hramonic drive has a reduction ratio n = #external teeth / 2 = 128 and it invert the rotation, so given the output speed we know that the motor produces a speed wm = - n*w.

**wm** = - 128 * 180°/s = - 402.1239 rad/s [it's clockwise direction, because the first w was counter-clock-wise]

i = (Fm * wm)/kt = - 2,5515 A.

**Va** = R * i + kv * wm = 0.309 * (-2,5515) + 7.88 * 10^-3 * (-402.1239) = -3.9572 V.

