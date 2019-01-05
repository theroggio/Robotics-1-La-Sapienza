# Coordinated velocity

Coordination throught a motion can be imposed saying that [ position , angle_fi ] -> [ joint_derivated , angle_derivated ] = [ desired_speed , 0 ]

Where the angle_derivation = 0 is set in this way because we do not want the orientation to change, so it's derivative must be zero. While position obviously changes and we want to impose the velocity of the other robot (because slave robot should go coordinated with master robot).

Being this a differential kinematic problem we can use the analytical jacobian (so we derive position and angle_fi according to joint variables).

As always the desired velocity in cartesian space is J * velocity_cartesian; so if we invert the formula we obatin that velocity_joint = inv(J) * velocity_cartesian.

