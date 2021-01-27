# computer-graphics

Computer graphics from scrath.

<h2>1 Points, Vectors and Normals</h2>

  1 - Points represents a position;
  2 - Vectors represents a direction;
  3 - Normals are perpendicular to the plane tangent a P(Point). 
  4 - All then can be represented by n-Vectors. 
  
Points and vectors can be transformed using linear transformations.
 
  1 - Translation for Points;
  2 - Rotation for Vector.
  
The length o the Vector can be set to 1, in which case we say that it is normalised.

<h2>2 Coordinate Systems</h2>

Coordinates system (x, y and z).

<h2>3 Math Operations on Points and Vectors</h2>

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

<code>
+ = x1 + x2, y1 + y2, z1 + z2
- = x1 - x2, y1 - y2, z1 - z2
* = x1 * x2, y1 * y2, z1 * z2
</code>  


<h2>4 Matrices</h2>

M = 1 2 3
    4 5 6
    
Example: 2 rows and 3 columns [2x3]

[3x3] and [4x4] matrices are most commons in CG.

<b>Make transformations</b>

If two matrices can be written as m x p and p x n they can be multiplied (row x column). Multiply row by column.
Matrices can be multiplied only if the matrix on the left side of the multiplication has a number of columns that is equal to the number of rows of the matric which is on the right. The order to multiply matrices matter.

m x p matrix multiplied by a p x n matrix, gives a m x n matrix.

<h2>5 How Does Matrix Work: Part 1</h2>

<b>conventions:</b> Different author/programs use different conventions!

<b>POint-Matrix Multiplication</b>

P = [x y x]

[x y x ] *  c00 c01 c02 c03
            c10 c11 c12 c13
            c20 c21 c22 c23
            
Xtransformed = x * c00 + x * c10 + z * c20           
Ytransformed = x * c01 + x * c11 + z * c21
Ztransformed = x * c02 + x * c12 + z * c22

<b>The Identity Matrix</b>

The identity matrix or unit matrix is a square matrix whose coefficients are all 0 excepted the coefficients along the diagonal which are set to 1:

1 0 0
0 1 0
0 0 1

The result of P multiplied by the identity matrix is P.

<b>The Scaling Matrix</b>

Sx 0 0
0 Sy 0
0 0 Sz

XScaling = x * Sx + x * c10 + z * c20           
YScaling = x * c01 + x * Sy + z * c21
ZScaling = x * c02 + x * c12 + z * Sz

<b>The Rotation Matrix</b>

Rotaton 90º P = (1, 0, 0) to Pt = (0, 1, 0) 

RotationZ = 0 1 0
            1 0 0
            0 0 1  


<b>This don't work in clockwise</b>

Rz(a) = cos(a) sin(a) 0   0 1 0
        sin(a) cos(a) 0 = 1 0 0
        0      0      1   0 0 1 
        
<b>This work in clockwise</b>

Rz(a) = cos(a)  sin(a) 0
        -sin(a) cos(a) 0
        0       0      1
        
        


