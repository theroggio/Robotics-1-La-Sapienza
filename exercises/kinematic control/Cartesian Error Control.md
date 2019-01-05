# Error in initial cartesian position

If we have an initial error in position in the cartesian space we should use a feedback control driven by the cartesian error. For example:

q' = inv(J) * [ desired(pos,angle) + K( desired(pos,angle) - current(pos,angle) )]

In this way the error goes exponentially to zero and it's decoupled for each joint. K is a diagonal positive matrix similar to the learning rate of gradient descent algorithm. 
