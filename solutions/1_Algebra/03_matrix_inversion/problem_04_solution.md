# Exercise 4. Gauss–Jordan

## Problem

Find $A^{-1}$ using the Gauss–Jordan method for

$$
A=
\begin{pmatrix}
1 & 2 \\
3 & 5
\end{pmatrix}.
$$

Show the augmented matrix $[A\mid I]$ after successive operations and explain why obtaining $I$ on the left gives the inverse on the right.

> **Why this exercise:** introduces the Gauss–Jordan method together with its meaning, not merely as a sequence of operations.

## Method

We place the identity matrix to the right of $A$ to form the augmented matrix $[A\mid I]$.

We then apply elementary row operations to the entire augmented matrix until the left block becomes $I$. The right block will then be $A^{-1}$:

$$
[A\mid I]\longrightarrow[I\mid A^{-1}].
$$

Every operation must act on both blocks. We create a leading $1$ in each row and eliminate the other entries in its column.

## Solution

### 1. Form the augmented matrix

Start with

$$
[A\mid I]=
\left[
\begin{array}{cc|cc}
1 & 2 & 1 & 0 \\
3 & 5 & 0 & 1
\end{array}
\right].
$$

The first pivot is already $1$, so we can eliminate the entry below it.

### 2. Eliminate the first entry of the second row

Apply

$$
R_2\leftarrow R_2-3R_1.
$$

The new second row is

$$
(3-3\cdot1,\;5-3\cdot2,\;0-3\cdot1,\;1-3\cdot0)
=(0,-1,-3,1).
$$

Thus, the augmented matrix becomes

$$
\left[
\begin{array}{cc|cc}
1 & 2 & 1 & 0 \\
0 & -1 & -3 & 1
\end{array}
\right].
$$

### 3. Make the second pivot equal to one

Apply

$$
R_2\leftarrow -R_2.
$$

This changes the sign of every entry in the second row:

$$
\left[
\begin{array}{cc|cc}
1 & 2 & 1 & 0 \\
0 & 1 & 3 & -1
\end{array}
\right].
$$

### 4. Eliminate the entry above the second pivot

Using the current second row, apply

$$
R_1\leftarrow R_1-2R_2.
$$

The new first row is

$$
(1-2\cdot0,\;2-2\cdot1,\;1-2\cdot3,\;0-2\cdot(-1))
=(1,0,-5,2).
$$

We obtain

$$
\left[
\begin{array}{cc|cc}
1 & 0 & -5 & 2 \\
0 & 1 & 3 & -1
\end{array}
\right].
$$

The left block is now the identity matrix. Therefore, the right block gives

$$
A^{-1}=
\begin{pmatrix}
-5 & 2 \\
3 & -1
\end{pmatrix}.
$$

### 5. Explain why the method works

Each elementary row operation is equivalent to multiplying on the left by an invertible elementary matrix.

Let $E$ represent the combined effect of all the operations. Applying them to both blocks transforms the augmented matrix into

$$
[EA\mid EI].
$$

Since the left block has become $I$, we have

$$
EA=I.
$$

The matrix $E$ is invertible because all the row operations are reversible. Hence, $EA=I$ implies $A=E^{-1}$, and therefore $E=A^{-1}$.

The right block is $EI=E$, so it is exactly $A^{-1}$.

## Verification

Let

$$
C=
\begin{pmatrix}
-5 & 2 \\
3 & -1
\end{pmatrix}
$$

be the inverse obtained above. Multiplying by the original matrix gives

$$
AC=
\begin{pmatrix}
1\cdot(-5)+2\cdot3 & 1\cdot2+2\cdot(-1) \\
3\cdot(-5)+5\cdot3 & 3\cdot2+5\cdot(-1)
\end{pmatrix}.
$$

Simplifying,

$$
\begin{aligned}
AC&=
\begin{pmatrix}
-5+6 & 2-2 \\
-15+15 & 6-5
\end{pmatrix}\\
&=
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}\\
&=I.
\end{aligned}
$$

The reverse product also gives

$$
CA=
\begin{pmatrix}
-5+6 & -10+10 \\
3-3 & 6-5
\end{pmatrix}
=I.
$$

Thus, $AC=CA=I$, confirming that the right block obtained by Gauss–Jordan elimination is the inverse of $A$.
