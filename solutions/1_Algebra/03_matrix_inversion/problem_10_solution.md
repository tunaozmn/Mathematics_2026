# Exercise 10. Inverse of a Diagonal Matrix

## Problem

Given

$$
D=
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5
\end{pmatrix},\qquad E=
\begin{pmatrix}
2 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 5
\end{pmatrix}.
$$

Without using Gauss–Jordan elimination, decide which matrix is invertible. For the invertible matrix, give the inverse and check the result by multiplication.

> **Why this exercise:** teaches how to recognize invertibility and the inverse without using a full procedure when the matrix structure gives the answer immediately.

## Method

A diagonal matrix multiplies each coordinate by its corresponding diagonal entry. It is invertible exactly when every diagonal entry is nonzero.

In that case, the inverse is obtained by replacing each diagonal entry with its reciprocal. Multiplying the two diagonal matrices then gives 1 in every diagonal position and 0 elsewhere.

If a diagonal entry is zero, the corresponding coordinate is lost under the transformation, so the transformation cannot be reversed uniquely.

## Solution

### 1. Determine whether D is invertible

The diagonal entries of $D$ are $2$, $-3$, and $5$. All three are nonzero, so $D$ is invertible.

Equivalently, its determinant is

$$
\det D=2\cdot(-3)\cdot5=-30\ne0.
$$

### 2. Construct the inverse of D

Take the reciprocal of each diagonal entry:

$$
D^{-1}=
\begin{pmatrix}
\frac12 & 0 & 0 \\
0 & -\frac13 & 0 \\
0 & 0 & \frac15
\end{pmatrix}.
$$

The negative sign in the second entry remains because the reciprocal of $-3$ is $-\frac13$.

### 3. Determine whether E is invertible

The second diagonal entry of $E$ is zero. Thus,

$$
\det E=2\cdot0\cdot5=0,
$$

so $E$ is not invertible.

To see why this prevents an inverse, consider its action on a vector:

$$
\begin{aligned}
E
\begin{pmatrix}
x \\
y \\
z
\end{pmatrix}
&=
\begin{pmatrix}
2x \\
0 \\
5z
\end{pmatrix}.
\end{aligned}
$$

The output contains no information about $y$. Different vectors with the same first and third coordinates therefore have the same image, so the original vector cannot be recovered uniquely.

Hence, $E^{-1}$ does not exist.

## Verification

Multiply $D$ by the proposed inverse:

$$
\begin{aligned}
DD^{-1}
&=
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5
\end{pmatrix}
\begin{pmatrix}
\frac12 & 0 & 0 \\
0 & -\frac13 & 0 \\
0 & 0 & \frac15
\end{pmatrix} \\
&=
\begin{pmatrix}
2\cdot\frac12 & 0 & 0 \\
0 & (-3)\cdot\left(-\frac13\right) & 0 \\
0 & 0 & 5\cdot\frac15
\end{pmatrix} \\
&=
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix} \\
&=I.
\end{aligned}
$$

In the reverse order, the diagonal products are

$$
\frac12\cdot2=1,\qquad
\left(-\frac13\right)\cdot(-3)=1,\qquad
\frac15\cdot5=1.
$$

All off-diagonal entries remain zero, so $D^{-1}D=I$ as well. This confirms the inverse.
