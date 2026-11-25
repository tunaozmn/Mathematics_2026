# Exercise 10. Detecting Dependence

## Problem

Without carrying out a full determinant calculation, explain why

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
0 & 1 & 5 \\
\end{pmatrix}=0.
$$

Identify a specific dependence between the rows and connect it with noninvertibility of the matrix.

> **Why this exercise:** teaches how to recognize a zero determinant from the structure of a matrix.

## Method

If one row of a matrix is a multiple of another, its rows are linearly dependent. A square matrix with linearly dependent rows has determinant zero.

We can demonstrate this dependence by subtracting a suitable multiple of one row from another. This operation preserves the determinant and produces a zero row.

Finally, we use the fact that a square matrix is invertible if and only if its determinant is nonzero.

## Solution

### 1. Identify the dependence between the rows

Let $A$ denote the given matrix. Its first two rows are

$$
R_1=(1,2,3),
\qquad
R_2=(2,4,6).
$$

Every entry of the second row is twice the corresponding entry of the first:

$$
R_2=2R_1.
$$

Equivalently,

$$
R_2-2R_1=(0,0,0).
$$

This is a nontrivial linear relation between the rows, so they are linearly dependent.

### 2. Use a row operation to explain the zero determinant

Apply

$$
R_2\leftarrow R_2-2R_1.
$$

The matrix becomes

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & 0 \\
0 & 1 & 5
\end{pmatrix}.
$$

Subtracting a multiple of another row does not change the determinant. The resulting matrix has a zero row, so its determinant is zero.

Therefore,

$$
\det A=0.
$$

No full determinant expansion is needed.

### 3. Explain noninvertibility

Since the determinant is zero, $A$ is not invertible.

The row relation explains this: the second row repeats the information contained in the first row, multiplied by $2$. Thus, the three rows are not independent.

## Verification

We can also confirm noninvertibility by finding a nonzero vector that $A$ maps to zero.

Take

$$
x=
\begin{pmatrix}
7 \\
-5 \\
1
\end{pmatrix}.
$$

Then

$$
\begin{aligned}
Ax&=
\begin{pmatrix}
1\cdot7+2\cdot(-5)+3\cdot1 \\
2\cdot7+4\cdot(-5)+6\cdot1 \\
0\cdot7+1\cdot(-5)+5\cdot1
\end{pmatrix}\\
&=
\begin{pmatrix}
7-10+3 \\
14-20+6 \\
-5+5
\end{pmatrix}\\
&=
\begin{pmatrix}
0 \\
0 \\
0
\end{pmatrix}.
\end{aligned}
$$

If $A$ had an inverse, multiplying $Ax=0$ by $A^{-1}$ would give $x=0$. However, the chosen vector is nonzero.

This confirms that $A$ is not invertible, consistent with $\det A=0$.
