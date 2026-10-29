# Exercise 6. Transpose

## Problem

For

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}
$$

compute $A^T$, $B^T$, and $AB$. Then verify in this example that

$$
(AB)^T=B^TA^T.
$$

## Method

The transpose of a matrix is obtained by exchanging its rows and columns. An entry in row $i$, column $j$ moves to row $j$, column $i$.

A matrix of size $m\times n$ therefore has a transpose of size $n\times m$.

Matrix multiplication uses the row-by-column rule. To verify the required identity, compute $AB$ and transpose the result, then independently compute $B^TA^T$ and compare all entries.

## Solution

### 1. Transpose of A

The rows of $A$ become the columns of $A^T$:

$$
A^T=
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 \\
\end{pmatrix}.
$$

Since $A$ has size $2\times3$, its transpose has size $3\times2$.

### 2. Transpose of B

The rows of $B$ become the columns of $B^T$:

$$
B^T=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3 \\
\end{pmatrix}.
$$

Since $B$ has size $3\times2$, its transpose has size $2\times3$.

### 3. Compute AB

The product is defined because the 3 columns of $A$ match the 3 rows of $B$. The result has size $2\times2$.

Applying the row-by-column rule gives

$$
AB=
\begin{pmatrix}
1\cdot1+2\cdot2+3\cdot(-1) & 1\cdot0+2\cdot1+3\cdot3 \\
4\cdot1+5\cdot2+6\cdot(-1) & 4\cdot0+5\cdot1+6\cdot3 \\
\end{pmatrix}.
$$

Simplifying each entry,

$$
AB=
\begin{pmatrix}
1+4-3 & 0+2+9 \\
4+10-6 & 0+5+18 \\
\end{pmatrix}=
\begin{pmatrix}
2 & 11 \\
8 & 23 \\
\end{pmatrix}.
$$

## Verification

### 1. Transpose the product AB

Exchanging the rows and columns of the computed product gives

$$
(AB)^T=
\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}.
$$

The diagonal entries remain unchanged, while the entries 11 and 8 exchange positions.

### 2. Independently compute the product of the transposes

The sizes of $B^T$ and $A^T$ are $2\times3$ and $3\times2$, respectively. Their product is defined and has size $2\times2$.

$$
B^TA^T=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 \\
\end{pmatrix}.
$$

Computing each entry gives

$$
B^TA^T=
\begin{pmatrix}
1\cdot1+2\cdot2+(-1)\cdot3 & 1\cdot4+2\cdot5+(-1)\cdot6 \\
0\cdot1+1\cdot2+3\cdot3 & 0\cdot4+1\cdot5+3\cdot6 \\
\end{pmatrix}.
$$

Therefore,

$$
B^TA^T=
\begin{pmatrix}
1+4-3 & 4+10-6 \\
0+2+9 & 0+5+18 \\
\end{pmatrix}=
\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}.
$$

### 3. Compare the results

Both calculations give the same size and the same entry in every position:

$$
(AB)^T=B^TA^T=
\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}.
$$

This verifies the identity for the given matrices. Transposing a product reverses the order of the factors.

The reversed order is essential: $A^TB^T$ would have size $3\times3$ in this example, whereas $(AB)^T$ has size $2\times2$.
