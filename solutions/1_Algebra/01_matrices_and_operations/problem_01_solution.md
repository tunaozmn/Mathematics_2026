# Exercise 1. Matrix Size and Entries

## Problem

Given

$$
A=
\begin{pmatrix}
2 & -1 & 3 \\
0 & 4 & 5 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 0 \\
-2 & 3 \\
4 & 1 \\
\end{pmatrix}.
$$

1. State the sizes of matrices $A$ and $B$.
2. Read off the entries $a_{12}$, $a_{23}$, $b_{21}$, and $b_{32}$.
3. Write the second row of $A$ and the first column of $B$ as vectors.

## Method

A matrix with $m$ rows and $n$ columns has size $m\times n$.
The entry $a_{ij}$ is located in row $i$ and column $j$ of matrix $A$.
The same indexing convention applies to matrix $B$.

A row is written as a row vector, and a column is written as a column vector.

## Solution

### 1. Matrix sizes

Matrix $A$ has 2 rows and 3 columns, so its size is $2\times3$.

Matrix $B$ has 3 rows and 2 columns, so its size is $3\times2$.

### 2. Specified entries

- $a_{12}=-1$: the entry in row 1, column 2 of $A$.
- $a_{23}=5$: the entry in row 2, column 3 of $A$.
- $b_{21}=-2$: the entry in row 2, column 1 of $B$.
- $b_{32}=1$: the entry in row 3, column 2 of $B$.

### 3. Row and column vectors

The second row of $A$ is the $1\times3$ row vector

$$
\begin{pmatrix}
0 & 4 & 5 \\
\end{pmatrix}.
$$

The first column of $B$ is the $3\times1$ column vector

$$
\begin{pmatrix}
1 \\
-2 \\
4 \\
\end{pmatrix}.
$$

## Verification

The second row of $A$ contains 3 entries, matching the number of columns of $A$. Its third entry is $5$, consistent with $a_{23}=5$.

The first column of $B$ contains 3 entries, matching the number of rows of $B$. Its second entry is $-2$, consistent with $b_{21}=-2$.

Direct inspection of the original matrices also confirms $a_{12}=-1$ and $b_{32}=1$.
