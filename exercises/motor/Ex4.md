# Motor velocity given as RPM

If motor has maximum speed given in RPM, link driven has max velocity given by **v = reduction_factors * [RPM] * (2pi/60)**.

Reduction factors from gears, harmonic drives, etc are in this case **divided** because we're computing a link velocity that needs to be smaller than the motor velocity. 

The link length (ig is the case) is **multiplied** because the more it's the length the more a small rotation produces a large variation -> larger speed.
