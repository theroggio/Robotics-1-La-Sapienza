## Proof error convergence to zero

The proof is given by the Lyapunov function: **V = 1/2 * e * transpose(e) >= 0**.

**V' = transpose(e) * e' =  transpose(e) * (r_d' - r') = transpose(e) * (r_d' - J * q')**

Substituting q' from the control law we obtain ** -k * transpose(e) *J * transpose(J) * e <= 0**

As long as J is notsingular this assure the convergence of the error to zero.

This is true even for reduntant robots, the only thing to consider is that the jacobian wouldn't be a squared matrix so when required during the computation we cannot use the inverse but we must use the pseudo-inverse.
