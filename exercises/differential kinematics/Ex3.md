# Jacobian build and null space

The simple jacobian used to compute the linear velocity of the end effector is the one related just to the differentiation of the position (analytic jacobian, not the geometrical one).

We just need to derive the position f(q) along all the q joint variables (so it produces a matrix 3-by-m, m = number of joints variables).

The jacobian matrix could be singular ( det(J) = 0 ), solving this equations we obtain a certain amount of values (for set of joint variables) for which the robot is in a singular configuration.

Computing the jacobian at these singularities we can inspect their null spaces.

## Example

f(q) = [ Ac1 + Dc12 ; As1 + Ds12 ]

J(q) = [ -(As1 + Ds12)  ,   -Ds12  ;   Ac1 + Dc12  , Dc12  ]

### Singularities 

det(J) = ADs2

q2 = { 0 , pi }

### Null Spaces

J(q2 = 0) = [ -(A+D)s1  , -Ds1  ; (A+D)c1  , Dc1  ]

Null space: solving for the vector v such that J * v = 0 we obtain a possible **v = [ -D ; A+D ]**. Matlab has a function. Geometrically is possible to do it by reduction to triangular matrix (last column is the vector span).

Range space: it's a basis for the jacobian, if the null space has dimension 1, the range space must have dimension one! In this case the easiest way is to choose [ -s1 ; c1 ].


J(q2 = pi) = [ (D-A)s1 , Ds1 ; (A-D)c1 , -Dc1 ].

Null space: one possibility is [ D ; A-D ].

Range space: [ -s1 ; c1 ].

