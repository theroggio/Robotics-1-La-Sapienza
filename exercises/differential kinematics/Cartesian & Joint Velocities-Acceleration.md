# General Differential problem

## Treated for circular trajectory of exercise <a href='https://github.com/theroggio/Robotics-1-La-Sapienza/blob/master/exercises/trajectories/Ex1.md'> Ex1 </a>

### Cartesian velocity and acceleration in point P2

Being P2 the other extreme of the diameter, to be there we need t = T/2, so that s(t) = pi. We differentiate the parametric path twice (once for velocity, another time for acceleration).

p'(s) = R * [ -sin(s + theta) ; cos(s + theta) ] 

p''(s) = R * [ -cos(s + theta) ; -sin(s + theta) ]

We need to compute also s' and s'' because the derivation on time is composed by the parametrization with s (in fact we derived p(s) not p(t)!).

s'(t) = (12pi/T) * [ (t/T) - (t/T)^2 ]

s''(t) = (12pi/T^2) * [ 1 - (2t/T) ]

Now we can compute effectively velocity and acceleration at P2.

p'(t) = p'(s) * s'(t) = we want it at P2 so p'(T/2) = p'(pi) * s'(T/2) = R * [ sin(theta) ; - cos(theta) ] * (3pi/T)

We could replace R with its formula to have **(x1 - x2)/2** and **(y1 - y2)/2** instead of cos(theta) and sin(theta).

Similarly the acceleration can be found as p''(t) = p''(s) * s'(t)^2 + p'(s) * s''(t)

### Associated joint velocity and acceleration 

First of all we need to move to joint space finding the equations of end-effector in joint variables. From the picture is easy to see that **f(q)** = [ q2 * cos(q1) ; q2 * sin(q1) ].

At time t = pi (when we're at P2) we know that that q1 (the angle) must be the angle of P2 so atan2( y2, x2). Q2 must be the distance toward P2 that can be computed from its coordinates as sqrt(x2^2 + y2^2). 

The **velocity** can be computed as q'(t) = inv(J(q(t))) * p'(t) -> knowing p'(t) from previous part we just need to compute the inverse at q(T/2), that is known from last part. The Jacobian is easy to find once we have f(q).

The **acceleration** is q''(t) = inv(J(q(t))) * [ p''(t) - J'(q(t)) * q'(t) ].

Pay attention that J' is the time derivative of the jacobian (with respect to time! so every joint variable is a time variable!). 
