# Balanced Wrenches

Given the configuration qa find all possible wrench vectors whose appliesd to the configuration would be balanced without control: remains in static equilibrium without balancing equilibrium.

First we need to compute the jacobian J(qa) and its transpose tJ(qa). 

tJ(qa) = [  0  1  0  0  0  1  ,
            1  0  1  0 -1  0  ,
            1  0  0  0  0  0  ,
            1  0  0  0 -1  0  ,
            0  0 -1  0  0  0  ]
            
The wrenches that do not perturbe the equilibrium are the ones belonmging to the null space of the matrix, in this case **u1 = ( 0 1 0 0 0 -1)** and **u2 = ( 0 0 0 1 0 0 )**
