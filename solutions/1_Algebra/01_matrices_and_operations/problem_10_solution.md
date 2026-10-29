# Problem 10 — Columns of a Matrix Product

## Problem

Given the matrices

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},
\qquad
B=
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix},
$$

denote the columns of $B$ by $b_1$ and $b_2$.

Compute the product of $A$ with each column, calculate $AB$, and explain why the columns of $AB$ are exactly these two matrix-vector products.

## Method

The matrix $A$ has size $2\times3$, and $B$ has size $3\times2$. Their product is therefore defined and has size $2\times2$.

Each column of $B$ has size $3\times1$. Multiplication by $A$ produces a column of size $2\times1$.

Matrix multiplication can be performed one column at a time:

$$
B=
\begin{pmatrix}
b_1 & b_2 \\
\end{pmatrix}
\quad\Longrightarrow\quad
AB=
\begin{pmatrix}
Ab_1 & Ab_2 \\
\end{pmatrix}.
$$

## Solution

### 1. Identify the columns of B

$$
b_1=
\begin{pmatrix}
1 \\
-1 \\
3 \\
\end{pmatrix},
\qquad
b_2=
\begin{pmatrix}
2 \\
0 \\
1 \\
\end{pmatrix}.
$$

### 2. Multiply A by the first column

$$
Ab_1=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 \\
-1 \\
3 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot1+2\cdot(-1)+0\cdot3 \\
0\cdot1+1\cdot(-1)+1\cdot3 \\
\end{pmatrix}=
\begin{pmatrix}
-1 \\
2 \\
\end{pmatrix}.
$$

### 3. Multiply A by the second column

$$
Ab_2=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 \\
0 \\
1 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot2+2\cdot0+0\cdot1 \\
0\cdot2+1\cdot0+1\cdot1 \\
\end{pmatrix}=
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}.
$$

### 4. Compute the matrix product

Using row-by-column multiplication,

$$
AB=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot1+2\cdot(-1)+0\cdot3 & 1\cdot2+2\cdot0+0\cdot1 \\
0\cdot1+1\cdot(-1)+1\cdot3 & 0\cdot2+1\cdot0+1\cdot1 \\
\end{pmatrix}=
\begin{pmatrix}
-1 & 2 \\
2 & 1 \\
\end{pmatrix}.
$$

### 5. Explain the column relationship

The first column of $AB$ is obtained by multiplying every row of $A$ by the first column of $B$. These are exactly the calculations used to obtain $Ab_1$.

Similarly, the second column of $AB$ is obtained by multiplying every row of $A$ by the second column of $B$. These calculations produce $Ab_2$.

Therefore,

$$
AB=
\begin{pmatrix}
Ab_1 & Ab_2 \\
\end{pmatrix}=
\begin{pmatrix}
-1 & 2 \\
2 & 1 \\
\end{pmatrix}.
$$

## Verification

The matrix-vector products can also be checked using linear combinations of the columns of $A$.

For the first column of $B$, the coefficients are 1, -1, and 3:

$$
Ab_1=
\begin{pmatrix}
1 \\
0 \\
\end{pmatrix}-
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}+
3\begin{pmatrix}
0 \\
1 \\
\end{pmatrix}=
\begin{pmatrix}
-1 \\
2 \\
\end{pmatrix}.
$$

For the second column of $B$, the coefficients are 2, 0, and 1:

$$
Ab_2=
2\begin{pmatrix}
1 \\
0 \\
\end{pmatrix}+
0\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}+
\begin{pmatrix}
0 \\
1 \\
\end{pmatrix}=
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}.
$$

Both results agree with the corresponding columns of $AB$.
