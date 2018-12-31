## Workspace of RPR planar robot (second link as angle of pi/2 fixed)

1) l1 >= l3

Workspace has inner and outer circular boundary. **Rin = l1 - l3** and **Rout = sqrt(l1^2 + D^2) + l3^2** where D is the length of prismatic joint 2.

2) l1 < l3

Has **Rin = l3 - sqrt(l1^2 + D^2)**, if this value is 0 mans we have no holes inside the workspace.
