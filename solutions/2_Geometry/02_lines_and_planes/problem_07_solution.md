# Exercise 7. A Line Relative to a Plane

## Problem

For

$$
L:(x,y,z)=(1,1,0)+t(1,-1,0),\qquad \Pi:x+y+z=2,
$$

determine whether the line intersects the plane at one point, is parallel to it, or lies in it. Explain the role of the dot product of the direction vector and the normal vector.

> **Why this exercise:** builds a universal test for the relative position of a line and a plane.

## Method

For a line with direction vector $v$ and a plane with normal vector $n$, the dot product $n\cdot v$ measures whether moving along the line changes the plane's left-hand side.

If $n\cdot v\ne0$, the line intersects the plane at exactly one point.

If $n\cdot v=0$, the line's direction is parallel to the plane. We must then check a point on the line:

- If the point lies in the plane, the entire line lies in it.
- If the point does not lie in the plane, the line is parallel to the plane with no common points.

## Solution

### 1. Identify the point, direction, and normal

From the line equation, a point on the line is

$$
p=(1,1,0),
$$

and its direction vector is

$$
v=(1,-1,0).
$$

From the plane equation, a normal vector is

$$
n=(1,1,1).
$$

### 2. Calculate the dot product

$$
\begin{aligned}
n\cdot v
&=1\cdot1+1\cdot(-1)+1\cdot0 \\
&=0.
\end{aligned}
$$

Thus, the line direction is perpendicular to the normal and therefore parallel to the plane.

This calculation alone does not distinguish a line contained in the plane from a parallel line outside it.

### 3. Check a point on the line

Substitute $p=(1,1,0)$ into the plane equation:

$$
1+1+0=2.
$$

Therefore, $p$ lies in the plane.

Since the line starts at a point in the plane and moves in a direction parallel to it, every point of the line remains in the plane. Hence,

$$
L\subset\Pi.
$$

The line lies entirely in the plane, so they have infinitely many common points.

### 4. Explain the role of the dot product

For any parameter value $t$,

$$
n\cdot(p+tv)=n\cdot p+t(n\cdot v).
$$

Here,

$$
n\cdot p=2,
\qquad
n\cdot v=0.
$$

Therefore,

$$
n\cdot(p+tv)=2+t\cdot0=2.
$$

The zero dot product means that moving along the line does not change the value of $x+y+z$. Since that value is already 2 at the starting point, the plane equation holds along the entire line.

## Verification

Write the line in coordinate form:

$$
\begin{cases}
x=1+t, \\
y=1-t, \\
z=0.
\end{cases}
$$

Substitute into the plane equation:

$$
\begin{aligned}
x+y+z
&=(1+t)+(1-t)+0 \\
&=2.
\end{aligned}
$$

This identity holds for every real $t$, confirming that the entire line lies in the plane.
