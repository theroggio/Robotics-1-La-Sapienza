# Exam 16, November 2018
## Exercise 1

The orientation of a body is given in terms of YXY Euler angles (α, β, γ) = ( π/2 , -π/4 , π/4). The orientation is the result of a rotation around the unit vector r = (1/sqrt(3), -1/sqrt(3), 1/sqrt(3)) by an angle of -30°.

Given these two way of expressing the orientation we can compute the rotation matrices:

1) R1= rotationmatrix('Y', π/2)*rotationmatrix('X',-π/4)*rotationmatrix('Y',π/4)
2) R2= rotationaxisangle( r ,-π/6)

The two matrices are different because one is wrt the reference frame, the other wrt the initial orientation. So their relative orientation is indeed the initial orientation of the body.

InitOrient = transpose(R2)*R1

The result is obviously uniquely defined! Given all the parameters there are no others interpretations. 

To express the solution as Roll-Pitch-Yaw matrix let's remember that this matrix is made up as  RPY = rotationmatrix('Z',angle3)*rotationmatrix('Y',angle2)*rotationamtrix('X',anlge1).
Because it is with fixed axis (so we use the multiplication on the contrary direction). Now we have the representation as (angle1, angle2, angle3) and its values with the InitOrient matrix.

We just need to solve the inverse problem: 

### step-by-step way 
From the matrices we understand which values to use in order to solve for angles with atan2 formula.
angle2 = atan2( -R31 , sqrt((R32)^2 + (R33)^2))
angle2' = atan2( -R31 ,-sqrt((R32)^2 + (R33)^2))

angle1 = atan2(R32,R33)
angle1' = atan2(-R32,-R33)

angle3 = atan2(R21,R11)
angle3' = atan2(-R21,R11)
