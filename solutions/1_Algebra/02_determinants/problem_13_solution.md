# Exercise 13. Determinant by Elimination

## Problem

Compute the determinant

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 5 & 7 \\
1 & 0 & 2
\end{pmatrix}
$$

using elimination. Record the effect of every row operation used on the value of the determinant.

> **Why this exercise:** reinforces organizing a determinant calculation through row operations without introducing an unnecessary second procedure.

## Method

We use elimination to create zeros below the main diagonal. Once the matrix is upper triangular, its determinant is the product of its diagonal entries.

At each step, we use a row operation of the form

$$
R_i\leftarrow R_i+cR_j,\qquad i\ne j.
$$

Adding a multiple of another row leaves the determinant unchanged. Since no row swaps or row scalings are needed, the final triangular matrix will have the same determinant as the original matrix.

## Solution

### 1. Eliminate the first entry of the second row

Apply

$$
R_2\leftarrow R_2-2R_1.
$$

The new second row is

$$
(2-2\cdot1,\;5-2\cdot2,\;7-2\cdot3)=(0,1,1).
$$

Thus, the matrix becomes

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
1 & 0 & 2
\end{pmatrix}.
$$

This operation leaves the determinant unchanged because it subtracts a multiple of another row.

### 2. Eliminate the first entry of the third row

Apply

$$
R_3\leftarrow R_3-R_1.
$$

The new third row is

$$
(1-1,\;0-2,\;2-3)=(0,-2,-1).
$$

We obtain

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & -2 & -1
\end{pmatrix}.
$$

This operation also leaves the determinant unchanged.

### 3. Eliminate the second entry of the third row

Using the current second row, apply

$$
R_3\leftarrow R_3+2R_2.
$$

The new third row is

$$
(0+2\cdot0,\;-2+2\cdot1,\;-1+2\cdot1)=(0,0,1).
$$

The resulting matrix is

$$
U=
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & 1
\end{pmatrix}.
$$

Again, the determinant is unchanged. The factor $2$ belongs to the row being added; it does not multiply the determinant by $2$.

### 4. Calculate the determinant

The matrix $U$ is upper triangular. Its determinant is therefore the product of its diagonal entries:

$$
\det U=1\cdot1\cdot1=1.
$$

All three row operations preserved the determinant, so

$$
\boxed{\det A=1}.
$$

## Verification

We can check the elimination arithmetic by reversing the row operations, starting from $U$.

First, subtract twice the second row from the third:

$$
(0,0,1)-2(0,1,1)=(0,-2,-1).
$$

Next, add the first row to the third:

$$
(0,-2,-1)+(1,2,3)=(1,0,2).
$$

Finally, add twice the first row to the second:

$$
(0,1,1)+2(1,2,3)=(2,5,7).
$$

These are exactly the rows of the original matrix. Each reverse operation also preserves the determinant, confirming that

$$
\det A=\det U=1.
$$
