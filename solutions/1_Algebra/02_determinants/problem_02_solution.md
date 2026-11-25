# Exercise 2. Determinant of a 3×3 Matrix

## Problem

For

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
2 & 1 & 5 \\
\end{pmatrix}
$$

compute $\det A$ using Sarrus' rule. Then perform one simple check using a chosen property of the determinant.

> **Why this exercise:** teaches a basic method for $3\times3$ matrices and builds the habit of checking the result without adding a second full solution.

## Method

Sarrus' rule applies to $3\times3$ matrices. We repeat the first two columns to the right of the matrix, then calculate the products along the three downward-right diagonals and the three upward-right diagonals.

The determinant is the sum of the downward-right products minus the sum of the upward-right products.

For a general matrix, this gives

$$
\det
\begin{pmatrix}
a & b & c\\
d & e & f\\
g & h & i
\end{pmatrix}
=(aei+bfg+cdh)-(ceg+bdi+afh).
$$

Each product keeps the signs of its entries. In particular, the sum being subtracted may itself be negative.

## Solution

### 1. Repeat the first two columns

The arrangement used for Sarrus' rule is

$$
\begin{array}{ccc|cc}
1 & 2 & -1 & 1 & 2\\
0 & 3 & 4 & 0 & 3\\
2 & 1 & 5 & 2 & 1
\end{array}.
$$

The two additional columns are only a calculation aid; they do not change the size of the original matrix.

### 2. Calculate the downward-right products

The three products are

$$
1\cdot3\cdot5=15,
$$

$$
2\cdot4\cdot2=16,
$$

$$
(-1)\cdot0\cdot1=0.
$$

Their sum is

$$
15+16+0=31.
$$

### 3. Calculate the upward-right products

The three products are

$$
2\cdot3\cdot(-1)=-6,
$$

$$
1\cdot4\cdot1=4,
$$

$$
5\cdot0\cdot2=0.
$$

Their sum is

$$
-6+4+0=-2.
$$

### 4. Subtract the two sums

Therefore,

$$
\begin{aligned}
\det A
&=(15+16+0)-(-6+4+0)\\
&=31-(-2)\\
&=33.
\end{aligned}
$$

Thus, the determinant of $A$ is $33$.

## Verification

Adding a multiple of one row to another leaves the determinant unchanged. We can use this property to obtain an upper triangular matrix.

First, apply $R_3\leftarrow R_3-2R_1$:

$$
\begin{pmatrix}
1 & 2 & -1\\
0 & 3 & 4\\
2 & 1 & 5
\end{pmatrix}
\longrightarrow
\begin{pmatrix}
1 & 2 & -1\\
0 & 3 & 4\\
0 & -3 & 7
\end{pmatrix}.
$$

Next, apply $R_3\leftarrow R_3+R_2$:

$$
\begin{pmatrix}
1 & 2 & -1\\
0 & 3 & 4\\
0 & -3 & 7
\end{pmatrix}
\longrightarrow
\begin{pmatrix}
1 & 2 & -1\\
0 & 3 & 4\\
0 & 0 & 11
\end{pmatrix}.
$$

The determinant of a triangular matrix is the product of its diagonal entries. Since neither operation changed the determinant,

$$
\det A=1\cdot3\cdot11=33.
$$

This agrees with the result obtained using Sarrus' rule.
