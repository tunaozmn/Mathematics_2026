# Exercise 3. Vector Normalization

## Problem

For $v=(3,4)$ find a unit vector $e$ with the same direction and orientation. Check that $\|e\|=1$, reconstruct $v$ in the form $v=\|v\|e$, and explain what changes during normalization and what remains unchanged.

> **Why this exercise:** teaches how to separate direction from vector length.

## Method

To normalize a nonzero vector, divide it by its length:

$$
e=\frac{v}{\|v\|}.
$$

This makes the length equal to 1. Since the scaling factor is positive, the resulting vector has the same direction and orientation as the original vector.

Normalization is not defined for the zero vector because its length is zero.

## Solution

### 1. Calculate the length of v

Using the Euclidean length formula,

$$
\begin{aligned}
\|v\|
&=\sqrt{3^2+4^2} \\
&=\sqrt{9+16} \\
&=5.
\end{aligned}
$$

Since $\|v\|\ne0$, the vector can be normalized.

### 2. Divide by the length

Multiply each coordinate by $\frac15$:

$$
\begin{aligned}
e
&=\frac{v}{\|v\|} \\
&=\frac15(3,4) \\
&=\left(\frac35,\frac45\right).
\end{aligned}
$$

Thus, the required unit vector is

$$
e=\left(\frac35,\frac45\right).
$$

### 3. Explain the geometric effect

Normalization changes the length from 5 to 1. Each coordinate is multiplied by the same positive factor, $\frac15$.

The direction remains unchanged because the new vector is a scalar multiple of the original. The orientation also remains unchanged because that scalar is positive: the vector still points the same way.

When drawn from the origin, the endpoints of $v$ and $e$ lie on the same ray. The endpoint of $e$ lies on the unit circle.

## Verification

### 1. Check that e has length 1

$$
\begin{aligned}
\|e\|
&=\sqrt{\left(\frac35\right)^2+\left(\frac45\right)^2} \\
&=\sqrt{\frac9{25}+\frac{16}{25}} \\
&=\sqrt{1} \\
&=1.
\end{aligned}
$$

Therefore, $e$ is a unit vector.

### 2. Reconstruct the original vector

Multiply the unit vector by the original length:

$$
\begin{aligned}
\|v\|e
&=5\left(\frac35,\frac45\right) \\
&=(3,4) \\
&=v.
\end{aligned}
$$

This verifies the decomposition $v=\|v\|e$: the factor $\|v\|$ gives the length, while $e$ gives the direction and orientation.
