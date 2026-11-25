# Exercise 12. Finding Inverses Without Starting from Scratch

## Problem

It is known that

$$
A^{-1}=
\begin{pmatrix}
2 & -1 \\
-3 & 2
\end{pmatrix}.
$$

Without finding $A$, compute $(3A)^{-1}$, $(A^T)^{-1}$, and $(A^2)^{-1}$. Justify each result using the appropriate property.

> **Why this exercise:** teaches how to use inverse properties instead of carrying out unnecessary full calculations.

## Method

We use three properties of inverse matrices:

1. For a nonzero scalar $c$, $(cA)^{-1}=\frac1c A^{-1}$.
2. The inverse of a transpose is the transpose of the inverse: $(A^T)^{-1}=(A^{-1})^T$.
3. The inverse of a product reverses the order: $(AB)^{-1}=B^{-1}A^{-1}$. In particular, $(A^2)^{-1}=A^{-1}A^{-1}$.
Each property lets us work directly with the given matrix $A^{-1}$.

## Solution

### 1. Find the inverse of 3A

Multiplying $A$ by 3 is undone by multiplying its inverse by $\frac13$. Therefore,

$$
\begin{aligned}
(3A)^{-1}
&=\frac13 A^{-1} \\
&=\frac13
\begin{pmatrix}
2 & -1 \\
-3 & 2
\end{pmatrix} \\
&=
\begin{pmatrix}
\frac23 & -\frac13 \\
-1 & \frac23
\end{pmatrix}.
\end{aligned}
$$

The scalar $\frac13$ multiplies every entry of the inverse.

### 2. Find the inverse of the transpose

Using $(A^T)^{-1}=(A^{-1})^T$, transpose the given inverse by interchanging its rows and columns:

$$
\begin{aligned}
(A^T)^{-1}
&=(A^{-1})^T \\
&=
\begin{pmatrix}
2 & -3 \\
-1 & 2
\end{pmatrix}.
\end{aligned}
$$

### 3. Find the inverse of the square

Apply the inverse-of-a-product property to $A^2=AA$:

$$
(A^2)^{-1}=A^{-1}A^{-1}.
$$

Thus, we multiply the given inverse by itself:

$$
\begin{aligned}
(A^2)^{-1}
&=
\begin{pmatrix}
2 & -1 \\
-3 & 2
\end{pmatrix}
\begin{pmatrix}
2 & -1 \\
-3 & 2
\end{pmatrix} \\
&=
\begin{pmatrix}
2\cdot2+(-1)\cdot(-3) & 2\cdot(-1)+(-1)\cdot2 \\
(-3)\cdot2+2\cdot(-3) & (-3)\cdot(-1)+2\cdot2
\end{pmatrix} \\
&=
\begin{pmatrix}
4+3 & -2-2 \\
-6-6 & 3+4
\end{pmatrix} \\
&=
\begin{pmatrix}
7 & -4 \\
-12 & 7
\end{pmatrix}.
\end{aligned}
$$

The square here is a matrix product, not the square of each individual entry.

## Verification

Let $C=A^{-1}$. By definition,

$$
AC=CA=I.
$$

We can verify all three constructions without finding $A$.

For the scalar multiple,

$$
(3A)\left(\frac13 C\right)=AC=I,
\qquad
\left(\frac13 C\right)(3A)=CA=I.
$$

For the transpose, use the fact that transposing a product reverses its order:

$$
A^TC^T=(CA)^T=I,
\qquad
C^TA^T=(AC)^T=I.
$$

For the square, use associativity:

$$
\begin{aligned}
A^2C^2
&=A(AC)C \\
&=AIC \\
&=AC \\
&=I.
\end{aligned}
$$

Similarly,

$$
\begin{aligned}
C^2A^2
&=C(CA)A \\
&=CIA \\
&=CA \\
&=I.
\end{aligned}
$$

These identities confirm all three inverses using only the given inverse and its defining properties.
