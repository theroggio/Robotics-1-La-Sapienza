## Advertisements: how to balance velocities and torque/moments

When asked to find a joint velocity corresponding to a certain cartesian velocity and angular body velocity the jacobian to consider is the one from

**r = [ pos_x ; pos_y ; angle (usually q1+q2+q3..) ]**



When asked to balance torque/momentum we use this same jacobian, but transpose. 

**torque = - transpose(J)  * [ forces ; momentum]**
