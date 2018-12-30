## Acceleration command control

- Solve the inverse kinematics for the current position **p**. We'll have one or more possible **q** configurations.

- For each configuration we can compute the jacobian **J(q)** and solve for the **q' = inv(J) * p'**.

- We can now compute the joint acceleration as **q'' = inv(J) * (acc_cart - deriv_J * q')**.

