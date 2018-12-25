# Circular trajectory of planar robot

## Specifics:

- Starting and ending point is P1, start and end velocity is zero

- Passing per P2

- Tangent at P2 has to be orthogonal to the segment P1-P2

- Timing law along Cartesian path should be a minimal polynomial

## Solution

The generic formula for a circle in the plane (considering its center as (0,0)) is **(x-x0)^2 + (y-y0)^2 = R^2**.

Imposing its passing for P1 and P2 we obtain two equations (that needs to be equal because they need to be on the same circle, with the same radius).
The third condition is the one that gives us the unique solution: the requirement of orthogonality means that the tangent should pass through the center of the circle.

