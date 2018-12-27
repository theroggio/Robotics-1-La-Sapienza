# Cylindrical coordinates

Given a position in the cartesian space **p**, the same position in cylindrical coordinates has three parameters: azimuth, elevation and distance.

In the case of a generic position for the end effector its cylindrical coordinates depend on its structure. 

If **p = [ q3 * c1 ; q3 * s1 ; q2 + d ]** the cylindric coordinates are:

azimuth = angle between reference and O-Pproj line = q3

elevation = effective height = p(z) = q2 + d

distance = euclidean distance from z-axis to p = sqrt(px^2 + py^2)
