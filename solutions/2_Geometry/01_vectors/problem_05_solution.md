# Exercise 5. Angle Between Vectors

## Problem

Given $u=(1,1,0)$ and $v=(1,0,1)$:

1. Use the sign of $u\cdot v$ to predict the type of angle.
2. Compute the angle.
3. Compare the result with the prediction.

> **Why this exercise:** teaches how to extract qualitative information first and only then perform the exact calculation.

## Method

For two nonzero vectors,

$$
u\cdot v=\|u\|\,\|v\|\cos\theta,
$$

where $0\le\theta\le\pi$ is the angle between them.

Since both lengths are positive, the sign of the dot product matches the sign of $\cos\theta$. A positive dot product indicates an angle less than $90^\circ$, a zero dot product indicates a right angle, and a negative dot product indicates an angle greater than $90^\circ$.

After predicting the angle type, we calculate

$$
\cos\theta=\frac{u\cdot v}{\|u\|\,\|v\|}.
$$

## Solution

### 1. Use the dot product to predict the angle type

Compute the dot product:

$$
\begin{aligned}
u\cdot v
&=1\cdot1+1\cdot0+0\cdot1 \\
&=1.
\end{aligned}
$$

The dot product is positive, so the angle is less than $90^\circ$.

The vectors are not scalar multiples of each other, so the angle is not zero. Therefore, we predict an acute angle.

### 2. Calculate the lengths

For $u$,

$$
\begin{aligned}
\|u\|
&=\sqrt{1^2+1^2+0^2} \\
&=\sqrt2.
\end{aligned}
$$

For $v$,

$$
\begin{aligned}
\|v\|
&=\sqrt{1^2+0^2+1^2} \\
&=\sqrt2.
\end{aligned}
$$

### 3. Compute the angle

Substitute into the angle formula:

$$
\begin{aligned}
\cos\theta
&=\frac{u\cdot v}{\|u\|\,\|v\|} \\
&=\frac{1}{\sqrt2\cdot\sqrt2} \\
&=\frac12.
\end{aligned}
$$

Hence,

$$
\theta=\arccos\left(\frac12\right)
=\frac{\pi}{3}
=60^\circ.
$$

### 4. Compare with the prediction

The calculated angle, $60^\circ$, is acute, agreeing with the positive dot product.

Geometrically, both vectors have a positive first coordinate, but their remaining nonzero coordinates point along different coordinate axes. They therefore point partly in the same direction without being parallel.

## Verification

Substitute the calculated angle and lengths into the geometric dot product formula:

$$
\begin{aligned}
\|u\|\,\|v\|\cos60^\circ
&=\sqrt2\cdot\sqrt2\cdot\frac12 \\
&=1 \\
&=u\cdot v.
\end{aligned}
$$

This agrees with the coordinate calculation, confirming that the angle is $60^\circ$.
