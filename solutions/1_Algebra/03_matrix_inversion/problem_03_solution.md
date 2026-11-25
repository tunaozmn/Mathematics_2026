# Exercise 3. When Does the Inverse Not Exist?

## Problem

For

$$
A=
\begin{pmatrix}
2 & 4 \\
1 & 2
\end{pmatrix}
$$

explain in two ways why $A^{-1}$ does not exist: using the determinant and using dependence between the rows.

> **Why this exercise:** connects two signs of noninvertibility instead of treating them as unrelated facts.

## Method

A square matrix is invertible if and only if its determinant is nonzero. For a $2\times2$ matrix, we calculate the determinant using

$$
\det
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
=ad-bc.
$$

We can also examine its rows. If one row is a multiple of another, the rows are linearly dependent, so the matrix is not invertible.

These criteria describe the same underlying issue: the matrix does not preserve enough independent information for its action to be reversed uniquely.

## Solution

### 1. Use the determinant

Calculate

$$
\begin{aligned}
\det A
&=2\cdot2-4\cdot1\\
&=4-4\\
&=0.
\end{aligned}
$$

Since the determinant is zero, $A$ is not invertible. Therefore, $A^{-1}$ does not exist.

### 2. Identify the dependence between the rows

The rows are

$$
R_1=(2,4),
\qquad
R_2=(1,2).
$$

The first row is twice the second:

$$
R_1=2R_2.
$$

Equivalently,

$$
R_1-2R_2=(0,0).
$$

This is a nontrivial linear relation between the rows, so they are linearly dependent.

An invertible matrix must have linearly independent rows. Thus, the row dependence also shows that $A^{-1}$ does not exist.

### 3. Connect the two explanations

Apply the row operation

$$
R_1\leftarrow R_1-2R_2.
$$

The resulting matrix is

$$
\begin{pmatrix}
0 & 0 \\
1 & 2
\end{pmatrix}.
$$

Subtracting a multiple of another row preserves the determinant. The resulting zero row makes the determinant zero.

Thus, the dependence between the original rows explains why the determinant calculation gave zero.

## Verification

We can confirm noninvertibility by finding a nonzero vector that $A$ maps to zero.

Take

$$
x=
\begin{pmatrix}
-2 \\
1
\end{pmatrix}.
$$

Then

$$
\begin{aligned}
Ax&=
\begin{pmatrix}
2\cdot(-2)+4\cdot1 \\
1\cdot(-2)+2\cdot1
\end{pmatrix}\\
&=
\begin{pmatrix}
-4+4 \\
-2+2
\end{pmatrix}\\
&=
\begin{pmatrix}
0 \\
0
\end{pmatrix}.
\end{aligned}
$$

If $A^{-1}$ existed, multiplying $Ax=0$ by $A^{-1}$ would give $x=0$. However, our chosen vector is nonzero.

This confirms that $A$ has no inverse, consistently with both the zero determinant and the dependent rows.
