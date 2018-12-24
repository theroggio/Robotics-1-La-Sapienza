# Exam 16, November 2018
## Exercise 2

Is it possible to generate the following matrix with four Denavit-Hartenberg parameters? Provide the values or explain why not. 

M = [ -0.7071 ,  0.5  ,   -0.5  ,  -1   ;
      -0.7071 , -0.5  ,    0.5  ,  -1   ;
            0 ,0.7071 ,  0.7071 ,-0.7071;
            0 ,   0   ,    0    ,   1   ]
            
The determinant of it's 3x3 first minor is +1, so it is a rotation matrix. Let's consider the general matrix created by a DH frame:

M = [ cos(theta) ,  -cos(alpha)sen(theta)  ,   sen(alpha)sen(theta)  ,  a*cos(theta)   ;
      sen(theta) ,   cos(alpha)cos(theta)  ,  -sen(alpha)cos(theta)  ,  a*sen(theta)   ;
            0    ,        sen(alpha)       ,          cos(alpha)     ,       d         ;
            0    ,             0           ,             0           ,       1         ]
            
I'ts easy to see that:

**d** = -0.7071

**alpha** = atan2(M32,M33)

**theta** = atan2(M21,M11)

**a** = M14/cos(theta)

Obviously if using one of these equations we'd observe an inconsistency then it was not an homogeneous transformation matrix.
