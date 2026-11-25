# Exercise 7. Inverse of a Product

## Problem

For

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix},
\qquad
B=
\begin{pmatrix}
2 & 0 \\
0 & 3
\end{pmatrix}
$$

compute $(AB)^{-1}$ and $B^{-1}A^{-1}$. Check that the results are the same and explain the meaning of the reversed order.

> **Why this exercise:** reinforces the inverse-of-a-product property and requires its interpretation.

## Method

For two invertible matrices of the same size,

$$
(AB)^{-1}=B^{-1}A^{-1}.
$$

We will calculate both sides separately: first find $AB$ and invert it, then find the individual inverses and multiply them in the reversed order.

For a $2\times2$ matrix

$$
M=
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
$$

with $ad-bc\ne0$, we use

$$
M^{-1}=\frac{1}{ad-bc}
\begin{pmatrix}
d & -b \\
-c & a
\end{pmatrix}.
$$

## Solution

### 1. Calculate AB

Using row-by-column multiplication,

$$
\begin{aligned}
AB
&=
\begin{pmatrix}
1\cdot2+1\cdot0 & 1\cdot0+1\cdot3 \\
0\cdot2+1\cdot0 & 0\cdot0+1\cdot3
\end{pmatrix}\\
&=
\begin{pmatrix}
2 & 3 \\
0 & 3
\end{pmatrix}.
\end{aligned}
$$

### 2. Find the inverse of AB

The determinant is

$$
\det(AB)=2\cdot3-3\cdot0=6.
$$

Since it is nonzero, the inverse exists. Applying the formula gives

$$
\begin{aligned}
(AB)^{-1}
&=\frac16
\begin{pmatrix}
3 & -3 \\
0 & 2
\end{pmatrix}\\
&=
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & \frac13
\end{pmatrix}.
\end{aligned}
$$

### 3. Find the individual inverses

For $A$,

$$
\det A=1\cdot1-1\cdot0=1.
$$

Therefore,

$$
A^{-1}=
\begin{pmatrix}
1 & -1 \\
0 & 1
\end{pmatrix}.
$$

For $B$,

$$
\det B=2\cdot3-0\cdot0=6.
$$

Hence,

$$
B^{-1}=
\begin{pmatrix}
\frac12 & 0 \\
0 & \frac13
\end{pmatrix}.
$$

### 4. Calculate B inverse times A inverse

Multiply in the required order:

$$
B^{-1}A^{-1}=
\begin{pmatrix}
\frac12 & 0 \\
0 & \frac13
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
0 & 1
\end{pmatrix}.
$$

Thus,

$$
\begin{aligned}
B^{-1}A^{-1}
&=
\begin{pmatrix}
\frac12\cdot1+0\cdot0 & \frac12\cdot(-1)+0\cdot1 \\
0\cdot1+\frac13\cdot0 & 0\cdot(-1)+\frac13\cdot1
\end{pmatrix}\\
&=
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & \frac13
\end{pmatrix}.
\end{aligned}
$$

This is exactly the matrix obtained for $(AB)^{-1}$.

### 5. Explain the reversed order

When $AB$ acts on a column vector $x$, the matrix $B$ acts first:

$$
(AB)x=A(Bx).
$$

To recover $x$, we must first undo the action of $A$ using $A^{-1}$, then undo the action of $B$ using $B^{-1}$.

The combined operation is therefore $B^{-1}A^{-1}$, since the rightmost matrix acts first.

The reversed order also places each matrix next to its inverse:

$$
(AB)(B^{-1}A^{-1})
=A(BB^{-1})A^{-1}
=AA^{-1}
=I.
$$

## Verification

Let

$$
C=
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & \frac13
\end{pmatrix}.
$$

Check its product with $AB$:

$$
\begin{aligned}
(AB)C
&=
\begin{pmatrix}
2 & 3 \\
0 & 3
\end{pmatrix}
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & \frac13
\end{pmatrix}\\
&=
\begin{pmatrix}
1+0 & -1+1 \\
0+0 & 0+1
\end{pmatrix}\\
&=I.
\end{aligned}
$$

In the reverse direction,

$$
C(AB)=
\begin{pmatrix}
1 & \frac32-\frac32 \\
0 & 1
\end{pmatrix}
=I.
$$

Both products confirm that

$$
(AB)^{-1}=B^{-1}A^{-1}=
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & \frac13
\end{pmatrix}.
$$
