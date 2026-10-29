# Exercise 2. Addition and Scalar Multiplication

## Problem

For

$$
A=
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
4 & -2 \\
0 & 5 \\
\end{pmatrix}
$$

compute

$$
A+B,\qquad A-B,\qquad 3A-2B.
$$

Explain why matrix addition is possible only for matrices of the same size.

## Method

Matrix addition and subtraction are performed entry by entry: entries in the same row and column are added or subtracted.

Scalar multiplication multiplies every entry of a matrix by the scalar.

For each position $(i,j)$, the corresponding entries of the results are

$$
(A+B)_{ij}=a_{ij}+b_{ij},\qquad
(A-B)_{ij}=a_{ij}-b_{ij},\qquad
(3A-2B)_{ij}=3a_{ij}-2b_{ij}.
$$

Both given matrices have size $2\times2$, so these operations are defined.

## Solution

### 1. Addition

Adding corresponding entries gives

$$
A+B=
\begin{pmatrix}
1+4 & 2+(-2) \\
-1+0 & 3+5 \\
\end{pmatrix}=
\begin{pmatrix}
5 & 0 \\
-1 & 8 \\
\end{pmatrix}.
$$

### 2. Subtraction

Subtracting each entry of $B$ from the corresponding entry of $A$ gives

$$
A-B=
\begin{pmatrix}
1-4 & 2-(-2) \\
-1-0 & 3-5 \\
\end{pmatrix}=
\begin{pmatrix}
-3 & 4 \\
-1 & -2 \\
\end{pmatrix}.
$$

In particular, subtracting a negative entry changes the sign: $2-(-2)=2+2=4$.

### 3. Scalar multiplication and subtraction

Multiplying every entry of $A$ by 3 gives

$$
3A=
\begin{pmatrix}
3 & 6 \\
-3 & 9 \\
\end{pmatrix}.
$$

Multiplying every entry of $B$ by 2 gives

$$
2B=
\begin{pmatrix}
8 & -4 \\
0 & 10 \\
\end{pmatrix}.
$$

Therefore,

$$
3A-2B=
\begin{pmatrix}
3-8 & 6-(-4) \\
-3-0 & 9-10 \\
\end{pmatrix}=
\begin{pmatrix}
-5 & 10 \\
-3 & -1 \\
\end{pmatrix}.
$$

### 4. Why equal sizes are required

Matrix addition pairs every entry of one matrix with the entry in the same position in the other matrix.

The matrices must therefore have the same number of rows and the same number of columns. Otherwise, some positions would have no corresponding entry, so ordinary matrix addition would not be defined.

Having the same total number of entries is not sufficient. For example, a $2\times3$ matrix and a $3\times2$ matrix cannot be added.

## Verification

The results can be checked by reversing the operations.

Subtracting $B$ from the computed sum recovers $A$:

$$
\begin{pmatrix}
5 & 0 \\
-1 & 8 \\
\end{pmatrix}-
\begin{pmatrix}
4 & -2 \\
0 & 5 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix}=A.
$$

Adding $B$ to the computed difference also recovers $A$:

$$
\begin{pmatrix}
-3 & 4 \\
-1 & -2 \\
\end{pmatrix}+
\begin{pmatrix}
4 & -2 \\
0 & 5 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix}=A.
$$

Adding $2B$ to the computed value of $3A-2B$ recovers $3A$:

$$
\begin{pmatrix}
-5 & 10 \\
-3 & -1 \\
\end{pmatrix}+
\begin{pmatrix}
8 & -4 \\
0 & 10 \\
\end{pmatrix}=
\begin{pmatrix}
3 & 6 \\
-3 & 9 \\
\end{pmatrix}=3A.
$$

All three results have size $2\times2$, as expected.
