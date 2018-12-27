# Orientation of vectors after rotation

If is given a body and then it is rotated (final orientation is easily computed from rotation matrices) it can be difficult to understand old vectors position in the new frame.

1) If the rotatio is around that vector than it is immutate.

2) If we want to know the position of the unit-vector **x** after rotation we can do it applying all the rotation until that moment and taking the x column.

3) Position of tip of a link it's similar, depending on where it lied before the rotations and the 'braccio' of the rotation = link length.
