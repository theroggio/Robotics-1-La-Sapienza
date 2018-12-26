# Velocity profiles of joints

Find the minimum rest-to-rest motion between [ 1 , -0.5 ] and [ 0 , 0.2 ], given limits for velocity and acceleration of the two joints (v1 max 0.5, v2 max 0.8 | acc 1 max 0.8, acc 2 max 0.5).

First we compute the joint displacement as **d = [ -1 , 0.7 ]**.

The condition for having a time in which joint is a cruise velocity is Vi^2/Ai < abs(displacement).

We can see that this is true for the first joint, but not for the second: 1.28 < 0.7 !

For the first joint we can compute minimum time as T = ( displacement * acceleration + velocity^2 ) / (velocity * acceleration) = 2,625.

For second joint we do not arrive to cruise velocity, we have a triangular profile and the area should be equal to the displacement of 0.7.
So ther equation to solve is: 0.7 = base * h / 2 = Time * Vmax / 2 = Time * (Acceleration * Time / 2 ) / 2 = A * T^2 / 4 and find the time needed.

Minimum time is the time required for both joints to move (so the max between the two values). 

### Coordinated motion

To have a corrdinated motion the two times should be equal, so the faster one needs to slow down. 

This basically means solving the same equations for Acceleration considering that time should be same as T1 = 2,625. This changes the profile of the second joint speed, whose maximum value decreases.
