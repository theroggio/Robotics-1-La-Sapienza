## Alternative representations of rotation matrices time derivative

A rotation matrix always (for every t) holds R * transpose(R) = I

If we derive as R = R(t) we find: R' * transpose(R) + R * transpose(R') = 0.

Putting S(t) = R' * transpose(R) we obtain S + transpose(S) = 0.

If we consider a constant vectr pc and a p(t) = R(t) * pc we can see that p'(t) = R'(t) * pc.

That we can rewrite as p'(t) = S(t) * R(t) * pc.

From mechanics we also know that given an angular speed w of the body p'(t) = w(t) **x** R(t) * pc.

Basically it's proven that S(t) describes the dot product between w and R(t) * pc. S(t) -> S(w(t)).

This justify the first possibility: **R' = S(w) * R**

Similarly if we consider the identity on the other side as transpose(R) * R = I we have a similar procedure ending up in transpose(R) * R' = S(omega). From which **R' = R * S(omega)**.


