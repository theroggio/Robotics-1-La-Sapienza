# Geometric Jacobian and its inspection

From DH table we can derive both end-effector position and rotation matrices of all frames wrt base frame. 

First from the homogeneous trasnformation matrix to the end-effector we take the position of e-e. Derivating for all joint variablkes we compute the analytical jacobian (first three rows).

For the angular part, every joint here is rotational so they all have angular part expressed as (z0 , R1z , R1R2z , ... ) and so on.

### When linear jacobian loses rank?

Inspecting the linear jacobian can be particulary hard to tell when it loses rank. Some expedients that cna be ued is shifting frame (pre multiplying fro the transpose of R1) or multiplying (post) for a constant to transform the matrix in a more easy one. 

THen obsviously if there are similar rows we can inspect which values of joint variables make them equals, or if a row has just one value different from zero (if it's all null the matrix loses rank).

### What angular velocities can be generated?

This regards only the angular part of the jacobian. Basically we're looking for the vectors spanning the range space (linear independent vector of the matrix). 

### Jacobian singularities

Stacking the two matrices one above the other (as it should be to express both angular and linear joint velocities) we can check its rank and its singular configurations. 

We already have a singular configuration for linear velocities, doing the needed reductions we can see that the angular velocities does not help recovering the singularity (matrix has rank 4 < 6).

## Joint velocities which results in a zero-linear body velocity

After having the configuration of the robot we can plug this info inside the linear jacobian, then computing the null space. Every scaling vector of the null space which is not all-zero, is a joint velocity which results in a zero linear velocity of the body.

