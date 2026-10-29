# Problem 7 — Identity Matrix, Zero Matrix, and Powers

## Problem

Given the matrix

$$
A=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix},
$$

compute $AI$, $IA$, $A+0$, $A^2$, and $A^3$. Explain the roles of the identity matrix and the zero matrix, and describe the pattern in successive powers of $A$.

## Method

The identity matrix and the zero matrix must have size $2 \times 2$:

$$
I=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix},
\qquad
0=
\begin{pmatrix}
0 & 0 \\
0 & 0 \\
\end{pmatrix}.
$$

Multiplying a matrix by the identity matrix leaves it unchanged. Adding the zero matrix also leaves it unchanged.

Matrix powers are calculated using matrix multiplication:

$$
A^2=AA,
\qquad
A^3=A^2A.
$$

Each entry of a product is obtained by multiplying the corresponding row of the first matrix by the corresponding column of the second matrix and adding the results.

## Solution

### 1. Multiplication by the identity matrix

Multiplying on the right gives

$$
AI=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}=A.
$$

Multiplying on the left gives

$$
IA=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}=A.
$$

Thus, the identity matrix is a neutral element for matrix multiplication.

### 2. Addition of the zero matrix

Matrix addition is performed entry by entry:

$$
A+0=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}+
\begin{pmatrix}
0 & 0 \\
0 & 0 \\
\end{pmatrix}=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}=A.
$$

The zero matrix is a neutral element for matrix addition.

### 3. The square of A

$$
A^2=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}=
\begin{pmatrix}
2\cdot2+1\cdot0 & 2\cdot1+1\cdot2 \\
0\cdot2+2\cdot0 & 0\cdot1+2\cdot2 \\
\end{pmatrix}=
\begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}.
$$

### 4. The cube of A

$$
A^3=A^2A=
\begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}=
\begin{pmatrix}
4\cdot2+4\cdot0 & 4\cdot1+4\cdot2 \\
0\cdot2+4\cdot0 & 0\cdot1+4\cdot2 \\
\end{pmatrix}=
\begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}.
$$

### 5. Pattern in successive powers

The first three powers are

$$
A=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix},
\qquad
A^2=
\begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix},
\qquad
A^3=
\begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}.
$$

The diagonal entries are powers of 2, and the lower-left entry remains zero. The upper-right entry in the nth power is $n2^{n-1}$.

For every integer $n\geq1$, the general formula is

$$
A^n=
\begin{pmatrix}
2^n & n2^{n-1} \\
0 & 2^n \\
\end{pmatrix}.
$$

## Verification of the Pattern

For $n=1$, the formula gives the original matrix $A$.

Assume the formula holds for some integer $n\geq1$. Multiplying by $A$ gives

$$
A^{n+1}=A^nA=
\begin{pmatrix}
2^n & n2^{n-1} \\
0 & 2^n \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}=
\begin{pmatrix}
2^{n+1} & 2^n+n2^n \\
0 & 2^{n+1} \\
\end{pmatrix}=
\begin{pmatrix}
2^{n+1} & (n+1)2^n \\
0 & 2^{n+1} \\
\end{pmatrix}.
$$

This is the same formula with $n$ replaced by $n+1$. Therefore, the pattern holds for all integers $n\geq1$ by mathematical induction.
