# Robot required joint velocity when detected human

Specifics ask to check distance of the human: d < D1 stop | D1 < d < D2 it can retract with velocity inversely proportional to d, along horizontal and centripetal || 
repulsed with v inversely proportional to distance from ee along horizontal direction | d > D2 nothing happens.

First we need a vector expressing the position of the human (as x_human, y_human), its norm specifies the distance from origin of robot (not from end effector!).

So if **norm(d) < D1** velocity should be **0** because the robot must stop. 

If **norm(d) > D2** velocity should be the one required for the **task**, nothing changes.

If we're in the between section the joint velocity is inv(J)*v where v can be one of the following:

1) v = - ee / (norm(ee) * norm(d) )

2) v = (ee - d) / norm(ee - d)
