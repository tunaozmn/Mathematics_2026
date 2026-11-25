# Exercise 2. Formula for a 2×2 Matrix

## Problem

Find the inverse of

$$
A=
\begin{pmatrix}
3 & 2 \\
5 & 4
\end{pmatrix}
$$

using the formula for a $2\times2$ matrix. At the end, check the result by computing one product with $A$.

> **Why this exercise:** teaches the simplest explicit formula for an inverse and requires verification using the definition.

## Method

For a matrix

$$
M=
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix},
$$

the inverse exists exactly when its determinant is nonzero:

$$
\det M=ad-bc\ne0.
$$

In that case,

$$
M^{-1}=\frac{1}{ad-bc}
\begin{pmatrix}
d & -b \\
-c & a
\end{pmatrix}.
$$

To apply the formula, we interchange the two diagonal entries, change the signs of the other two entries, and multiply the resulting matrix by the reciprocal of the determinant.

## Solution

### 1. Check that the inverse exists

The determinant of $A$ is

$$
\begin{aligned}
\det A
&=3\cdot4-2\cdot5\\
&=12-10\\
&=2.
\end{aligned}
$$

Since $\det A=2\ne0$, the matrix is invertible.

### 2. Apply the inverse formula

Here, $a=3$, $b=2$, $c=5$, and $d=4$.

Interchanging the diagonal entries and changing the signs of the off-diagonal entries gives

$$
\begin{pmatrix}
4 & -2 \\
-5 & 3
\end{pmatrix}.
$$

Multiplying by the reciprocal of the determinant, we obtain

$$
A^{-1}=\frac12
\begin{pmatrix}
4 & -2 \\
-5 & 3
\end{pmatrix}.
$$

### 3. Simplify the entries

The factor $\frac12$ multiplies every entry. Therefore,

$$
A^{-1}=
\begin{pmatrix}
2 & -1 \\
-\frac52 & \frac32
\end{pmatrix}.
$$

## Verification

Compute $AA^{-1}$ using the factored form of the inverse:

$$
AA^{-1}=\frac12
\begin{pmatrix}
3 & 2 \\
5 & 4
\end{pmatrix}
\begin{pmatrix}
4 & -2 \\
-5 & 3
\end{pmatrix}.
$$

Using row-by-column multiplication,

$$
AA^{-1}=\frac12
\begin{pmatrix}
3\cdot4+2\cdot(-5) & 3\cdot(-2)+2\cdot3 \\
5\cdot4+4\cdot(-5) & 5\cdot(-2)+4\cdot3
\end{pmatrix}.
$$

Thus,

$$
\begin{aligned}
AA^{-1}
&=\frac12
\begin{pmatrix}
12-10 & -6+6 \\
20-20 & -10+12
\end{pmatrix}\\
&=\frac12
\begin{pmatrix}
2 & 0 \\
0 & 2
\end{pmatrix}\\
&=
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}\\
&=I.
\end{aligned}
$$

The product is the identity matrix, confirming the calculated inverse.
