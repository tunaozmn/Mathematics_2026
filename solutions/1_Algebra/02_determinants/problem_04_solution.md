# Exercise 4. Triangular Matrix

## Problem

Without expanding the determinant, compute

$$
\det
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}.
$$

State the rule for an arbitrary triangular matrix and explain it using this example.

> **Why this exercise:** reinforces an important property of triangular matrices.

## Method

A square matrix is upper triangular when every entry below its main diagonal is zero. It is lower triangular when every entry above its main diagonal is zero.

For either type of triangular matrix, the determinant equals the product of the main diagonal entries:

$$
\det T=t_{11}t_{22}\cdots t_{nn}.
$$

Therefore, we first check that the matrix is triangular, identify its diagonal entries, and multiply them. No determinant expansion is needed.

## Solution

### 1. Identify the triangular structure

Let $T$ denote the given matrix:

$$
T=
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7
\end{pmatrix}.
$$

The entries below the main diagonal are

$$
t_{21}=0,\qquad t_{31}=0,\qquad t_{32}=0.
$$

Thus, $T$ is upper triangular, so the diagonal-product rule applies.

### 2. Multiply the diagonal entries

The main diagonal contains $2$, $-3$, and $7$. Hence,

$$
\begin{aligned}
\det T
&=2\cdot(-3)\cdot7\\
&=(-6)\cdot7\\
&=-42.
\end{aligned}
$$

### 3. Explain the rule in this example

The entries $4$, $1$, and $5$ lie above the main diagonal. They do not affect the determinant of this triangular matrix.

The triangular pattern of zeros ensures that every term in the determinant formula other than the diagonal product contains a zero factor. This leaves only the product of the diagonal entries.

The same reasoning applies to triangular matrices of any size, whether upper or lower triangular.

## Verification

As an arithmetic check, multiply the diagonal entries in a different grouping:

$$
2\cdot((-3)\cdot7)=2\cdot(-21)=-42.
$$

There is exactly one negative diagonal entry, so the product must be negative. Its absolute value is

$$
2\cdot3\cdot7=42.
$$

Both checks are consistent with $\det T=-42$.
