# Inverse kinematics spacial robot

### First step

Usually one of the angles can be derived from X^2 + Y^2 + (Z - d)^2.

### Second step

It's common to have now some sine or cosine who show up with similar multiplications, like c1 * stuff = x and s1 * stuff = y; then we can compute q1 as atan2(y,x) and atan2(-y,-x) because we could divide for stuff that usually is what remains from x^2 + y^2.

### Third step

Find a way to isolate cosine and sine of the last joint. Build a system in two equations from the initial three.
Obviously this means we'll have up to four solutions.

From desired position we can restrict to solutions of interest, but generally we have joint_1(+|-), from which joint_2(+|-) and so for joint_3(++|+-|-+|--).
