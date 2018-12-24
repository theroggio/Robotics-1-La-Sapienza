# Exam 16, November 2018
## Exercise 2

Is it possible to generate the following matrix with four Denavit-Hartenberg parameters? Provide the values or explain why not. 

M = [ -0.7071 ,  0.5  ,   -0.5  ,  -1   ;
      -0.7071 , -0.5  ,    0.5  ,  -1   ;
            0 ,0.7071 ,  0.7071 ,-0.7071;
            0 ,   0   ,    0    ,   1   ]
            
Let's consider the general matrix created by a DH frame:

M = [ cos(theta) ,  -cos(alpha)sen(theta)  ,   sen(alpha)sen(theta)  ,  a*cos(theta)   ;
      sen(theta) ,   cos(alpha)cos(theta)  ,  -sen(alpha)cos(theta)  ,  a*sen(theta)   ;
            0    ,        sen(alpha)       ,          cos(alpha)     ,       d         ;
            0    ,             0           ,             0           ,       1         ]
            
I'ts easy to see that:

**d** = -0.7071

**alpha** = atan2(M32,M33)

**theta** = atan2(M21,M11)

**a** = M14/cos(theta)
