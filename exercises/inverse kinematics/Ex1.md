# Exam 16 November 2018
## Exercise 5

Given the position of the end effector as a combination of joint variables (if you have DH frames you can compute it as the multiplication from base from to end frame and take just the three displacement components, in this case we take two because it's a planar robot so third component is always 0).

We obtain:

a1*cos(q1) - q2*sin(q1) = -2

a1*sin(q1) + q2*cos(q1) = -3

### Q2

x^2 + y^2 = (-2)^2 + (-3)^2

a1^2 + q2^2 = 13

q2 = +- sqrt(13 - a1^2)

### Q1

From before we obtain two results (unless q2 = 0 then we're in a singular case); so we should obtain two distinct solutions for q1.

q1 = atan2( a1*y - q2*x , a1*x + q2*y)

We can see that in this way we obtain (a1^2 + q2^2) multiplying the sin and cos, but being the same values we can just ignore them. Using first the positive and then the negative value of q2 we obtain the solutions.

