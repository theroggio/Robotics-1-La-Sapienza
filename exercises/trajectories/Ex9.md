## Circular trajectory for two points and with radius assigned

In general an arc length on a circle of radius R can be written as **ds = Rdtheta** so its parametrization is:

**p(s) = C + R * [cos(s/R + fi) ; sin(s/R + fi) ]**

with negative sign to go clockwise and fi is the phase associated with the point A of the trajectory.

The length of the arc can be computed without knowing C as **L = 2 * R * arcsin(d/2R)** where d is the euclidean distance between points.

### Numerical solution with data 

C = (-1,0)

Knowing the center we can infer the angle fi for point A (in this case is pi). So we have characterized the whole curve with s from 0 to L.

## Acceleration normal boundary

Analysing the norm properties we can decompose the norm of p'' in its tangent and normal part. 

norm(dp/ds) = 1   -> norm(p') = norm(s')  -> norm(p_t'') = norm(s'')

norm(dp^2/d^2t) = 1/R   ->  norm(p_n'') = s''^2 / R   ->  norm(p'') = sqrt( norm(p_n'')^2 +   norm(p_t'')^2 )

