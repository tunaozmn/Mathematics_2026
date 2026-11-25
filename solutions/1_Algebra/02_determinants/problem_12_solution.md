# Exercise 12. A Parameter Revealed by a Row Operation

## Problem

For

$$
A(t)=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & t \\
0 & 1 & 1 \\
\end{pmatrix}
$$

find the values of $t$ for which the matrix is not invertible.

Before computing the determinant, perform the operation

$$
R_2\leftarrow R_2-2R_1
$$

and use the resulting structure. At the end, explain what special thing happens to the rows for the value of the parameter you found.

> **Why this exercise:** combines a parameter, row operations, and recognition of dependence in one short argument.

## Method

Subtracting a multiple of one row from another does not change the determinant.

The required operation creates two zeros in the second row. We can then expand along that row, leaving only one potentially nonzero term.

Finally, a square matrix is not invertible exactly when its determinant is zero. We solve this condition for $t$ and examine the corresponding rows of the original matrix.

## Solution

### 1. Apply the required row operation

Before calculating the determinant, perform

$$
R_2\leftarrow R_2-2R_1.
$$

The new second row is

$$
(2-2\cdot1,\;4-2\cdot2,\;t-2\cdot3)
=(0,0,t-6).
$$

Therefore, the transformed matrix is

$$
C(t)=
\begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & t-6 \\
0 & 1 & 1
\end{pmatrix}.
$$

The determinant is unchanged:

$$
\det A(t)=\det C(t).
$$

### 2. Use the zeros to calculate the determinant

The only potentially nonzero entry in the second row is $t-6$, in position $(2,3)$.

Its cofactor sign is

$$
(-1)^{2+3}=-1.
$$

Removing the second row and third column leaves the matrix

$$
\begin{pmatrix}
1 & 2 \\
0 & 1
\end{pmatrix},
$$

whose determinant is

$$
1\cdot1-2\cdot0=1.
$$

Thus,

$$
\begin{aligned}
\det A(t)
&=-(t-6)\cdot1\\
&=6-t.
\end{aligned}
$$

### 3. Find the parameter value for noninvertibility

Set the determinant equal to zero:

$$
6-t=0.
$$

Solving gives

$$
t=6.
$$

Therefore, $A(t)$ is not invertible only when $t=6$. For every other real value of $t$, its determinant is nonzero and the matrix is invertible.

### 4. Explain what happens to the rows

Substituting $t=6$ into the original matrix gives

$$
A(6)=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
0 & 1 & 1
\end{pmatrix}.
$$

The second row is now exactly twice the first:

$$
(2,4,6)=2(1,2,3).
$$

Hence, the rows are linearly dependent. The required row operation turns the second row into a zero row, explaining why the determinant vanishes.

## Verification

We can check the determinant expression by expanding the original matrix along its first column:

$$
\begin{aligned}
\det A(t)
&=1(4\cdot1-t\cdot1)-2(2\cdot1-3\cdot1)\\
&=(4-t)-2(-1)\\
&=6-t.
\end{aligned}
$$

This agrees with the expression obtained after the row operation. In particular,

$$
\det A(6)=6-6=0,
$$

confirming the parameter value found.
