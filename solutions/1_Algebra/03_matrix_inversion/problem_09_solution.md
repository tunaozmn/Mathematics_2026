# Exercise 9. Matrix Equation

## Problem

Given

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1
\end{pmatrix},\qquad B=
\begin{pmatrix}
3 & 1 \\
2 & 4
\end{pmatrix}.
$$

Solve the equation $AX=B$ for $X$. Before calculating, decide on which side of the equation $A^{-1}$ must be used. Then check the result by computing $AX$.

> **Why this exercise:** teaches that order matters in matrix equations and must guide the solution.

## Method

Since $A$ multiplies $X$ on the left, we multiply both sides of the equation on the left by $A^{-1}$:

$$
A^{-1}(AX)=A^{-1}B.
$$

By associativity and the identity $A^{-1}A=I$, we obtain

$$
(A^{-1}A)X=IX=X=A^{-1}B.
$$

The order matters because matrix multiplication is generally not commutative. Multiplying on the right would give $AXA^{-1}=BA^{-1}$, which does not isolate $X$.

We therefore find $A^{-1}$, compute $A^{-1}B$, and check the result in the original equation.

## Solution

### 1. Check that A is invertible

The determinant is

$$
\det A=1\cdot1-2\cdot0=1.
$$

Since the determinant is nonzero, $A$ is invertible. Consequently, the equation has the unique solution $X=A^{-1}B$.

### 2. Find the inverse of A

Using the inverse formula for a $2\times2$ matrix,

$$
\begin{aligned}
A^{-1}
&=\frac{1}{1}
\begin{pmatrix}
1 & -2 \\
0 & 1
\end{pmatrix} \\
&=
\begin{pmatrix}
1 & -2 \\
0 & 1
\end{pmatrix}.
\end{aligned}
$$

### 3. Compute X in the correct order

Multiply $A^{-1}$ by $B$:

$$
X=A^{-1}B=
\begin{pmatrix}
1 & -2 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
3 & 1 \\
2 & 4
\end{pmatrix}.
$$

Using row-by-column multiplication,

$$
\begin{aligned}
X
&=
\begin{pmatrix}
1\cdot3+(-2)\cdot2 & 1\cdot1+(-2)\cdot4 \\
0\cdot3+1\cdot2 & 0\cdot1+1\cdot4
\end{pmatrix} \\
&=
\begin{pmatrix}
3-4 & 1-8 \\
2 & 4
\end{pmatrix} \\
&=
\begin{pmatrix}
-1 & -7 \\
2 & 4
\end{pmatrix}.
\end{aligned}
$$

Thus, the solution is

$$
X=
\begin{pmatrix}
-1 & -7 \\
2 & 4
\end{pmatrix}.
$$

## Verification

Substitute the resulting matrix into $AX$:

$$
AX=
\begin{pmatrix}
1 & 2 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
-1 & -7 \\
2 & 4
\end{pmatrix}.
$$

Calculating the entries gives

$$
\begin{aligned}
AX
&=
\begin{pmatrix}
1\cdot(-1)+2\cdot2 & 1\cdot(-7)+2\cdot4 \\
0\cdot(-1)+1\cdot2 & 0\cdot(-7)+1\cdot4
\end{pmatrix} \\
&=
\begin{pmatrix}
-1+4 & -7+8 \\
2 & 4
\end{pmatrix} \\
&=
\begin{pmatrix}
3 & 1 \\
2 & 4
\end{pmatrix} \\
&=B.
\end{aligned}
$$

The product equals the given matrix $B$, confirming that $X=A^{-1}B$ solves the equation.
