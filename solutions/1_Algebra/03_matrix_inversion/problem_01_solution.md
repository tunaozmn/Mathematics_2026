# Exercise 1. Definition of the Inverse

## Problem

For

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 1
\end{pmatrix},
\qquad
B=
\begin{pmatrix}
1 & -1 \\
-1 & 2
\end{pmatrix}
$$

check, without using a formula, whether $B=A^{-1}$. Compute $AB$ and $BA$ and relate the result to the definition of the inverse.

> **Why this exercise:** starts from the definition of the inverse through multiplication before any formulas or computational methods are introduced.

## Method

By definition, a matrix $B$ is the inverse of a square matrix $A$ when

$$
AB=BA=I,
$$

where $I$ is the identity matrix of the same size.

For these $2\times2$ matrices,

$$
I=
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}.
$$

We calculate both products using row-by-column multiplication. Each entry is the sum of the products of corresponding entries from a row of the first matrix and a column of the second.

## Solution

### 1. Calculate AB

Multiply each row of $A$ by each column of $B$:

$$
AB=
\begin{pmatrix}
2\cdot1+1\cdot(-1) & 2\cdot(-1)+1\cdot2 \\
1\cdot1+1\cdot(-1) & 1\cdot(-1)+1\cdot2
\end{pmatrix}.
$$

Simplifying the entries gives

$$
\begin{aligned}
AB&=
\begin{pmatrix}
2-1 & -2+2 \\
1-1 & -1+2
\end{pmatrix}\\
&=
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}\\
&=I.
\end{aligned}
$$

Thus, multiplying $A$ by $B$ on the right produces the identity matrix.

### 2. Calculate BA

Now multiply in the reverse order:

$$
BA=
\begin{pmatrix}
1\cdot2+(-1)\cdot1 & 1\cdot1+(-1)\cdot1 \\
(-1)\cdot2+2\cdot1 & (-1)\cdot1+2\cdot1
\end{pmatrix}.
$$

Simplifying gives

$$
\begin{aligned}
BA&=
\begin{pmatrix}
2-1 & 1-1 \\
-2+2 & -1+2
\end{pmatrix}\\
&=
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}\\
&=I.
\end{aligned}
$$

Multiplying $A$ by $B$ on the left also produces the identity matrix.

### 3. Apply the definition of the inverse

Both required products equal the identity:

$$
AB=BA=I.
$$

Therefore, $B$ is the inverse of $A$:

$$
A^{-1}=B=
\begin{pmatrix}
1 & -1 \\
-1 & 2
\end{pmatrix}.
$$

This conclusion follows directly from the definition, without using an inverse formula.

## Verification

We can also illustrate how $B$ undoes the action of $A$ on a vector. Take

$$
x=
\begin{pmatrix}
1 \\
2
\end{pmatrix}.
$$

Applying $A$ gives

$$
\begin{aligned}
Ax&=
\begin{pmatrix}
2\cdot1+1\cdot2 \\
1\cdot1+1\cdot2
\end{pmatrix}\\
&=
\begin{pmatrix}
4 \\
3
\end{pmatrix}.
\end{aligned}
$$

Applying $B$ to this result gives

$$
\begin{aligned}
B(Ax)&=
\begin{pmatrix}
1\cdot4+(-1)\cdot3 \\
(-1)\cdot4+2\cdot3
\end{pmatrix}\\
&=
\begin{pmatrix}
1 \\
2
\end{pmatrix}\\
&=x.
\end{aligned}
$$

The original vector is recovered. This illustrates the inverse relationship; the complete verification for all vectors is provided by the matrix identities $AB=BA=I$ above.
