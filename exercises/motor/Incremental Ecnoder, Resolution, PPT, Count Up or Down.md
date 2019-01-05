# Exam 16 November 2018
## Exercise 4

### If an incremental encoder with quadrature detection is used on the motor side, how many bits should its internal computer use to obtain a resolution of 10^-3 deg on the link side?

Given link resolution we need an output resolution of **r** = n * e = 128 * 10^-3 deg.

Thus the internal computer should be able to count a number of pulses per turn equal to **N** = [360/r] = 2813.

This requires a minimum number of bits **Nb** = [log_2(N)] = 12.

### How many pulses per turn should the optical disk have? 

It has quadrature detection so it needs **pulses** = [N/4] = [2813/4] = 704.

### How many pulses would be counted in total in one second when the motor is at steady state with speed w?

Then **count** = [w * N/(2*pi)] = [402.1239 rad/s * 2813/6.14] = 180032.

### The counter is going up or down?

The counter is going **down** because the speed is negative (w < 0), this is due to the wm speed and the output speed being in opposite direction because of the harmonic drive.
