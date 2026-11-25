# Exercise 10. Projection of a Point onto a Plane

## Problem

Find the orthogonal projection of $P=(2,1,3)$ onto the plane $x+y+z=3$, and then find the reflection of $P$ across this plane. Check that the midpoint of the segment joining the point and its reflection lies on the plane.

> **Why this exercise:** combines the normal, intersection, and distance into the construction of a projection and reflection.

## Method

The orthogonal projection is the intersection of the plane with the line through $P$ in the normal direction.

Let the projection be $H$. The reflected point $P'$ lies on the same normal line, on the opposite side of the plane, at the same distance from $H$. Therefore,

$$
P'=2H-P.
$$

This also makes $H$ the midpoint of the segment joining $P$ and $P'$.

## Solution

### 1. Identify the normal direction

For the plane

$$
x+y+z=3,
$$

a normal vector is

$$
n=(1,1,1).
$$

The line through $P=(2,1,3)$ in this direction is

$$
(x,y,z)=(2,1,3)+t(1,1,1).
$$

Equivalently,

$$
\begin{cases}
x=2+t, \\
y=1+t, \\
z=3+t.
\end{cases}
$$

### 2. Find the intersection with the plane

Substitute the line coordinates into the plane equation:

$$
(2+t)+(1+t)+(3+t)=3.
$$

Simplifying,

$$
\begin{aligned}
6+3t&=3, \\
3t&=-3, \\
t&=-1.
\end{aligned}
$$

Thus, the orthogonal projection is

$$
\begin{aligned}
H
&=(2,1,3)-(1,1,1) \\
&=(1,0,2).
\end{aligned}
$$

### 3. Find the reflected point

The projection is halfway between the original point and its reflection. Hence,

$$
\begin{aligned}
P'
&=2H-P \\
&=2(1,0,2)-(2,1,3) \\
&=(2,0,4)-(2,1,3) \\
&=(0,-1,1).
\end{aligned}
$$

Therefore,

$$
H=(1,0,2),
\qquad
P'=(0,-1,1).
$$

### 4. Explain the geometry

The displacement from the plane to the original point is

$$
P-H=(1,1,1)=n.
$$

The displacement from the plane to the reflected point is

$$
P'-H=(-1,-1,-1)=-n.
$$

These displacements are perpendicular to the plane, equal in length, and opposite in orientation. Thus, the two points lie symmetrically on opposite sides of the plane.

## Verification

### 1. Check the projection

The point $H=(1,0,2)$ satisfies

$$
1+0+2=3,
$$

so it lies in the plane.

Also, $P-H=n$, confirming that the segment from $P$ to $H$ is perpendicular to the plane. Therefore, $H$ is the orthogonal projection.

### 2. Check the midpoint

The midpoint of $P$ and $P'$ is

$$
\begin{aligned}
M
&=\frac{P+P'}{2} \\
&=\left(
\frac{2+0}{2},
\frac{1+(-1)}{2},
\frac{3+1}{2}
\right) \\
&=(1,0,2) \\
&=H.
\end{aligned}
$$

Since $1+0+2=3$, this midpoint lies on the plane, as required.

### 3. Check equal distances

The distances from the two points to $H$ are

$$
\|P-H\|=\sqrt{1^2+1^2+1^2}=\sqrt3,
$$

$$
\|P'-H\|=\sqrt{(-1)^2+(-1)^2+(-1)^2}=\sqrt3.
$$

Together with the opposite normal displacements, this confirms that $P'=(0,-1,1)$ is the reflection of $P$ across the plane.
