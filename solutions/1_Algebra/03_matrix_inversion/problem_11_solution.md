# Exercise 11. Parameter and Invertibility

## Problem

For

$$
A(t)=
\begin{pmatrix}
1 & t \\
t & 1
\end{pmatrix}
$$

find all $t$ for which the matrix is invertible, and then give a formula for $A(t)^{-1}$. Explain what happens to this formula at the excluded values.

> **Why this exercise:** combines a parameter, determinant, and an explicit inverse formula in one problem.

## Method

A square matrix is invertible exactly when its determinant is nonzero.

We first calculate the determinant as an expression in $t$ and identify the values where it vanishes. For all other values, we apply the inverse formula for a $2\times2$ matrix.

At the excluded values, we examine both the denominator in the formula and the rows of the original matrix.

## Solution

### 1. Calculate the determinant

For the given matrix,

$$
\begin{aligned}
\det A(t)
&=1\cdot1-t\cdot t \\
&=1-t^2 \\
&=(1-t)(1+t).
\end{aligned}
$$

The determinant is zero exactly when

$$
t=1 \quad \text{or} \quad t=-1.
$$

Therefore, $A(t)$ is invertible for every real $t$ satisfying

$$
t\ne1 \quad \text{and} \quad t\ne-1.
$$

### 2. Apply the inverse formula

For a $2\times2$ matrix, we interchange the diagonal entries, change the signs of the off-diagonal entries, and divide by the determinant.

The diagonal entries are both 1, so interchanging them leaves them unchanged. The off-diagonal entries become $-t$.

Thus,

$$
A(t)^{-1}=
\frac{1}{1-t^2}
\begin{pmatrix}
1 & -t \\
-t & 1
\end{pmatrix},
\qquad t\ne1,\quad t\ne-1.
$$

### 3. Explain the excluded values

At $t=1$ or $t=-1$, the denominator $1-t^2$ is zero, so the inverse formula is undefined. This reflects the fact that the original matrix has no inverse at these values.

When $t=1$,

$$
A(1)=
\begin{pmatrix}
1 & 1 \\
1 & 1
\end{pmatrix}.
$$

The two rows are identical, so they are linearly dependent.

When $t=-1$,

$$
A(-1)=
\begin{pmatrix}
1 & -1 \\
-1 & 1
\end{pmatrix}.
$$

The second row is the negative of the first, so the rows are again linearly dependent.

In both cases, the determinant is zero and no inverse exists.

## Verification

For $t\ne1$ and $t\ne-1$, multiply the original matrix by the proposed inverse:

$$
\begin{aligned}
A(t)A(t)^{-1}
&=
\frac{1}{1-t^2}
\begin{pmatrix}
1 & t \\
t & 1
\end{pmatrix}
\begin{pmatrix}
1 & -t \\
-t & 1
\end{pmatrix} \\
&=
\frac{1}{1-t^2}
\begin{pmatrix}
1-t^2 & -t+t \\
t-t & 1-t^2
\end{pmatrix} \\
&=
\frac{1}{1-t^2}
\begin{pmatrix}
1-t^2 & 0 \\
0 & 1-t^2
\end{pmatrix} \\
&=I.
\end{aligned}
$$

In the reverse order,

$$
\begin{aligned}
A(t)^{-1}A(t)
&=
\frac{1}{1-t^2}
\begin{pmatrix}
1 & -t \\
-t & 1
\end{pmatrix}
\begin{pmatrix}
1 & t \\
t & 1
\end{pmatrix} \\
&=
\frac{1}{1-t^2}
\begin{pmatrix}
1-t^2 & t-t \\
-t+t & 1-t^2
\end{pmatrix} \\
&=I.
\end{aligned}
$$

Both products equal the identity, confirming the formula for every permitted value of $t$.
