## TRajectory of rotation between Ri and Rf

Given initial and final oritentation as rotation matrices (remember if we have angles of euler expressing the rotation w can find it easily) we can represent them in any way we want (even as axis - angle mode).

We can compute the relative orientation between final and initial orientation as R1' * R2 (expressed in firs frame coordinates). This is the 'motion' we have to perform.

Representing this as axis-angle we can define a cubic polynomial trajectory as **theta(t) = theta_f * (3 * tau^2 - 2 * tau^3)**

where theta_init is 0 because is the initial orientation and it's our reference frame. We can also compute velocity and see that this is a rest-to-resto motion.

To compute the norm of the angular velocity in the frame we can use **w = axis * angle'**.

To compute it in a reference absolute frame, external from all the computation, we must have a Ra0 so that **wa = Ra0 * axis *angle'**.

