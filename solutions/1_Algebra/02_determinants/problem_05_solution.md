# Exercise 5. Row Operations

## Problem

For

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 1 & 0 \\
-1 & 4 & 2 \\
\end{pmatrix}
$$

find $\det A$ by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

> **Why this exercise:** connects determinants with row operations and requires conscious tracking of every step.

## Method

We use row operations to transform the matrix into upper triangular form. Its determinant can then be found by multiplying the diagonal entries.

The three elementary row operations affect the determinant as follows:

- Swapping two rows changes its sign.
- Multiplying one row by a nonzero number multiplies the determinant by that number.
- Adding a multiple of another row leaves the determinant unchanged.

We will use only the third type:

$$
R_i\leftarrow R_i+cR_j,\qquad i\neq j.
$$

Therefore, every matrix obtained during our calculation will have the same determinant as $A$.

## Solution

### 1. Eliminate the first entry of the second row

Apply

$$
R_2\leftarrow R_2-2R_1.
$$

The new second row is

$$
(2-2\cdot1,\;1-2\cdot2,\;0-2\cdot3)
=(0,-3,-6).
$$

Thus, the matrix becomes

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
-1 & 4 & 2
\end{pmatrix}.
$$

This operation leaves the determinant unchanged because we subtract a multiple of another row.

### 2. Eliminate the first entry of the third row

Apply

$$
R_3\leftarrow R_3+R_1.
$$

The new third row is

$$
(-1+1,\;4+2,\;2+3)=(0,6,5).
$$

We obtain

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 6 & 5
\end{pmatrix}.
$$

Adding the first row to the third row also leaves the determinant unchanged.

### 3. Eliminate the second entry of the third row

Using the current second row, apply

$$
R_3\leftarrow R_3+2R_2.
$$

The new third row is

$$
(0+2\cdot0,\;6+2\cdot(-3),\;5+2\cdot(-6))
=(0,0,-7).
$$

The resulting matrix is

$$
U=
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 0 & -7
\end{pmatrix}.
$$

This operation again leaves the determinant unchanged. The factor $2$ multiplies the row being added; it does not multiply the determinant by $2$.

### 4. Calculate the determinant

The matrix $U$ is upper triangular. Since all three operations preserved the determinant,

$$
\begin{aligned}
\det A
&=\det U\\
&=1\cdot(-3)\cdot(-7)\\
&=21.
\end{aligned}
$$

Therefore, the determinant of the original matrix is $21$.

## Verification

We can check the result by expanding the original determinant along its second row, which contains a zero. The cofactor signs along this row are $-$, $+$, and $-$.

$$
\begin{aligned}
\det A
&=-2\bigl(2\cdot2-3\cdot4\bigr)
+1\bigl(1\cdot2-3\cdot(-1)\bigr)\\
&=-2(4-12)+(2+3)\\
&=16+5\\
&=21.
\end{aligned}
$$

This agrees with the result obtained using row operations.
