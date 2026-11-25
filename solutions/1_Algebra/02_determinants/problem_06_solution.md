# Exercise 6. Parameter and Invertibility

## Problem

For

$$
A(t)=
\begin{pmatrix}
t & 1 \\
2 & t \\
\end{pmatrix}
$$

find all values of $t$ for which the matrix is not invertible. Explain how your answer is related to the determinant being zero.

> **Why this exercise:** shows how the determinant can be used to study a family of matrices depending on a parameter.

## Method

A square matrix is not invertible if and only if its determinant is zero.

For a $2\times2$ matrix, we use

$$
\det
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
=ad-bc.
$$

We first express the determinant in terms of $t$. Then we solve the equation $\det A(t)=0$ to find all parameter values for which the inverse does not exist.

## Solution

### 1. Calculate the determinant in terms of t

The diagonal entries are both $t$, while the other two entries are $1$ and $2$. Therefore,

$$
\begin{aligned}
\det A(t)
&=t\cdot t-1\cdot2\\
&=t^2-2.
\end{aligned}
$$

### 2. Find when the determinant is zero

Set the expression equal to zero:

$$
t^2-2=0.
$$

Hence,

$$
t^2=2,
$$

which has two real solutions:

$$
t=\sqrt{2}
\qquad\text{or}\qquad
t=-\sqrt{2}.
$$

Both signs are needed because squaring either value gives $2$.

### 3. State the invertibility conclusion

The determinant is zero exactly at these two values. Thus, $A(t)$ is not invertible precisely when

$$
t=-\sqrt{2}\quad\text{or}\quad t=\sqrt{2}.
$$

For every other real value of $t$, the determinant is nonzero, so $A(t)$ is invertible.

## Verification

Substituting each value into the determinant gives

$$
\det A(\sqrt{2})=(\sqrt{2})^2-2=2-2=0,
$$

and

$$
\det A(-\sqrt{2})=(-\sqrt{2})^2-2=2-2=0.
$$

We can also see why the rows become dependent. Whenever $t^2=2$,

$$
tR_1=t(t,1)=(t^2,t)=(2,t)=R_2.
$$

Thus, at both values found, the second row is a multiple of the first. This agrees with the zero determinant and the absence of an inverse.
