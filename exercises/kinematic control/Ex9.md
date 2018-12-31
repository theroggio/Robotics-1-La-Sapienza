## Velocity control on 6R manipulator with wrist

To impose and compute velocity (linear and angular) of the manipulator we can write:

**[ v ; w ] = [ J11 , 0 ; J21 ; J22 ] * [ q'b ; q'w ]**

If the jacobian has full rank and it's invertible:

**[ q'b ; q'w ] = [ inv(J11) , 0 ; - inv(J22) * J21 * inv(J11) , inv(J22) ] * [ v ; w ]**

In presence of errors on both angular and linear velocity:

**q'b = inv(J11) * (vel_d + Kb * (pos_d - p))**

**q'w = - inv(J22) * J21 * q'b + inv(J22) * T * Kw * (angle_d - angle)**

Where **Kb** and **Kw** are two positive diagonal matrices. And **T** is the mapping between euler angles and angular velocity.

It's easy to acknowledge that the errors converge exponentially to zero.
