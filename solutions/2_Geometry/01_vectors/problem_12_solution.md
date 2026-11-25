# Exercise 12. A Normal Vector to a Plane

## Problem

Given $A=(1,0,2)$, $B=(2,1,0)$, and $C=(0,3,1)$. Construct two vectors lying in the plane, find a vector perpendicular to both, and check the perpendicularity using dot products.

> **Why this exercise:** creates a direct bridge from vectors to the description of a plane.

## Method

We construct two vectors in the plane by subtracting the coordinates of a common starting point:

$$
u=\overrightarrow{AB}=B-A,
\qquad
v=\overrightarrow{AC}=C-A.
$$

Their cross product is perpendicular to both. If it is nonzero, the two vectors are not parallel and determine a plane. The cross product is then a normal vector to that plane.

## Solution

### 1. Construct two vectors in the plane

From $A$ to $B$,

$$
\begin{aligned}
u=\overrightarrow{AB}
&=(2-1,\;1-0,\;0-2) \\
&=(1,1,-2).
\end{aligned}
$$

From $A$ to $C$,

$$
\begin{aligned}
v=\overrightarrow{AC}
&=(0-1,\;3-0,\;1-2) \\
&=(-1,3,-1).
\end{aligned}
$$

Both vectors connect points of the plane, so they give directions lying in it.

### 2. Compute a vector perpendicular to both

Use the cross product:

$$
n=u\times v.
$$

Calculating its coordinates gives

$$
\begin{aligned}
n
&=\bigl(
1\cdot(-1)-(-2)\cdot3,\;
(-2)\cdot(-1)-1\cdot(-1),\;
1\cdot3-1\cdot(-1)
\bigr) \\
&=(-1+6,\;2+1,\;3+1) \\
&=(5,3,4).
\end{aligned}
$$

Therefore, a normal vector is

$$
n=(5,3,4).
$$

### 3. Explain the geometric meaning

Since $n$ is nonzero, the vectors $\overrightarrow{AB}$ and $\overrightarrow{AC}$ are not parallel. Thus, the three points are not collinear and determine a unique plane.

The vector $n$ is perpendicular to both independent directions in that plane, so it is perpendicular to the plane.

A normal vector is not unique: any nonzero scalar multiple of $n$ is also a normal vector. In particular, reversing the cross product gives $-n$, which points in the opposite direction.

## Verification

Check perpendicularity to $\overrightarrow{AB}$:

$$
\begin{aligned}
n\cdot\overrightarrow{AB}
&=(5,3,4)\cdot(1,1,-2) \\
&=5+3-8 \\
&=0.
\end{aligned}
$$

Check perpendicularity to $\overrightarrow{AC}$:

$$
\begin{aligned}
n\cdot\overrightarrow{AC}
&=(5,3,4)\cdot(-1,3,-1) \\
&=-5+9-4 \\
&=0.
\end{aligned}
$$

Both dot products are zero, confirming that $n=(5,3,4)$ is perpendicular to both constructed vectors and is a normal vector to the plane through $A,B,C$.
