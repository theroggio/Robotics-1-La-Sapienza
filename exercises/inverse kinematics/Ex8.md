## Inverse kinematics for angles alpha - beta of rotation identifying vector n as axis Z of a new frame

Generic formula:

**R(alpha, beta) * [ nx ; ny ; nz ] = [ 0 ; 0 ; 1]**

In this example the rotations were about y and x current axes.

[ c(a)  ,  s(a) * s(b)  ,  s(a) * c(b)  ; 0  ,  c(b)  ,  -s(b)  ;  -s(a)  ,  c(a) * s(b)  ,  c(a) * c(b) ] * [nx ; ny ; nz] = [ 0 ; 0 ; 1 ]

[ c(a) * nx + s(a) * s(b) * ny + s(a) * c(b) * nz ; c(b) * ny - s(b) * nz ; - s(a) * nx + c(a) * s(b) * ny + c(a) * c(b) * nz ] = [ 0 ; 0 ; 1 ]


- First we square and sum first and third row and obtain **ny * s(b) + nz * c(b) = +- sqrt(1 - nx^2)**.

  This with the second row allow us to define beta.
  
- Having expression for s(b) and c(b) we can substitute them in first and third row and obtain a 2-eq linear system for alpha.
