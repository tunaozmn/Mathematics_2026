# Exercise 11. Shortening the Calculation with Row Operations

## Problem

Compute

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6 \\
\end{pmatrix}
$$

by first performing row operations that create as many zeros as possible. State which operations do not change the determinant.

> **Why this exercise:** develops planning instead of mechanically repeating the same procedure.

## Method

The first column contains three identical entries. Subtracting the first row from each of the other two rows will therefore create two zeros immediately.

We use row operations of the form

$$
R_i\leftarrow R_i+cR_j,\qquad i\neq j.
$$

Adding a multiple of another row does not change the determinant.

After creating zeros below the main diagonal, we can calculate the determinant by multiplying the diagonal entries of the resulting upper triangular matrix.

## Solution

### 1. Create zeros in the first column

Let $A$ denote the given matrix. Apply

$$
R_2\leftarrow R_2-R_1,
\qquad
R_3\leftarrow R_3-R_1.
$$

The new rows are

$$
R_2=(1-1,\;3-2,\;4-3)=(0,1,1),
$$

and

$$
R_3=(1-1,\;4-2,\;6-3)=(0,2,3).
$$

Thus, the matrix becomes

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 2 & 3
\end{pmatrix}.
$$

Both operations preserve the determinant. The first row remains unchanged.

### 2. Create a zero below the second diagonal entry

Using the current second row, apply

$$
R_3\leftarrow R_3-2R_2.
$$

The new third row is

$$
(0-2\cdot0,\;2-2\cdot1,\;3-2\cdot1)=(0,0,1).
$$

We obtain

$$
U=
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & 1
\end{pmatrix}.
$$

This operation also leaves the determinant unchanged.

### 3. Calculate the determinant

The matrix is now upper triangular. All entries below its main diagonal are zero, so no further row operations are needed.

Since every operation preserved the determinant,

$$
\begin{aligned}
\det A
&=\det U\\
&=1\cdot1\cdot1\\
&=1.
\end{aligned}
$$

Therefore, the determinant of the original matrix is $1$.

## Verification

We can check the result by expanding the original determinant along its first row:

$$
\begin{aligned}
\det A
&=1(3\cdot6-4\cdot4)
-2(1\cdot6-4\cdot1)
+3(1\cdot4-3\cdot1)\\
&=(18-16)-2(6-4)+3(4-3)\\
&=2-4+3\\
&=1.
\end{aligned}
$$

This agrees with the result obtained by creating zeros through row operations.
