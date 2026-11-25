# Exercise 9. Cross Product as a Perpendicular Direction

## Problem

For $u=(1,2,0)$ and $v=(0,1,3)$ compute $u\times v$. Use dot products to check perpendicularity to both vectors, compute $v\times u$, and compare the results.

> **Why this exercise:** teaches the geometric meaning of the cross product and the effect of changing the order of its arguments.

## Method

For vectors in $\mathbb{R}^3$, the cross product is

$$
u\times v=
(u_2v_3-u_3v_2,\;
u_3v_1-u_1v_3,\;
u_1v_2-u_2v_1).
$$

If the vectors are not parallel, their cross product is a nonzero vector perpendicular to both. Its orientation is determined by the right-hand rule.

We compute the cross product, verify perpendicularity using dot products, and then calculate the product in the reverse order.

## Solution

### 1. Compute u × v

Substitute the coordinates into the formula:

$$
\begin{aligned}
u\times v
&=(2\cdot3-0\cdot1,\;
0\cdot0-1\cdot3,\;
1\cdot1-2\cdot0) \\
&=(6,-3,1).
\end{aligned}
$$

Let

$$
n=u\times v=(6,-3,1).
$$

### 2. Check perpendicularity to u

Compute

$$
\begin{aligned}
n\cdot u
&=(6,-3,1)\cdot(1,2,0) \\
&=6\cdot1+(-3)\cdot2+1\cdot0 \\
&=6-6 \\
&=0.
\end{aligned}
$$

Since both vectors are nonzero, this confirms that $n$ is perpendicular to $u$.

### 3. Check perpendicularity to v

Similarly,

$$
\begin{aligned}
n\cdot v
&=(6,-3,1)\cdot(0,1,3) \\
&=6\cdot0+(-3)\cdot1+1\cdot3 \\
&=-3+3 \\
&=0.
\end{aligned}
$$

Thus, $n$ is also perpendicular to $v$. It is therefore a normal vector to the plane spanned by $u$ and $v$.

### 4. Compute v × u

Reverse the order in the cross product formula:

$$
\begin{aligned}
v\times u
&=(1\cdot0-3\cdot2,\;
3\cdot1-0\cdot0,\;
0\cdot2-1\cdot1) \\
&=(-6,3,-1).
\end{aligned}
$$

### 5. Compare the results geometrically

The two results satisfy

$$
v\times u=-(u\times v).
$$

They have the same length and lie along the same normal line, but point in opposite directions.

This illustrates the anti-commutative property of the cross product: reversing the order changes the sign. Geometrically, the right-hand rule selects the opposite orientation when the order of the two vectors is reversed.

## Verification

The dot products above verified that $u\times v$ is perpendicular to both original vectors.

For the reverse product,

$$
\begin{aligned}
(v\times u)\cdot u
&=(-6)\cdot1+3\cdot2+(-1)\cdot0 \\
&=0, \\
(v\times u)\cdot v
&=(-6)\cdot0+3\cdot1+(-1)\cdot3 \\
&=0.
\end{aligned}
$$

The lengths also agree:

$$
\|u\times v\|=\sqrt{6^2+(-3)^2+1^2}=\sqrt{46},
$$

$$
\|v\times u\|=\sqrt{(-6)^2+3^2+(-1)^2}=\sqrt{46}.
$$

Both products are perpendicular to the same plane, with equal lengths and opposite orientations.
