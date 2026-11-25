# Exercise 6. Solving a System Using the Inverse

## Problem

Solve

$$
Ax=b,
$$

where

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 3
\end{pmatrix},
\qquad
b=
\begin{pmatrix}
5 \\
7
\end{pmatrix},
$$

using $x=A^{-1}b$. Then substitute the resulting vector back into the equation and check the result.

> **Why this exercise:** shows the connection between inverse matrices and solving a linear system.

## Method

If $A$ is invertible, we can multiply both sides of $Ax=b$ on the left by $A^{-1}$:

$$
A^{-1}Ax=A^{-1}b.
$$

Since $A^{-1}A=I$, this gives

$$
x=A^{-1}b.
$$

We first check that the determinant is nonzero, then find the inverse using the $2\times2$ formula. Finally, we multiply the inverse by $b$ and verify the solution in the original equation.

## Solution

### 1. Check that A is invertible

Calculate the determinant:

$$
\begin{aligned}
\det A
&=2\cdot3-1\cdot1\\
&=6-1\\
&=5.
\end{aligned}
$$

Since $\det A=5\ne0$, the inverse exists and the system has exactly one solution.

### 2. Find the inverse

For a $2\times2$ matrix, we interchange the diagonal entries, change the signs of the off-diagonal entries, and divide by the determinant.

Therefore,

$$
A^{-1}=
\frac15
\begin{pmatrix}
3 & -1 \\
-1 & 2
\end{pmatrix}.
$$

### 3. Multiply the inverse by b

Using $x=A^{-1}b$,

$$
x=
\frac15
\begin{pmatrix}
3 & -1 \\
-1 & 2
\end{pmatrix}
\begin{pmatrix}
5 \\
7
\end{pmatrix}.
$$

Each coordinate is obtained by multiplying a row of the inverse by the column vector:

$$
\begin{aligned}
x
&=\frac15
\begin{pmatrix}
3\cdot5+(-1)\cdot7 \\
(-1)\cdot5+2\cdot7
\end{pmatrix}\\
&=\frac15
\begin{pmatrix}
15-7 \\
-5+14
\end{pmatrix}\\
&=\frac15
\begin{pmatrix}
8 \\
9
\end{pmatrix}\\
&=
\begin{pmatrix}
\frac85 \\
\frac95
\end{pmatrix}.
\end{aligned}
$$

Thus, the unique solution is

$$
x_1=\frac85,
\qquad
x_2=\frac95.
$$

## Verification

Substitute the resulting vector into the original equation:

$$
Ax=
\begin{pmatrix}
2 & 1 \\
1 & 3
\end{pmatrix}
\begin{pmatrix}
\frac85 \\
\frac95
\end{pmatrix}.
$$

Calculating both coordinates gives

$$
\begin{aligned}
Ax
&=
\begin{pmatrix}
2\cdot\frac85+\frac95 \\
\frac85+3\cdot\frac95
\end{pmatrix}\\
&=
\begin{pmatrix}
\frac{16+9}{5} \\
\frac{8+27}{5}
\end{pmatrix}\\
&=
\begin{pmatrix}
5 \\
7
\end{pmatrix}\\
&=b.
\end{aligned}
$$

Both equations are satisfied, confirming that the vector found using $A^{-1}b$ is the solution.
