# Exercise 5. Matrix Times Vector

## Problem

Let

$$
A=
\begin{pmatrix}
2 & -1 \\
1 & 3 \\
\end{pmatrix},\qquad x=
\begin{pmatrix}
4 \\
2 \\
\end{pmatrix}.
$$

Compute $Ax$. Then express $Ax$ as a linear combination of the columns of $A$, with coefficients coming from the vector $x$.

## Method

Matrix $A$ has size $2\times2$, and the column vector $x$ has size $2\times1$. The inner dimensions match, so $Ax$ is defined and has size $2\times1$.

There are two equivalent ways to compute the product:

1. Take the dot product of each row of $A$ with $x$.
2. Multiply each column of $A$ by the corresponding entry of $x$, then add the resulting vectors.

If the columns of $A$ are denoted by $c_1$ and $c_2$, the second method gives

$$
Ax=x_1c_1+x_2c_2.
$$

## Solution

### 1. Compute Ax using rows

The first entry is obtained from the first row of $A$:

$$
2\cdot4+(-1)\cdot2=8-2=6.
$$

The second entry is obtained from the second row of $A$:

$$
1\cdot4+3\cdot2=4+6=10.
$$

Therefore,

$$
Ax=
\begin{pmatrix}
2\cdot4+(-1)\cdot2 \\
1\cdot4+3\cdot2 \\
\end{pmatrix}=
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}.
$$

### 2. Express Ax as a linear combination of columns

The columns of $A$ are

$$
c_1=
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix},\qquad c_2=
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}.
$$

The entries of $x$ are 4 and 2. These become the coefficients of the first and second columns, respectively:

$$
Ax=4c_1+2c_2.
$$

Substituting the columns gives

$$
Ax=4
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
+2
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}.
$$

After scalar multiplication,

$$
Ax=
\begin{pmatrix}
8 \\
4 \\
\end{pmatrix}+
\begin{pmatrix}
-2 \\
6 \\
\end{pmatrix}=
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}.
$$

Thus, multiplying $A$ by $x$ produces a weighted sum of the columns of $A$. The weights are the corresponding entries of $x$.

## Verification

Both methods produce the same vector:

- The row method gives the entries $8-2=6$ and $4+6=10$.
- The column method gives the entries $8+(-2)=6$ and $4+6=10$.

The result has 2 rows and 1 column, matching the expected size $2\times1$.
