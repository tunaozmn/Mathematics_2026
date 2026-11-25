# Exercise 4. Dot Product and Perpendicularity

## Problem

For $u=(1,2,-1)$ and $v=(2,-1,3)$ compute $u\cdot v$ and determine whether the vectors are perpendicular. Then find $a$ so that $w=(2,-1,a)$ is perpendicular to $u$, and check the result.

> **Why this exercise:** shows the dot product as both a test and a tool for constructing a perpendicularity condition.

## Method

The dot product is the sum of the products of corresponding coordinates:

$$
u\cdot v=u_1v_1+u_2v_2+u_3v_3.
$$

Two nonzero vectors are perpendicular exactly when their dot product is zero.

We first calculate $u\cdot v$. Then we impose the condition $u\cdot w=0$ and solve for $a$.

## Solution

### 1. Compute the dot product of u and v

$$
\begin{aligned}
u\cdot v
&=1\cdot2+2\cdot(-1)+(-1)\cdot3 \\
&=2-2-3 \\
&=-3.
\end{aligned}
$$

Since the dot product is not zero, $u$ and $v$ are not perpendicular.

### 2. Set up the perpendicularity condition for w

For $w=(2,-1,a)$,

$$
\begin{aligned}
u\cdot w
&=1\cdot2+2\cdot(-1)+(-1)\cdot a \\
&=2-2-a \\
&=-a.
\end{aligned}
$$

To make $w$ perpendicular to $u$, require

$$
-a=0.
$$

Therefore,

$$
a=0,
$$

and the required vector is

$$
w=(2,-1,0).
$$

### 3. Interpret the condition geometrically

The dot product also satisfies

$$
u\cdot w=\|u\|\,\|w\|\cos\theta,
$$

where $\theta$ is the angle between the vectors.

Both vectors are nonzero, so their lengths are positive. Thus, $u\cdot w=0$ implies $\cos\theta=0$, giving a right angle.

For this particular vector, the contributions from the first two coordinates cancel. Setting $a=0$ makes the third contribution zero as well.

## Verification

Substitute the value $a=0$ directly:

$$
\begin{aligned}
u\cdot w
&=(1,2,-1)\cdot(2,-1,0) \\
&=1\cdot2+2\cdot(-1)+(-1)\cdot0 \\
&=2-2+0 \\
&=0.
\end{aligned}
$$

Therefore, $w=(2,-1,0)$ is perpendicular to $u$, confirming the result.
