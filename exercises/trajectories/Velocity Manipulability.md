# Velocity manipulability (ellipsoid and value)

the manipulability is **mu = det(J * transp(J))**

It's easy to see that near or in a singularity this value is zero, then it should be provided a computation of J describing the type of singularity and where does the robot lose motion.

When rank is 2 (instead of full rank 3) we just lose motion on 'one direction', if we have rank 1 then we do not have anymore an ellipsoid but a segment. 

