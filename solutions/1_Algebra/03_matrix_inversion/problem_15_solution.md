# Exercise 15. Two Methods for Solving the Same System

## Problem

For

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 3
\end{pmatrix},\qquad b=
\begin{pmatrix}
7 \\
8
\end{pmatrix}
$$

solve $Ax=b$ in two ways:

1. using $A^{-1}b$,
2. using Gaussian elimination.

Compare both solutions, the number of essential steps, and state which method was simpler in this example.

> **Why this exercise:** compares two known methods and prepares the student to choose a solution method consciously.

## Method

The inverse method finds $A^{-1}$ and then computes $x=A^{-1}b$.

Gaussian elimination works directly with the augmented matrix $[A\mid b]$. We eliminate the entry below the first pivot and then use back substitution.

Both methods solve the same system:

$$
\begin{aligned}
2x_1+x_2&=7, \\
x_1+3x_2&=8.
\end{aligned}
$$

## Solution

### 1. Solve using the inverse

First, calculate the determinant:

$$
\det A=2\cdot3-1\cdot1=5.
$$

Since the determinant is nonzero, the inverse exists and the system has exactly one solution.

The inverse formula gives

$$
A^{-1}=
\frac15
\begin{pmatrix}
3 & -1 \\
-1 & 2
\end{pmatrix}.
$$

Now multiply by $b$:

$$
\begin{aligned}
x
&=A^{-1}b \\
&=\frac15
\begin{pmatrix}
3 & -1 \\
-1 & 2
\end{pmatrix}
\begin{pmatrix}
7 \\
8
\end{pmatrix} \\
&=\frac15
\begin{pmatrix}
3\cdot7-8 \\
-7+2\cdot8
\end{pmatrix} \\
&=\frac15
\begin{pmatrix}
13 \\
9
\end{pmatrix} \\
&=
\begin{pmatrix}
\frac{13}{5} \\
\frac95
\end{pmatrix}.
\end{aligned}
$$

### 2. Solve using Gaussian elimination

Start with the augmented matrix:

$$
[A\mid b]=
\left[
\begin{array}{cc|c}
2 & 1 & 7 \\
1 & 3 & 8
\end{array}
\right].
$$

Eliminate the first entry of the second row:

$$
R_2\leftarrow R_2-\frac12 R_1.
$$

The new second row is

$$
\begin{aligned}
&\left(
1-\frac12\cdot2,\;
3-\frac12\cdot1,\;
8-\frac12\cdot7
\right) \\
&\qquad=\left(
0,\;\frac52,\;\frac92
\right).
\end{aligned}
$$

Thus, the augmented matrix becomes

$$
\left[
\begin{array}{cc|c}
2 & 1 & 7 \\
0 & \frac52 & \frac92
\end{array}
\right].
$$

The second equation gives

$$
\frac52 x_2=\frac92,
\qquad
x_2=\frac95.
$$

Substitute this value into the first equation:

$$
\begin{aligned}
2x_1+\frac95&=7, \\
2x_1&=\frac{35}{5}-\frac95=\frac{26}{5}, \\
x_1&=\frac{13}{5}.
\end{aligned}
$$

Therefore,

$$
x=
\begin{pmatrix}
\frac{13}{5} \\
\frac95
\end{pmatrix}.
$$

### 3. Compare the two methods

Both methods give the same solution:

$$
x_1=\frac{13}{5},
\qquad
x_2=\frac95.
$$

Counting the main stages rather than individual arithmetic operations:

| Method | Essential stages |
| --- | --- |
| Inverse method | Three: calculate the determinant, construct the inverse, and multiply by $b$. |
| Gaussian elimination | Three: perform one elimination step, solve for $x_2$, and substitute back to find $x_1$. |

Although both have three main stages under this counting, the stages require different amounts of work.

Gaussian elimination was simpler for this example because one row operation immediately produced an equation containing only $x_2$. It avoided calculating all four entries of an inverse matrix.

The inverse method is still straightforward here, and an already known inverse could be reused for other right-hand sides.

## Verification

Substitute the solution into the original matrix equation:

$$
\begin{aligned}
Ax
&=
\begin{pmatrix}
2 & 1 \\
1 & 3
\end{pmatrix}
\begin{pmatrix}
\frac{13}{5} \\
\frac95
\end{pmatrix} \\
&=
\begin{pmatrix}
2\cdot\frac{13}{5}+\frac95 \\
\frac{13}{5}+3\cdot\frac95
\end{pmatrix} \\
&=
\begin{pmatrix}
\frac{35}{5} \\
\frac{40}{5}
\end{pmatrix} \\
&=
\begin{pmatrix}
7 \\
8
\end{pmatrix} \\
&=b.
\end{aligned}
$$

Both equations are satisfied, confirming the common solution obtained by the two methods.
