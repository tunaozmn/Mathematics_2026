# Exercise 1. Determinant of a 2×2 Matrix

## Problem

Compute

$$
\det
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix},\qquad \det
\begin{pmatrix}
1 & 7 \\
2 & 14 \\
\end{pmatrix}.
$$

Which matrix is invertible? Justify your answer.

> **Why this exercise:** introduces the simplest determinant calculation and immediately connects it with invertibility.

## Method

For a $2\times2$ matrix, the determinant is

$$
\det
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
=ad-bc.
$$

We calculate the two products separately and subtract the second from the first, keeping the signs of the entries.

A square matrix is invertible if and only if its determinant is nonzero. Therefore, after computing the determinants, we can decide whether each matrix has an inverse.

In the solution below, let $A$ denote the first matrix and $B$ the second.

## Solution

### 1. Calculate the determinant of the first matrix

For $A$, the two products are

$$
ad=3\cdot4=12,
\qquad
bc=(-2)\cdot5=-10.
$$

Substituting into the formula,

$$
\begin{aligned}
\det A
&=3\cdot4-(-2)\cdot5\\
&=12-(-10)\\
&=12+10\\
&=22.
\end{aligned}
$$

The negative sign in the entry $-2$ matters: the product being subtracted is $-10$, so this subtraction becomes addition.

### 2. Calculate the determinant of the second matrix

For $B$, the two products are

$$
ad=1\cdot14=14,
\qquad
bc=7\cdot2=14.
$$

Therefore,

$$
\begin{aligned}
\det B
&=1\cdot14-7\cdot2\\
&=14-14\\
&=0.
\end{aligned}
$$

### 3. Determine which matrix is invertible

The first matrix satisfies

$$
\det A=22\neq0,
$$

so $A$ is invertible.

The second matrix satisfies

$$
\det B=0,
$$

so $B$ is not invertible.

Thus, only the first matrix has an inverse.

## Verification

Adding a multiple of one row to another does not change the determinant. We can use this property to simplify both matrices and check the results.

For the first matrix, apply $R_2\leftarrow R_2+2R_1$:

$$
\begin{pmatrix}
3 & -2\\
5 & 4
\end{pmatrix}
\longrightarrow
\begin{pmatrix}
3 & -2\\
11 & 0
\end{pmatrix}.
$$

The determinant of the resulting matrix is

$$
3\cdot0-(-2)\cdot11=22,
$$

which confirms the first result.

For the second matrix, apply $R_2\leftarrow R_2-2R_1$:

$$
\begin{pmatrix}
1 & 7\\
2 & 14
\end{pmatrix}
\longrightarrow
\begin{pmatrix}
1 & 7\\
0 & 0
\end{pmatrix}.
$$

Its determinant is zero because it has a zero row. This confirms the second result.

The original second row of $B$ is twice its first row, so its rows are linearly dependent. This also explains why $B$ is not invertible.
