# Exercise 8. Sphere

## Problem

Reduce

$$
x^2+y^2+z^2-4x+2y-6z-2=0
$$

to canonical form. Find the center and radius. Give two points on the sphere and check them in the equation.

> **Why this exercise:** transfers the technique known from circles from two dimensions to three.

## Method

We complete the square separately for each coordinate.

The canonical equation of a sphere is

$$
(x-h)^2+(y-k)^2+(z-l)^2=r^2,
$$

where $(h,k,l)$ is the center and $r>0$ is the radius.

After finding the center and radius, we choose two points by moving one radius from the center along a coordinate axis.

## Solution

### 1. Group the terms

Rearrange the original equation:

$$
(x^2-4x)+(y^2+2y)+(z^2-6z)=2.
$$

### 2. Complete the squares

Use the identities

$$
x^2-4x=(x-2)^2-4,
$$

$$
y^2+2y=(y+1)^2-1,
$$

$$
z^2-6z=(z-3)^2-9.
$$

Substituting gives

$$
(x-2)^2-4+(y+1)^2-1+(z-3)^2-9=2.
$$

The subtracted constants total 14. Adding 14 to both sides produces the canonical form:

$$
(x-2)^2+(y+1)^2+(z-3)^2=16.
$$

### 3. Identify the center and radius

Comparing with the standard sphere equation, the center is

$$
C=(2,-1,3),
$$

and the radius is

$$
r=\sqrt{16}=4.
$$

Geometrically, the left-hand side is the squared distance from $(x,y,z)$ to $C$. Therefore, the equation describes all points exactly 4 units from the center.

### 4. Choose two points on the sphere

Move 4 units in each direction along the x-axis from the center:

$$
P=(2+4,-1,3)=(6,-1,3),
$$

$$
Q=(2-4,-1,3)=(-2,-1,3).
$$

Both points are 4 units from $C$ and lie at opposite ends of a diameter.

## Verification

### 1. Check P in the canonical equation

For $P=(6,-1,3)$,

$$
\begin{aligned}
(6-2)^2+(-1+1)^2+(3-3)^2
&=4^2+0^2+0^2 \\
&=16.
\end{aligned}
$$

Thus, $P$ lies on the sphere.

In the original equation,

$$
\begin{aligned}
6^2+(-1)^2+3^2-4\cdot6+2(-1)-6\cdot3-2
&=36+1+9-24-2-18-2 \\
&=0.
\end{aligned}
$$

### 2. Check Q in the canonical equation

For $Q=(-2,-1,3)$,

$$
\begin{aligned}
(-2-2)^2+(-1+1)^2+(3-3)^2
&=(-4)^2+0^2+0^2 \\
&=16.
\end{aligned}
$$

Thus, $Q$ also lies on the sphere.

In the original equation,

$$
\begin{aligned}
(-2)^2+(-1)^2+3^2-4(-2)+2(-1)-6\cdot3-2
&=4+1+9+8-2-18-2 \\
&=0.
\end{aligned}
$$

Both points satisfy both forms, confirming the sphere with center $(2,-1,3)$ and radius 4.
