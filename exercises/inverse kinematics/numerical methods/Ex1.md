# Exam 16 November 2018
## Exercise 5

The desired position of the origin of the last frame in the plane is **p** = (-2 -3). At some iteration the algorithm drive the robot from **q** = (-1 2) to **q2** = (-2.7742 -0.6519).

### What's the method used ? Explain why and the parameters used. 

First of all we need formulas relating the end-effector position to the joint variables. If DH is given, we can compute the final homogeneous transformation matrix and take the last column as displacement vector (just first three components, or 2 if planar problem).

Using these formulas and the correct informations about desired position the script **newthon raphson method** derives the following guess, it is different from **q1** so Newthon Raphson is not the method used.

We deduced is been used the Gradient Descent method, it's formula is very similar but uses an adaptive parameter alpha we need to find. 
The generic iteration is q = q_old + alpha * j^T * (desired - q_old). In this case q should be **q2**, q_old is our guess **q**, j^T is the jacobian of the displacement (found using DH tables), desired is **p**.

Replacing the values we found that **alpha** (learning rate) should be 0.5. 

