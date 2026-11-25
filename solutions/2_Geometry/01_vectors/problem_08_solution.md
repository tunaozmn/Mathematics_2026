# Exercise 8. Linear Combination and Checking the Result

## Problem

Check whether $w=(5,1)$ can be written as

$$
w=au+bv,
$$

where $u=(1,1)$ and $v=(2,-1)$. If so, find $a,b$, reconstruct $w$ from them, and explain the geometric meaning of the existence of such coefficients.

> **Why this exercise:** connects linear combinations with the geometry of directions.

## Method

We expand $au+bv$ coordinate by coordinate and equate the result to $w$. This gives a linear system for the coefficients $a,b$.

If the system has a solution, then $w$ is a linear combination of $u$ and $v$. We check the coefficients by substituting them back into the vector expression.

## Solution

### 1. Translate the vector equation into a system

Expand the proposed combination:

$$
\begin{aligned}
au+bv
&=a(1,1)+b(2,-1) \\
&=(a,a)+(2b,-b) \\
&=(a+2b,a-b).
\end{aligned}
$$

For this vector to equal $w=(5,1)$, corresponding coordinates must agree:

$$
\begin{cases}
a+2b=5, \\
a-b=1.
\end{cases}
$$

### 2. Solve for the coefficients

Subtract the second equation from the first:

$$
\begin{aligned}
(a+2b)-(a-b)&=5-1, \\
3b&=4, \\
b&=\frac43.
\end{aligned}
$$

Substitute into $a-b=1$:

$$
\begin{aligned}
a&=1+b \\
&=1+\frac43 \\
&=\frac73.
\end{aligned}
$$

Therefore, the required representation exists and is

$$
w=\frac73u+\frac43v.
$$

### 3. Explain the geometric meaning

The vectors $u$ and $v$ are not parallel. If $v=cu$, its first coordinate would require $c=2$, while its second coordinate would require $c=-1$. No single scalar satisfies both conditions.

Thus, $u$ and $v$ provide two independent directions in the plane. Their linear combinations can reach every vector in $\mathbb{R}^2$, and each representation is unique.

For this particular vector, move by $\frac73u$ and then by $\frac43v$. The combined displacement is $w=(5,1)$.

Both coefficients are positive, so both scaled vectors retain the orientations of their original vectors.

## Verification

Compute the two scaled vectors:

$$
\frac73u=\left(\frac73,\frac73\right),
\qquad
\frac43v=\left(\frac83,-\frac43\right).
$$

Add them:

$$
\begin{aligned}
\frac73u+\frac43v
&=\left(\frac73+\frac83,\;\frac73-\frac43\right) \\
&=\left(\frac{15}{3},\frac33\right) \\
&=(5,1) \\
&=w.
\end{aligned}
$$

This reconstructs the given vector exactly, confirming that $a=\frac73$ and $b=\frac43$.
