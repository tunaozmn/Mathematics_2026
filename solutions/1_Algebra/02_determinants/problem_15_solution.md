# Exercise 15. Combining Determinant Properties

## Problem

Let $A$ and $B$ be invertible $2\times2$ matrices with

$$
\det A=-2,\qquad \det B=3.
$$

Without finding the entries of the matrices, compute

$$
\det\left(B^{-1}A^TB\right).
$$

State the determinant properties you use in order and explain why the factors involving $B$ eventually cancel.

> **Why this exercise:** tests the transfer of several known properties into one short problem instead of checking a single property again with numbers.

## Method

We use three determinant properties in order.

First, the determinant of a product is the product of the determinants:

$$
\det(XYZ)=\det X\det Y\det Z.
$$

Second, the determinant of an inverse is the reciprocal of the original determinant:

$$
\det(B^{-1})=\frac{1}{\det B}.
$$

This is valid because $B$ is invertible, so $\det B\ne0$.

Third, transposing a matrix does not change its determinant:

$$
\det(A^T)=\det A.
$$

Together, these properties let us evaluate the expression using only the given determinants.

## Solution

### 1. Apply the product property

Separate the determinant into three scalar factors:

$$
\det\left(B^{-1}A^TB\right)
=\det(B^{-1})\det(A^T)\det B.
$$

### 2. Apply the inverse property

Since $\det B=3$,

$$
\det(B^{-1})=\frac{1}{3}.
$$

Therefore,

$$
\det\left(B^{-1}A^TB\right)
=\frac{1}{3}\det(A^T)\cdot3.
$$

### 3. Apply the transpose property

The transpose has the same determinant as $A$:

$$
\det(A^T)=\det A=-2.
$$

Substituting gives

$$
\begin{aligned}
\det\left(B^{-1}A^TB\right)
&=\frac{1}{3}\cdot(-2)\cdot3\\
&=-2.
\end{aligned}
$$

Thus,

$$
\boxed{\det\left(B^{-1}A^TB\right)=-2}.
$$

### 4. Explain the cancellation

The factors involving $B$ are reciprocal numbers:

$$
\det(B^{-1})\det B
=\frac{1}{\det B}\det B
=1.
$$

Since determinants are scalars, we can rearrange these factors when multiplying. Consequently,

$$
\frac{1}{\det B}\det A\det B=\det A.
$$

This cancellation occurs after taking determinants. We do not cancel the matrices $B^{-1}$ and $B$ directly across the intervening matrix $A^T$.

## Verification

Let

$$
C=B^{-1}A^TB.
$$

Multiplying on the left by $B$ gives

$$
BC=(BB^{-1})A^TB=A^TB.
$$

Taking determinants on both sides,

$$
\det B\det C=\det(A^T)\det B.
$$

Using the given values,

$$
3\det C=(-2)\cdot3=-6.
$$

Dividing by $3$ confirms that

$$
\det C=-2.
$$
