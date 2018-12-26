# Incremental encoder to measure position of motor

### It's needed to emasure the position of the tip of a link (motor driven) with a resolution of 0.01 [mm]. The incremental encoder can measure the angular position with a quadrature detection. The motor can have maximum torque t_m. 

If the encoder use angular position we first need to understand which is the angular resolution needec (we have it in mm, linear). 

The angular resolution at the tip of the link can be computed as the linear resolution / length of the link. This need to be converted into the angular resolution at the motor (so if there are any reduction ratios they need to be taken into account).

In the case of a spur gear or bevel gear with radius R1 and R2 the reduction ratio is R1/R2. Where R1 is where we know info and R2 is towards the unknown value.

Final angular reesolution at motor side is **delta_m = reduction_ratio * angular_resolution_end**.

#### How many pulses per turn should be generated on every channel ? 

Taking into account the quadrature of the incremental encoder: **N = [ 2pi / (resolution * 4) ]**.

#### How many bits are needed by the digital encoder? 

**Nbits = [ log_2 (N) ]**.

####  Neglecting dissipative eﬀects, what should be the value of the motor inertia Jm in order to maximize the angular acceleration of the link for a given motor torque? With this choice, what is the maximum linear acceleration achievable by the tip of the link?

This depends on linl inertia and reduction ratios N as:

**Jm = Jl / (N^2)**

this means that if motor has maximum torque tm = 0.8 the max torque at link is tl = N * tm = sqrt(J/Jm) * tm.

Using these formulas in the balance of torques equation we can derive the maximum acceleration:

tl = Jl * thetal'' + N * Jm * thetam'' = knowing that thetam'' = N * thetal'' => (Jl + N^2 * Jm) * thetal'' = 2 * Jl * thetal''

Maximum acceleration is = link_lenght * thetal'' = link_length * tl / (2 * Jl)
