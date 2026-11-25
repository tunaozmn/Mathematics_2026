# Exercise 5. A 3×3 Matrix

## Problem

Use Gauss–Jordan elimination to find the inverse of

$$
A=
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1
\end{pmatrix}.
$$

Check the result by multiplication.

> **Why this exercise:** provides necessary practice with the full method in a situation where the $2\times2$ formula no longer applies.

## Method

We form the augmented matrix $[A\mid I]$, using the $3\times3$ identity matrix.

We apply row operations to both blocks until the left block becomes the identity. The right block then gives the inverse:

$$
[A\mid I]\longrightarrow[I\mid A^{-1}].
$$

First, we eliminate the entries below the diagonal. Then we make every pivot equal to $1$ and eliminate the entries above the pivots.

## Solution

### 1. Form the augmented matrix

Start with

$$
\left[
\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
1 & 0 & 1 & 0 & 0 & 1
\end{array}
\right].
$$

### 2. Eliminate the first entry of the third row

Apply

$$
R_3\leftarrow R_3-R_1.
$$

On the left, the third row becomes $(0,-1,1)$. On the right, it becomes $(-1,0,1)$.

Thus,

$$
\left[
\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
0 & -1 & 1 & -1 & 0 & 1
\end{array}
\right].
$$

### 3. Eliminate the second entry of the third row

Apply

$$
R_3\leftarrow R_3+R_2.
$$

The left part of the third row becomes $(0,0,2)$, while the right part becomes $(-1,1,1)$:

$$
\left[
\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
0 & 0 & 2 & -1 & 1 & 1
\end{array}
\right].
$$

### 4. Make the third pivot equal to one

Divide the entire third row by $2$:

$$
R_3\leftarrow\frac12R_3.
$$

We obtain

$$
\left[
\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
0 & 0 & 1 & -\frac12 & \frac12 & \frac12
\end{array}
\right].
$$

### 5. Eliminate the entry above the third pivot

Apply

$$
R_2\leftarrow R_2-R_3.
$$

The right part of the second row becomes

$$
\left(0-\left(-\frac12\right),\;1-\frac12,\;0-\frac12\right)
=\left(\frac12,\frac12,-\frac12\right).
$$

Therefore,

$$
\left[
\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 0 & \frac12 & \frac12 & -\frac12 \\
0 & 0 & 1 & -\frac12 & \frac12 & \frac12
\end{array}
\right].
$$

The first row already has a zero in the third column, so no operation is needed there.

### 6. Eliminate the entry above the second pivot

Using the current second row, apply

$$
R_1\leftarrow R_1-R_2.
$$

The right part of the first row becomes

$$
\left(1-\frac12,\;0-\frac12,\;0-\left(-\frac12\right)\right)
=\left(\frac12,-\frac12,\frac12\right).
$$

The augmented matrix is now

$$
\left[
\begin{array}{ccc|ccc}
1 & 0 & 0 & \frac12 & -\frac12 & \frac12 \\
0 & 1 & 0 & \frac12 & \frac12 & -\frac12 \\
0 & 0 & 1 & -\frac12 & \frac12 & \frac12
\end{array}
\right].
$$

### 7. Read off the inverse

The left block is the identity matrix. Hence, the right block is

$$
A^{-1}=
\frac12
\begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1
\end{pmatrix}.
$$

## Verification

Multiply the original matrix by the proposed inverse:

$$
AA^{-1}=
\frac12
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1
\end{pmatrix}
\begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1
\end{pmatrix}.
$$

Each row of $A$ selects a sum of two rows of the second matrix. Thus,

$$
\begin{aligned}
AA^{-1}
&=\frac12
\begin{pmatrix}
1+1 & -1+1 & 1-1 \\
1-1 & 1+1 & -1+1 \\
1-1 & -1+1 & 1+1
\end{pmatrix}\\
&=\frac12
\begin{pmatrix}
2 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 2
\end{pmatrix}\\
&=
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix}\\
&=I.
\end{aligned}
$$

The product is the identity matrix, confirming the inverse obtained by Gauss–Jordan elimination.
