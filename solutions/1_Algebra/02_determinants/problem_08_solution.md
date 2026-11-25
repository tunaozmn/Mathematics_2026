# Exercise 8. Determinant of a Product

## Problem

Let $A,B$ be square matrices such that $\det A=3$ and $\det B=-5$. Compute $\det(AB)$, $\det(BA)$ and, if it exists, $\det(A^{-1}B)$. Explain why the first two results are equal even though usually $AB\neq BA$.

> **Why this exercise:** organizes how determinants behave with respect to products and inverses.

## Method

The requested products require $A$ and $B$ to have the same size.

For square matrices of the same size, the determinant of a product is the product of their determinants:

$$
\det(AB)=\det A\det B.
$$

Before using $A^{-1}$, we must check that $A$ is invertible. If $\det A\neq0$, its inverse exists and satisfies

$$
\det(A^{-1})=\frac{1}{\det A}.
$$

These properties allow us to calculate the requested determinants without knowing the entries of either matrix.

## Solution

### 1. Calculate the determinant of AB

Using the product property,

$$
\begin{aligned}
\det(AB)
&=\det A\det B\\
&=3\cdot(-5)\\
&=-15.
\end{aligned}
$$

### 2. Calculate the determinant of BA

Applying the same property in the reverse order,

$$
\begin{aligned}
\det(BA)
&=\det B\det A\\
&=(-5)\cdot3\\
&=-15.
\end{aligned}
$$

### 3. Check that the inverse of A exists

The given determinant is

$$
\det A=3\neq0.
$$

Therefore, $A$ is invertible, and

$$
\det(A^{-1})=\frac{1}{3}.
$$

### 4. Calculate the determinant of the remaining product

We can now apply the product property to $A^{-1}B$:

$$
\begin{aligned}
\det(A^{-1}B)
&=\det(A^{-1})\det B\\
&=\frac13\cdot(-5)\\
&=-\frac53.
\end{aligned}
$$

### 5. Explain why the first two determinants are equal

The matrices $AB$ and $BA$ need not be equal because matrix multiplication is generally not commutative.

However, their determinants are calculated by multiplying the same two real numbers in opposite orders:

$$
\det A\det B=3(-5)=(-5)3=\det B\det A.
$$

Multiplication of real numbers is commutative, so

$$
\det(AB)=\det(BA).
$$

Equal determinants do not imply that the matrices themselves are equal.

## Verification

Let $C=A^{-1}B$. Multiplying on the left by $A$ gives

$$
AC=A(A^{-1}B)=(AA^{-1})B=B.
$$

Consequently, the determinants must satisfy

$$
\det A\det C=\det B.
$$

Substituting our result,

$$
3\cdot\left(-\frac53\right)=-5,
$$

which agrees with the given value of $\det B$.

Therefore, the results are

$$
\det(AB)=-15,\qquad
\det(BA)=-15,\qquad
\det(A^{-1}B)=-\frac53.
$$
