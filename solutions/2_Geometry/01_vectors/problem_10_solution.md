# Exercise 10. Triangle Area from Vectors

## Problem

The points $A=(0,0,0)$, $B=(2,1,0)$, and $C=(1,3,2)$ form a triangle. Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$, compute the area of the parallelogram using the cross product, and then find the area of the triangle. Explain the factor $\frac12$.

> **Why this exercise:** shows the interpretation of the length of the cross product as area.

## Method

Two side vectors starting at the same vertex determine a parallelogram. Its area is the length of their cross product:

$$
\text{Area of parallelogram}
=\|\overrightarrow{AB}\times\overrightarrow{AC}\|.
$$

The triangle occupies half of that parallelogram, so

$$
\text{Area of triangle}
=\frac12\|\overrightarrow{AB}\times\overrightarrow{AC}\|.
$$

The cross product gives area because its length is $\|u\|\|v\|\sin\theta$: one side length multiplied by the perpendicular height.

## Solution

### 1. Construct the side vectors

Subtract the coordinates of $A$ from those of each endpoint:

$$
\begin{aligned}
\overrightarrow{AB}
&=B-A \\
&=(2-0,\;1-0,\;0-0) \\
&=(2,1,0),
\end{aligned}
$$

and

$$
\begin{aligned}
\overrightarrow{AC}
&=C-A \\
&=(1-0,\;3-0,\;2-0) \\
&=(1,3,2).
\end{aligned}
$$

Both vectors start at $A$, as required.

### 2. Compute the cross product

Let $u=\overrightarrow{AB}$ and $v=\overrightarrow{AC}$. Then

$$
\begin{aligned}
u\times v
&=(1\cdot2-0\cdot3,\;
0\cdot1-2\cdot2,\;
2\cdot3-1\cdot1) \\
&=(2,-4,5).
\end{aligned}
$$

### 3. Find the parallelogram area

Take the length of the cross product:

$$
\begin{aligned}
\text{Area of parallelogram}
&=\sqrt{2^2+(-4)^2+5^2} \\
&=\sqrt{4+16+25} \\
&=\sqrt{45} \\
&=3\sqrt5.
\end{aligned}
$$

### 4. Find the triangle area

The triangle and the parallelogram have the same base and perpendicular height. A triangle has area $\frac12$ times base times height, while a parallelogram has area base times height.

Equivalently, the diagonal joining $B$ and $C$ divides the parallelogram into two congruent triangles, one of which is $ABC$.

Therefore,

$$
\begin{aligned}
\text{Area of triangle }ABC
&=\frac12\cdot3\sqrt5 \\
&=\frac{3\sqrt5}{2}.
\end{aligned}
$$

The area is $\frac{3\sqrt5}{2}$ square units.

## Verification

First, check that the computed cross product is perpendicular to both side vectors:

$$
\begin{aligned}
(2,-4,5)\cdot(2,1,0)
&=4-4+0=0, \\
(2,-4,5)\cdot(1,3,2)
&=2-12+10=0.
\end{aligned}
$$

We can also check its squared length using

$$
\|u\times v\|^2
=\|u\|^2\|v\|^2-(u\cdot v)^2.
$$

Here,

$$
\|u\|^2=5,\qquad
\|v\|^2=14,\qquad
u\cdot v=5.
$$

Thus,

$$
\|u\times v\|^2=5\cdot14-5^2=70-25=45.
$$

This agrees with the calculated parallelogram area $\sqrt{45}=3\sqrt5$ and confirms the triangle area $\frac{3\sqrt5}{2}$.
