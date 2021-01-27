# computer-graphics

Computer graphics from scrath.

1# Resume

##Points, Vectors and Normals

  1 - Points represents a position;
  2 - Vectors represents a direction;
  3 - Normals are perpendicular to the plane tangent a P(Point). 
  4 - All then can be represented by n-Vectors. 
  
Points and vectors can be transformed using linear transformations.
 
  1 - Translation for Points;
  2 - Rotation for Vector.
  
The length o the Vector can be set to 1, in which case we say that it is normalised.
 
2# Resume

##Coordinate Systems

Coordinates system (x, y and z).

3# Resume

##Math Operations on Points and Vectors

||V|| = sqrt(x * x + y * y + z * z) length, norm or magnitude (Is like h2 = c2 + c2, but 3d space)
|| indicates the length of vector

Normalized vectors

The mathematical notation is:

^V = V / ||V|| 

Normalized vector = vector / length of vector

Dot Product 

The dot product or scalar product requires two vectors A and B  and can be seen as the projection of one vector onto the other.

A.B = A.x * B.x + A.y * B.y + A.z * B.z (This is quite similar to the way we compute the length of a vector). The result of this operation relates to the cosine of the angle.

    B
    ^
C <-|=> A, D  For instance: A * B = 0 (vectors are perpendicular to each  other);  A * C = -1 (vectors are pointing in opposite directions); A * D = 1 (vector are pointing in the exact same direction).

Cross Product

The cross prodcuct is aldo an operation on two vectors, but to the difference of the dot product which returns a number, the cross product returns a perpendicular vector to the other two.

C = A X B

Cx = Ay * Bz - Az * By
Cy = Az * Bx - Ax * Bz
Cz = Ax * By - Ay * Bx


Vector/Point Addition and Subtraction

+ = x1 + x2, y1 + y2, z1 + z2
- = x1 - x2, y1 - y2, z1 - z2
* = x1 * x2, y1 * y2, z1 * z2

4# Resume

##Matrices

M = 1 2 3
    4 5 6
    
Example: 2 rows and 3 columns [2x3]

[3x3] and [4x4] matrices are most commons in CG.

<b>Make transformations</b>

If two matrices can be written as m x p and p x n they can be multiplied (row x column). Multiply row by column.
Matrices can be multiplied only if the matrix on the left side of the multiplication has a number of columns that is equal to the number of rows of the matric which is on the right. The order to multiply matrices matter.




  


