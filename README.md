# ECS-129
Knot or No Knot


### Pseudocode
for i = 1 -> sequence length - 2
  calc avg of 3 points (i , i + 1, i + 2)
  assign A = i, B = i + 1, C = avg (makes triangle in 3d space)
  
  for j = 1 -> i - 1 (to check sequence before i)
    set points E & F to xj and xj + 1 respectively
    check to see if the line segment from E -> F intersects the triangle in 3d space
    
  for j = i + 1 -> sequence length - 1
    set points E & F to xj and xj + 1 respectively
    check to see if the line segment from E -> F intersects the triangle in 3d space
    
  reassign A = i + 1, B = avg, C = i + 2 (make second triangle with avg in 3d space)
  
  for j = 1 -> i - 1 (to check sequence before i)
    set points E & F to xj and xj + 1 respectively
    check to see if the line segment from E -> F intersects the triangle in 3d space
    
  for j = i + 1 -> sequence length - 1
    set points E & F to xj and xj + 1 respectively
    check to see if the line segment from E -> F intersects the triangle in 3d space
