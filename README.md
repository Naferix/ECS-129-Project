# ECS-129 Knot or No Knot
Imagine a protein chain as a string, if we were to take both ends of the string and pull them so as to straighten out the string, would a knot form? Some proteins do happen to possess knots, and while it is unsure if the knot plays any major role in the function of the proteins, this project detects knots in a protein chain.


### Pseudocode for Protein Smoothing Algorithm in a 3D space
```python
Calculate distance between line generated between the points i & i+2 
flag = 0
numKnots = 0

While (distance between center and the line i,i+2 < threshold for ALL line segments)
  
for # of iterations

  check to see if min of array of stored distances < threshold and if so break out of for loop (50)

  for i = 1 -> sequence length - 2
    calc avg of 3 points (i , i + 1, i + 2)
    assign A = i, B = i + 1, C = avg (makes triangle in 3d space)

    for j = 1 -> i - 1 (to check sequence before i)
      set points E & F to xj and xj + 1 respectively
      check to see if the line segment from E -> F intersects the triangle in 3d space 
      inc numKnots if intersect

    for j = i + 1 -> sequence length - 1
      set points E & F to xj and xj + 1 respectively
      check to see if the line segment from E -> F intersects the triangle in 3d space
      inc numKnots if intersect

    reassign A = i + 1, B = avg, C = i + 2 (make second triangle with avg in 3d space)

    for j = 1 -> i - 1 (to check sequence before i)  
      set points E & F to xj and xj + 1 respectively
      check to see if the line segment from E -> F intersects the triangle in 3d space
      inc numKnots if intersect

    for j = i + 1 -> sequence length - 1
      set points E & F to xj and xj + 1 respectively
      check to see if the line segment from E -> F intersects the triangle in 3d space
      inc numKnots if intersect

     reassign i+1 -> avg of 3 coords
     stored avg of 3 coords to stored distance list
```
