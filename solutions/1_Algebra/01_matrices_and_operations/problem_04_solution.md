# Exercise 4. Matrix Multiplication and Noncommutativity

## Problem

For

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
$$

compute $AB$ and $BA$. Is $AB=BA$? Use this example to explain what noncommutativity of matrix multiplication means.

## Method

Both matrices have size $2\times2$, so both products are defined and have size $2\times2$.

To obtain the entry in row $i$ and column $j$ of a product, multiply the entries of row $i$ of the first matrix by the corresponding entries of column $j$ of the second matrix, then add.

For these matrices,

$$
(AB)_{ij}=a_{i1}b_{1j}+a_{i2}b_{2j}.
$$

For $BA$, the order of the factors is reversed:

$$
(BA)_{ij}=b_{i1}a_{1j}+b_{i2}a_{2j}.
$$

## Solution

### 1. Compute AB

Applying the row-by-column rule to all four entries gives

$$
AB=
\begin{pmatrix}
1\cdot2+2\cdot3 & 1\cdot0+2\cdot1 \\
0\cdot2+1\cdot3 & 0\cdot0+1\cdot1 \\
\end{pmatrix}=
\begin{pmatrix}
8 & 2 \\
3 & 1 \\
\end{pmatrix}.
$$

For example, the upper-left entry is obtained from the first row of $A$ and the first column of $B$: $1\cdot2+2\cdot3=8$.

### 2. Compute BA

Reversing the order gives

$$
BA=
\begin{pmatrix}
2\cdot1+0\cdot0 & 2\cdot2+0\cdot1 \\
3\cdot1+1\cdot0 & 3\cdot2+1\cdot1 \\
\end{pmatrix}=
\begin{pmatrix}
2 & 4 \\
3 & 7 \\
\end{pmatrix}.
$$

For example, the upper-left entry now comes from the first row of $B$ and the first column of $A$: $2\cdot1+0\cdot0=2$.

### 3. Compare the products

The results are

$$
AB=
\begin{pmatrix}
8 & 2 \\
3 & 1 \\
\end{pmatrix},\qquad BA=
\begin{pmatrix}
2 & 4 \\
3 & 7 \\
\end{pmatrix}.
$$

Two matrices are equal only if they have the same size and all corresponding entries are equal.

Here, the entry in row 1, column 1 is 8 in $AB$ and 2 in $BA$. Therefore,

$$
AB\neq BA.
$$

Matrix multiplication is noncommutative: changing the order of the factors can change the result, even when both products are defined.

This does not mean that $AB$ and $BA$ are always different. Some pairs of matrices commute, but equality is not a general rule.

## Verification

The products can also be checked using linear combinations of rows.

### Check AB

The first row of $A$ is $(1,2)$, so the first row of $AB$ is the first row of $B$ plus twice its second row:

$$
\begin{pmatrix}
2 & 0 \\
\end{pmatrix}
+2
\begin{pmatrix}
3 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
8 & 2 \\
\end{pmatrix}.
$$

The second row of $A$ is $(0,1)$, so the second row of $AB$ equals the second row of $B$, namely $(3,1)$.

These rows agree with the computed product $AB$.

### Check BA

The first row of $B$ is $(2,0)$, so the first row of $BA$ is twice the first row of $A$, namely $(2,4)$.

The second row of $B$ is $(3,1)$, so the second row of $BA$ is three times the first row of $A$ plus its second row:

$$
3
\begin{pmatrix}
1 & 2 \\
\end{pmatrix}+
\begin{pmatrix}
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
3 & 7 \\
\end{pmatrix}.
$$

These rows agree with the computed product $BA$.
