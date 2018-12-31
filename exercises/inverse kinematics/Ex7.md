## Inverse kinematics for RPR planar robot

Given a specific as **r = ( px , py , angle )**  and the direct kinematics is possible that the third row -> angle = f(q) plugged in px and py can help in solvgin the inverse problem.

### Example:

f(q) = [ l1 * c1 - q2 * s1 - l3 * c12p/2 ; l1 * s1 + q2 * c1 + l3 * s13p/2 ; q1 + q3 + pi/2 ]

*Here c123p/2 means cos(q1 + q3 +pi/2)*

This means that when assigned a desired position and orientation we know the value angle = q1 + q3 + pi/2 and we can substitute it inside the other expression. 

Doing so we can solve for q2 (as in other planar problems where orientation didn't count). Then for q1 using px and py with right sum / multiplications. 

At the end we can use q2 and q1 to compute q3 = angle - q1 - pi/2.

