# Exercise 14. A Matrix That Is Its Own Inverse

## Problem

Assume that a square matrix $A$ satisfies

$$
A^2=I.
$$

Show that

$$
A^{-1}=A.
$$

Then give an example of a $2\times2$ matrix different from $I$ and $-I$ that satisfies this condition, and verify it by multiplication.

> **Why this exercise:** requires using the definition of the inverse in a short argument and constructing an example independently, without introducing a new topic.

## Method

By definition, a matrix $B$ is the inverse of $A$ if

$$
AB=BA=I.
$$

The condition $A^2=I$ already gives a product equal to the identity. We use it to show that $A$ itself satisfies the definition of the inverse.

For the example, we choose a matrix that exchanges the two coordinates. Exchanging them twice restores the original vector.

## Solution

### 1. Apply the definition of the inverse

The given condition means

$$
AA=I.
$$

Set $B=A$. Then both products required by the definition are

$$
AB=AA=I,
\qquad
BA=AA=I.
$$

Thus, $A$ is invertible, and its inverse is itself:

$$
A^{-1}=A.
$$

This argument establishes the existence of the inverse directly; we do not need to assume invertibility beforehand.

### 2. Construct an example

Choose

$$
A=
\begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix}.
$$

This matrix is different from both

$$
I=
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
\qquad\text{and}\qquad
-I=
\begin{pmatrix}
-1 & 0 \\
0 & -1
\end{pmatrix}.
$$

Its action on a vector is

$$
\begin{aligned}
A
\begin{pmatrix}
x \\
y
\end{pmatrix}
&=
\begin{pmatrix}
y \\
x
\end{pmatrix}.
\end{aligned}
$$

Applying the same transformation again exchanges the coordinates back. This suggests that $A^2=I$.

## Verification

Compute the square of the chosen matrix:

$$
\begin{aligned}
A^2
&=
\begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix}
\begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix} \\
&=
\begin{pmatrix}
0\cdot0+1\cdot1 & 0\cdot1+1\cdot0 \\
1\cdot0+0\cdot1 & 1\cdot1+0\cdot0
\end{pmatrix} \\
&=
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} \\
&=I.
\end{aligned}
$$

Therefore, the example satisfies the required condition, and

$$
A^{-1}=A=
\begin{pmatrix}
0 & 1 \\
1 & 0
\end{pmatrix}.
$$
