## Expression of rest-to-rest motion

p(s) = p_i + s * (P_f - P_i)

s(t) = 10 * (t/T)^3 - 15 * (t/T)^4 + 6 * (t/T)^5

## General control of velocity

q' = pinv(J) * (pd' + K * e)  where e = pd - p , K > 0 diagonal

## Control of velocity depending on normal and tangent direction

q' = pinv(J) * (pd' + R0t * K * transp(R0t) * e)   where R is matrix of rotation in the tangent/normal plane and K is a diagonal matrix kt , kn

To build R we have to evaluate **xt = (P_f - P_i) / norm(P_f - P_i) = ( alpha ; beta )** and then **R = [ alpha, -beta ; beta, alpha]**

## Error decreasing exponentially

e' = Rt0 * (pd' - p') = Rt0 * (pd' - J * q') = Rt0 * (pd' - J * (pinv(J) * (pd' + R0t * K * transp(R0t) * e))

= Rt0 * pd' - Rt0 * J * pinv(J) * pd' - Rt0 * J * pinv(J) * R0t * K * transp(R0t) * e

= Rt0 * pd' - Rt0 * pd' - Rt0 * R0t * K * transp(R0t) * e

= - K * transp(R0t) * e 

= - K * et

This means error decrease exponentially along the et vector (error along tangent and normal, because is R0t * e).

Evaluating the norm of the error we can find:

norm(e0(t)) = norm(et(t)) = sqrt( en^2 + et^2 ) = e^(-kt) * sqrt(en(0)^2 + et(0)^2) = e^(-kt) * norm(et(0))

This is a good way to impose specifics on rapidiuty of error recovering. 

## Control from a configuration q0

From previous control law we know that the velocity to be required is:

q' = pinv(J) * (pd' + R0t * K * transp(R0t) * e)
