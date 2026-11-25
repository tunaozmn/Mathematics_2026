# Exercise 3. Plane Through a Point with a Given Normal Vector

## Problem

Find the equation of the plane through $P=(1,-2,3)$ and perpendicular to $n=(2,1,-1)$. Check the result by substituting the point $P$ and explain the role of the normal vector.

> **Why this exercise:** shows the basic construction of a plane from a point and a normal vector.

## Method

If a plane passes through $P$ and has a nonzero normal vector $n$, then every point $X=(x,y,z)$ on the plane satisfies

$$
n\cdot(X-P)=0.
$$

This says that the displacement from $P$ to any other point of the plane is perpendicular to the normal vector.

## Solution

### 1. Construct the displacement from P

For a general point $X=(x,y,z)$,

$$
X-P=(x-1,\;y+2,\;z-3).
$$

The second coordinate is $y+2$ because the second coordinate of $P$ is $-2$.

### 2. Apply the perpendicularity condition

Using $n=(2,1,-1)$, require

$$
(2,1,-1)\cdot(x-1,y+2,z-3)=0.
$$

Expanding the dot product gives the point-normal form:

$$
2(x-1)+(y+2)-(z-3)=0.
$$

### 3. Simplify the equation

$$
\begin{aligned}
2x-2+y+2-z+3&=0, \\
2x+y-z+3&=0.
\end{aligned}
$$

Therefore, the required plane is

$$
\Pi:2x+y-z+3=0.
$$

Equivalently,

$$
2x+y-z=-3.
$$

### 4. Explain the role of the normal vector

The vector $n=(2,1,-1)$ is perpendicular to every direction lying in the plane. Its coordinates appear as the coefficients of $x,y,z$ in the plane equation.

The normal determines the plane's orientation. The requirement that the plane pass through $P$ determines its position.

Any nonzero scalar multiple of $n$ is also a normal vector to the same plane.

## Verification

### 1. Check that P lies on the plane

Substitute $P=(1,-2,3)$ into the equation:

$$
2\cdot1+(-2)-3+3=0.
$$

Thus, the plane contains the given point.

### 2. Check the normal against two plane directions

Choose two independent vectors

$$
u=(1,-2,0),
\qquad
v=(0,1,1).
$$

Their dot products with $n$ are

$$
n\cdot u=2\cdot1+1\cdot(-2)+(-1)\cdot0=0,
$$

$$
n\cdot v=2\cdot0+1\cdot1+(-1)\cdot1=0.
$$

Moving from $P$ in either direction preserves the plane equation. Hence, both are directions in the plane, and the given normal is perpendicular to both, as required.
