# Exercise 1. From a System to a Matrix

## Problem

Write the system

$$
\begin{cases}
2x-y+z=4, \\
x+3y-2z=1, \\
3x+y+z=7.
\end{cases}
$$

in the form $Ax=b$.
Identify the coefficient matrix, the vector of unknowns, and the right-hand side vector. Explain how each row of the matrix corresponds to one equation.

> **Why this exercise:** teaches how to move between a system of equations and matrix notation.

## Method

To write a linear system as a matrix equation, choose a fixed order for the unknowns. Here, we use $x,y,z$.

Each row of the coefficient matrix contains the coefficients from one equation in that order. The right-hand side vector contains the constants in the same equation order.

We write the vector of unknowns as $\mathbf{x}$ to distinguish it from the scalar variable $x$.

## Solution

### 1. Identify the coefficient matrix

The first equation is

$$
2x-y+z=4.
$$

Its coefficients, in the order $x,y,z$, are $2,-1,1$. These form the first row.

The second equation is

$$
x+3y-2z=1.
$$

Its coefficients are $1,3,-2$. These form the second row.

The third equation is

$$
3x+y+z=7.
$$

Its coefficients are $3,1,1$. These form the third row.

Therefore, the coefficient matrix is

$$
A=
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1
\end{pmatrix}.
$$

The columns correspond to $x$, $y$, and $z$, respectively.

### 2. Identify the two vectors

The vector of unknowns is

$$
\mathbf{x}=
\begin{pmatrix}
x \\
y \\
z
\end{pmatrix}.
$$

The right-hand side vector contains the constants from the three equations:

$$
b=
\begin{pmatrix}
4 \\
1 \\
7
\end{pmatrix}.
$$

### 3. Write the matrix equation

Combining these objects gives

$$
A\mathbf{x}=b,
$$

or explicitly,

$$
\begin{aligned}
\begin{pmatrix}
2 & -1 & 1 \\
1 & 3 & -2 \\
3 & 1 & 1
\end{pmatrix}
\begin{pmatrix}
x \\
y \\
z
\end{pmatrix}
&=
\begin{pmatrix}
4 \\
1 \\
7
\end{pmatrix}.
\end{aligned}
$$

Each row of $A$ is multiplied by the column vector of unknowns, producing the left-hand side of the corresponding equation.

## Verification

Expand the matrix-vector product:

$$
\begin{aligned}
A\mathbf{x}
&=
\begin{pmatrix}
2x+(-1)y+1z \\
1x+3y+(-2)z \\
3x+1y+1z
\end{pmatrix} \\
&=
\begin{pmatrix}
2x-y+z \\
x+3y-2z \\
3x+y+z
\end{pmatrix}.
\end{aligned}
$$

Equating this vector to $b$ gives

$$
\begin{cases}
2x-y+z=4, \\
x+3y-2z=1, \\
3x+y+z=7.
\end{cases}
$$

These are exactly the original equations, confirming that the matrix equation represents the given system.
