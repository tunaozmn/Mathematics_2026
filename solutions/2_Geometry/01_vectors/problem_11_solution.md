# Exercise 11. Decomposition into Parallel and Perpendicular Components

## Problem

Decompose $u=(3,4)$ into components parallel and perpendicular to $v=(1,2)$. Check

$$
u=u_{\parallel}+u_{\perp},\qquad u_{\perp}\cdot v=0.
$$

Explain why these are two independent checks of correctness.

> **Why this exercise:** deepens the idea of projection through construction and verification.

## Method

The parallel component is the projection of $u$ onto the direction of the nonzero vector $v$:

$$
u_{\parallel}=\frac{u\cdot v}{v\cdot v}\,v.
$$

The perpendicular component is the remainder:

$$
u_{\perp}=u-u_{\parallel}.
$$

We check both that the components reconstruct $u$ and that the remainder is perpendicular to $v$.

## Solution

### 1. Calculate the projection coefficient

Compute the required dot products:

$$
u\cdot v=3\cdot1+4\cdot2=11,
$$

$$
v\cdot v=1^2+2^2=5.
$$

Therefore,

$$
\frac{u\cdot v}{v\cdot v}=\frac{11}{5}.
$$

### 2. Find the parallel component

Multiply $v$ by the projection coefficient:

$$
\begin{aligned}
u_{\parallel}
&=\frac{11}{5}(1,2) \\
&=\left(\frac{11}{5},\frac{22}{5}\right).
\end{aligned}
$$

This component is parallel to $v$ because it is a scalar multiple of $v$.

### 3. Find the perpendicular component

Subtract the parallel component from $u$:

$$
\begin{aligned}
u_{\perp}
&=(3,4)-\left(\frac{11}{5},\frac{22}{5}\right) \\
&=\left(\frac{15}{5}-\frac{11}{5},
\frac{20}{5}-\frac{22}{5}\right) \\
&=\left(\frac45,-\frac25\right).
\end{aligned}
$$

Thus, the decomposition is

$$
u_{\parallel}=\left(\frac{11}{5},\frac{22}{5}\right),
\qquad
u_{\perp}=\left(\frac45,-\frac25\right).
$$

Geometrically, $u_{\parallel}$ lies along the line through the origin in direction $v$. The vector $u_{\perp}$ connects its endpoint to the endpoint of $u$ at a right angle to that line.

## Verification

### 1. Check that the components reconstruct u

$$
\begin{aligned}
u_{\parallel}+u_{\perp}
&=\left(\frac{11}{5},\frac{22}{5}\right)
+\left(\frac45,-\frac25\right) \\
&=\left(\frac{15}{5},\frac{20}{5}\right) \\
&=(3,4) \\
&=u.
\end{aligned}
$$

This confirms that no part of the original vector is missing from the decomposition.

### 2. Check perpendicularity

$$
\begin{aligned}
u_{\perp}\cdot v
&=\left(\frac45,-\frac25\right)\cdot(1,2) \\
&=\frac45-\frac45 \\
&=0.
\end{aligned}
$$

Thus, the remainder is perpendicular to $v$ and therefore also to $u_{\parallel}$.

### 3. Explain why the checks are independent

The reconstruction check verifies the sum, while the dot product check verifies the geometric direction of the remainder. Neither condition alone guarantees the other.

For example, choosing $u_{\parallel}=v$ and $u_{\perp}=u-v=(2,2)$ would reconstruct $u$, but

$$
(2,2)\cdot(1,2)=6\ne0.
$$

So a correct sum alone does not ensure perpendicularity.

Conversely, $(2,-1)$ is perpendicular to $v$ because

$$
(2,-1)\cdot(1,2)=2-2=0.
$$

However, pairing it with $u_{\parallel}=v$ gives

$$
(1,2)+(2,-1)=(3,1)\ne u.
$$

So perpendicularity alone does not ensure reconstruction.

Our calculated components satisfy both checks, and the parallel component is explicitly a multiple of $v$. Together, these facts confirm the required decomposition.
