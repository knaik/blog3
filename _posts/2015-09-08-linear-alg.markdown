---
layout: post
title:  "Linear Algebra Notes"
date:   2015-09-08 
categories: LinearAlgebra
---
#Day 2

1.1 no 71
Symmetric 

$$ A = A^T \quad a_{i,j} = a_{i,j}^T = a_{j,i} \quad a_{i,j} = a_{j,i} \quad \begin{bmatrix} a & b & c \\\ b & e & f \\\ c & f & i \end{bmatrix} $$

1.2 no 37

\\( u = \begin{bmatrix} 3 \\\ 8 \end{bmatrix} , \quad S = \left\lbrace \begin{bmatrix} 1 \\\ 2 \end{bmatrix} \begin{bmatrix} 2 \\\ 3 \end{bmatrix} \begin{bmatrix} -2 \\\ 5 \end{bmatrix} \right\rbrace \quad \quad
c_1 \begin{bmatrix} 1 \\\ 2 \end{bmatrix} + c_2 \begin{bmatrix} 2 \\\ 3 \end{bmatrix} + c_3 \begin{bmatrix} -2 \\\ 5 \end{bmatrix} \quad \quad \begin{bmatrix} c_1 + 2c_2 - 2c_3 \\\ 2 c_1 + 3c_2 + 5c_3 \end{bmatrix} \quad \begin{bmatrix} 3 \\\ 8 \end{bmatrix} \\)

System of linear equations:

\\(  a_1x_1+a_2x_2+\cdots +a_nx_n = k \\\
     a_1,\, a_2,\ \dots,\ a_n\; and \; k \; are \; real \; numbers \\\
 x_1,\, x_2,\ \dots,\ x_n \; are \; the \; variables \\)
 

 An equation is non-lin if any var is raised to a power, multiplied together or involve other functions
 
System eq

$$	a_{11} x_1 +  a_{12} x_2 + \cdots a_{1n} x_n =  b_1 \\\
	a_{21} x_1 +  a_{22} x_2 + \cdots a_{2n} x_n =  b_2 \\\
	\vdots  \quad \quad \quad \quad \quad  \vdots\\\
	 a_{m1} x_1 +  a_{m2} x_2 + \cdots a_{mn} x_n =  b_n \\\
 x_1 \begin{bmatrix} a_{11} \\\ \vdots \end{bmatrix} +  x_2 \begin{bmatrix} a_21 \\\ \vdots \end{bmatrix} +  x_3 \begin{bmatrix} a_31 \\\ \vdots  \end{bmatrix}   = \begin{bmatrix} b \\\ \vdots  \end{bmatrix} \\
A =  \begin{bmatrix} a_11 \end{bmatrix} , x = \begin{bmatrix} x_1 \\\ x_2 \\\ \vdots \end{bmatrix} ,  b = \begin{bmatrix} b \\\ \vdots \end{bmatrix} \\\
Ax = b $$

`x + y +z = 1`

`x -4y -z = 7`

`0 + y + 2z = 0`

\\( \begin{bmatrix} 1 &  1  & 1 \\\ 1 & -4 & -1 \\\ 0 & 1 & 2 \end{bmatrix}  \begin{bmatrix} x \\\ y \\\ z \end{bmatrix}  = \begin{bmatrix} 1 \\\ 7 \\\ 0 \end{bmatrix} \\)

Three operations that do not change a system of equations:

* Interchange two equations \\( A  \xrightarrow{ r_i \leftrightarrow r_j}  B \\)
* Multiply an equation by a non-zero scaler \\(	A \xrightarrow{r_i \rightarrow cr_i}  B \\)
* Multiply an equation by a scaler and add to another equation 	\\( A \xrightarrow{r_i \rightarrow cr_j + r_i} B \\)

Interchange two equations
\\( \begin{bmatrix} 2&-3&4&1\\\	-1&2&-1&-2\\\	2&3&1&-2	\end{bmatrix}	\xrightarrow{r_1 \leftrightarrow r_2}	\begin{bmatrix}	-1&2&-1&-2\\\ 	2&-3&4&1\\\ 	2&3&1&-2 	\end{bmatrix} \\)
	
Multiply an equation by a non-zero scaler
\\(	\begin{bmatrix}	-1&2&-1&-2\\\  2&-3&4&1\\\ 2&3&1&-2 	\end{bmatrix}  \xrightarrow{r_2 \rightarrow 2r_1 + r_2} \begin{bmatrix} -1&2&-1&-2\\\ 	0&1&2&-3\\\ 	2&3&1&-2 \end{bmatrix} \\)
	
Multiply an equation by a scaler and add to another equation
\\(	\begin{bmatrix}
	-1&2&-1&-2\\\
	%
	0&1&2&-3\\\
	%
	2&3&1&-2
	\end{bmatrix}
	%
	\xrightarrow{\begin{subarray}{l} r_3 \rightarrow 2r_1 + r_3, \\ r_1 \rightarrow -1r_1 \end{subarray}}
	%
	\begin{bmatrix}
	1&-2&1&2\\\
	%
	0&1&2&-3\\\
	%
	0&7&-1&-6
	\end{bmatrix}
	\\)

---------------------------
Special form of Matrices, goal is to use row ops to get to one of the special forms

The Row-Echelon Form:

 - The zero rows are in the bottom of the matrix
 - Each *leading entry* is in a column to the right of the leading entry in the previous row
 - The entries under leading entries are equal to zero * not real condition, just an implication

 $$ 	\begin{bmatrix} 2&-3&4&1 \\\ 0&0&-1&-2\\\ 0&0&0&0 \end{bmatrix} \quad and \quad \begin{bmatrix}  0&2&-1&-2 \\\ 0&0&4&1\\\ 0&0&0&5	\end{bmatrix}	$$

 Non-examples:
 
 $$	\begin{bmatrix} 	2&-3&4\\\ 0&0&0\\\ 0&0&1 	\end{bmatrix} \quad and \quad	\begin{bmatrix} 2&-3&4 \\\ 0&0&5 \\\ 0&0&1	\end{bmatrix} $$
	
Reduced Row Echelon form:

- All conditions of Row-Echelon form
- All leading entries are one (multiply with coefficient --> row operations to make this true)
- Entries above AND below leading entries are all zero
	-identity matrix in reduced row echelon

\\(	\begin{bmatrix} 1&-3&0&1 \\\ 0&0&1&-2\\\  0&0&0&0 	\end{bmatrix} \quad  \begin{bmatrix}	0&1&0&0\\\	0&0&1&0\\\	0&0&0&1	\end{bmatrix} \\\
	Non\; examples \quad \begin{bmatrix}  1&0&4\\\	0&1&0\\\	0&0&2 	\end{bmatrix} \quad \begin{bmatrix} 1&0&0\\\	0&0&1\\\	0&0&1	\end{bmatrix} \\)

augmented matrix 

`x + y +z = 1`
`x -4y -z = 7`
`0 + y + 2z = 0`
\\( \begin{bmatrix} 1 & 1 & 1 & | 1 \\\ 1 & -4 & | -1 \\\ 0 & 1 & 2 & \0 \end{bmatrix} \quad 	\xrightarrow{{row operations}} 	\begin{bmatrix}	1&0&0& \frac{7}{4}\\\	0&1&0 & \frac{-3}{2}\\\	0&0&1 & \frac{3}{4} \end{bmatrix} \\\ 
x_1 = \frac{7}{4}, \quad x_2= -\frac{3}{2}, \quad x_3 = \frac{3}{4} \\)

\\( x = \begin{bmatrix} 2 \\\ 1 - 2x_3 \\\ x_3 \end{bmatrix} = \begin{bmatrix} 2 \\\ 1 \\\ 0 \end{bmatrix} + \begin{bmatrix} 0 \\\ -2x_3 \\\ x_3 \end{bmatrix} \\\
= \begin{bmatrix} 2\\\ 1 \\\ 0 \end{bmatrix} + x_3 \begin{bmatrix} 0 \\\ -2 \\\ 1 \end{bmatrix} \\)

example b
soln 
	x3= 0, x2 = x2, x1 = 5 - 2x2

\\( x = \begin{bmatrix} 5 - 2x_2 \\\ x_2 \\\ 0 \end{bmatrix} = \begin{bmatrix} 5 \\\ 0 \\\ 0 \end{bmatrix} + \begin{bmatrix} -2x2 x2 0...... \\)

example c
no solution because
last row gives self contradictory solution `0 = 4 `
