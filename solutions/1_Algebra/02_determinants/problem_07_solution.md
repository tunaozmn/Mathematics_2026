# Exercise 7. Using Properties Instead of Recomputing

## Problem

Suppose that for a $3\times3$ matrix, $\det A=-4$. Compute

$$
\det(2A),\qquad \det(A^T),\qquad \det(A^2),\qquad \det(-A).
$$

Justify each answer using the appropriate property.

> **Why this exercise:** teaches how to use determinant properties instead of repeating a full calculation.

## Method

We use three determinant properties.

For an $n\times n$ matrix, multiplying the entire matrix by a scalar $c$ gives

$$
\det(cA)=c^n\det A.
$$

The exponent is $n$ because all $n$ rows are multiplied by $c$, and each row contributes one factor of $c$.

Taking the transpose preserves the determinant:

$$
\det(A^T)=\det A.
$$

The determinant of a product equals the product of the determinants:

$$
\det(AB)=\det A\det B.
$$

Here, $A$ has size $3\times3$, so we use $n=3$ in the scalar multiplication rule.

## Solution

### 1. Calculate the determinant of 2A

Multiplying $A$ by $2$ multiplies each of its three rows by $2$. Therefore,

$$
\begin{aligned}
\det(2A)
&=2^3\det A\\
&=8\cdot(-4)\\
&=-32.
\end{aligned}
$$

The factor is $2^3$, not just $2$, because the entire matrix is multiplied by $2$.

### 2. Calculate the determinant of the transpose

Transposing a matrix exchanges its rows and columns without changing its determinant. Thus,

$$
\det(A^T)=\det A=-4.
$$

### 3. Calculate the determinant of A squared

The expression $A^2$ means the matrix product $AA$. Using the product property,

$$
\begin{aligned}
\det(A^2)
&=\det(AA)\\
&=\det A\cdot\det A\\
&=(-4)(-4)\\
&=16.
\end{aligned}
$$

### 4. Calculate the determinant of -A

Since $-A=(-1)A$, all three rows are multiplied by $-1$. Hence,

$$
\begin{aligned}
\det(-A)
&=(-1)^3\det A\\
&=(-1)(-4)\\
&=4.
\end{aligned}
$$

There are three sign changes, so the determinant has the opposite sign to $\det A$.

The four results, in the order requested, are

$$
\boxed{-32,\qquad -4,\qquad 16,\qquad 4}.
$$

## Verification

We can check that the scalar multiplication results agree with each other by writing

$$
2A=(-2)(-A).
$$

Using the value $\det(-A)=4$,

$$
\det(2A)=(-2)^3\det(-A)=(-8)\cdot4=-32,
$$

which matches the first result.

The transpose and product properties are also consistent:

$$
\det(A^TA)=\det(A^T)\det A=(-4)(-4)=16.
$$

This equals $\det(A^2)$, as expected from the determinant properties, even though $A^TA$ and $A^2$ need not be the same matrix.
