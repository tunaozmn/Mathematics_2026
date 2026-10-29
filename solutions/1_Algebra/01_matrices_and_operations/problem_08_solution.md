# Problem 8 — Row Operations and Their Reversibility

## Problem

Given the matrix

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix},
$$

perform the following row operations in order:

1. Replace the second row by the second row minus twice the first row.
2. Replace the third row by the third row plus the first row.
3. Swap the second and third rows.

Write the matrix after each step and identify the inverse of each operation.

## Method

A row replacement changes only the specified row. All other rows remain unchanged. Each operation is applied to the matrix obtained in the previous step.

Adding a multiple of another row is reversed by subtracting the same multiple. Swapping two rows is reversed by swapping them again.

To reverse a sequence of operations, apply the inverse operations in reverse order.

## Solution

### 1. First row operation

Apply

$$
R_2\leftarrow R_2-2R_1.
$$

The new second row is

$$
\begin{pmatrix}
2 & 4 & 1 \\
\end{pmatrix}-
2\begin{pmatrix}
1 & 2 & -1 \\
\end{pmatrix}=
\begin{pmatrix}
2-2 & 4-4 & 1+2 \\
\end{pmatrix}=
\begin{pmatrix}
0 & 0 & 3 \\
\end{pmatrix}.
$$

Therefore, the matrix after the first step is

$$
A_1=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3 \\
\end{pmatrix}.
$$

The inverse operation is

$$
R_2\leftarrow R_2+2R_1.
$$

### 2. Second row operation

Starting from the matrix after the first step, apply

$$
R_3\leftarrow R_3+R_1.
$$

The new third row is

$$
\begin{pmatrix}
-1 & 1 & 3 \\
\end{pmatrix}+
\begin{pmatrix}
1 & 2 & -1 \\
\end{pmatrix}=
\begin{pmatrix}
0 & 3 & 2 \\
\end{pmatrix}.
$$

Therefore, the matrix after the second step is

$$
A_2=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2 \\
\end{pmatrix}.
$$

The inverse operation is

$$
R_3\leftarrow R_3-R_1.
$$

### 3. Third row operation

Swap the second and third rows:

$$
R_2\leftrightarrow R_3.
$$

The resulting matrix is

$$
A_3=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3 \\
\end{pmatrix}.
$$

The inverse operation is the same swap:

$$
R_2\leftrightarrow R_3.
$$

Swapping the same two rows twice restores their original positions.

## Verification

Starting from the final matrix, apply the inverse operations in reverse order.

First, swap the second and third rows again:

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3 \\
\end{pmatrix}
\xrightarrow{R_2\leftrightarrow R_3}
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2 \\
\end{pmatrix}.
$$

Next, subtract the first row from the third row:

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2 \\
\end{pmatrix}
\xrightarrow{R_3\leftarrow R_3-R_1}
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3 \\
\end{pmatrix}.
$$

Finally, add twice the first row to the second row:

$$
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3 \\
\end{pmatrix}
\xrightarrow{R_2\leftarrow R_2+2R_1}
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix}=A.
$$

The original matrix is recovered, confirming that all three operations are reversible.
