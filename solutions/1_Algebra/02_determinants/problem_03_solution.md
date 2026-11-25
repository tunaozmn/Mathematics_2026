# Exercise 3. Swapping Two Rows

## Problem

For

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 3 & 1 \\
2 & 1 & 1 \\
\end{pmatrix}
$$

compute $\det A$. Then form a matrix $B$ by swapping the first and second rows of $A$.

First predict $\det B$ using a determinant property, and then verify your prediction by calculation.

> **Why this exercise:** gives a second classical calculation with a $3\times3$ determinant while teaching the precise effect of a row swap on the sign of the determinant.

## Method

We calculate $\det A$ by expanding along the first row. For a general $3\times3$ matrix,

$$
M=
\begin{pmatrix}
a & b & c \\
d & e & f \\
g & h & i
\end{pmatrix},
$$

the expansion is

$$
\det M=a(ei-fh)-b(di-fg)+c(dh-eg).
$$

Each expression in parentheses is the determinant of the $2\times2$ matrix obtained by removing the corresponding entry's row and column. The signs of the three terms are $+$, $-$, and $+$.

The first row of $A$ contains a zero, so its third term contributes nothing.

We then use the row-swap property: exchanging two rows multiplies the determinant by $-1$. Since $B$ is obtained by one row swap,

$$
\det B=-\det A.
$$

## Solution

### 1. Calculate the determinant of A

Expanding along the first row,

$$
\begin{aligned}
\det A
&=1\det\begin{pmatrix}
3&1\\
1&1
\end{pmatrix}
-2\det\begin{pmatrix}
0&1\\
2&1
\end{pmatrix}.
\end{aligned}
$$

The two smaller determinants are

$$
\det\begin{pmatrix}
3&1\\
1&1
\end{pmatrix}
=3\cdot1-1\cdot1=2,
$$

and

$$
\det\begin{pmatrix}
0&1\\
2&1
\end{pmatrix}
=0\cdot1-1\cdot2=-2.
$$

Therefore,

$$
\begin{aligned}
\det A
&=1\cdot2-2\cdot(-2)\\
&=2+4\\
&=6.
\end{aligned}
$$

### 2. Form B by swapping the first two rows

Apply $R_1\leftrightarrow R_2$:

$$
A=
\begin{pmatrix}
1&2&0\\
0&3&1\\
2&1&1
\end{pmatrix}
\quad\longrightarrow\quad
B=
\begin{pmatrix}
0&3&1\\
1&2&0\\
2&1&1
\end{pmatrix}.
$$

The third row remains unchanged.

### 3. Predict the determinant of B

A single row swap reverses the sign of the determinant. Hence,

$$
\det B=-\det A=-6.
$$

The predicted determinant of $B$ is therefore $-6$.

## Verification

Calculate $\det B$ directly by expanding along its first row. The first entry is zero, so only the second and third terms remain:

$$
\begin{aligned}
\det B
&=-3\det\begin{pmatrix}
1&0\\
2&1
\end{pmatrix}
+1\det\begin{pmatrix}
1&2\\
2&1
\end{pmatrix}.
\end{aligned}
$$

Evaluating these determinants gives

$$
\begin{aligned}
\det B
&=-3(1\cdot1-0\cdot2)+1(1\cdot1-2\cdot2)\\
&=-3(1)+(1-4)\\
&=-3-3\\
&=-6.
\end{aligned}
$$

This agrees with the prediction:

$$
\det A=6,\qquad \det B=-6.
$$

The row swap changed the sign of the determinant while preserving its absolute value.
