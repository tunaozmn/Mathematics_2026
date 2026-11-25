# Exercise 6. Projection and Perpendicular Component

## Problem

Find the projection of $u=(4,2)$ onto the direction $v=(1,1)$. Then compute

$$
r=u-\mathrm{proj}_v\,u
$$

and verify that $r\cdot v=0$. Explain this result geometrically.

> **Why this exercise:** shows projection as a decomposition into parallel and perpendicular components.

## Method

For a nonzero vector $v$, the vector projection of $u$ onto the direction of $v$ is

$$
\mathrm{proj}_v\,u=\frac{u\cdot v}{v\cdot v}\,v.
$$

This gives the component of $u$ parallel to $v$. Subtracting it from $u$ gives the remaining component,

$$
r=u-\mathrm{proj}_v\,u.
$$

We check that this remainder is perpendicular to $v$ by computing their dot product.

## Solution

### 1. Calculate the projection coefficient

First, compute

$$
u\cdot v=4\cdot1+2\cdot1=6.
$$

Also,

$$
v\cdot v=1^2+1^2=2.
$$

Therefore, the projection coefficient is

$$
\frac{u\cdot v}{v\cdot v}=\frac62=3.
$$

### 2. Find the projection vector

Multiply $v$ by this coefficient:

$$
\begin{aligned}
\mathrm{proj}_v\,u
&=3(1,1) \\
&=(3,3).
\end{aligned}
$$

This vector is parallel to $v$ because it is a scalar multiple of $v$.

### 3. Calculate the remaining component

Subtract the projection from $u$:

$$
\begin{aligned}
r
&=u-\mathrm{proj}_v\,u \\
&=(4,2)-(3,3) \\
&=(1,-1).
\end{aligned}
$$

Thus, the decomposition is

$$
u=(3,3)+(1,-1).
$$

### 4. Explain the geometry

The direction $v=(1,1)$ determines the line $y=x$ through the origin.

The projection vector $(3,3)$ lies along this line. The remainder $(1,-1)$ points from the endpoint of the projection to the endpoint of $u$ and is perpendicular to the line.

Thus, $u$ is decomposed into two components: one parallel to the chosen direction and one perpendicular to it.

## Verification

First, check perpendicularity:

$$
\begin{aligned}
r\cdot v
&=(1,-1)\cdot(1,1) \\
&=1\cdot1+(-1)\cdot1 \\
&=0.
\end{aligned}
$$

Next, check that the components reconstruct the original vector:

$$
\mathrm{proj}_v\,u+r=(3,3)+(1,-1)=(4,2)=u.
$$

The squared lengths also satisfy the Pythagorean relation:

$$
\begin{aligned}
\|u\|^2&=4^2+2^2=20, \\
\|\mathrm{proj}_v\,u\|^2+\|r\|^2
&=(3^2+3^2)+(1^2+(-1)^2) \\
&=18+2 \\
&=20.
\end{aligned}
$$

These checks confirm the decomposition into perpendicular components.
