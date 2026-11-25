# Exercise 4. Plane Through Three Points

## Problem

Find the equation of the plane through

$$
A=(1,0,0),\quad B=(0,1,0),\quad C=(0,0,1).
$$

First construct two vectors lying in the plane, and then use the cross product. Check the resulting equation on all three points.

> **Why this exercise:** connects earlier vector tools with constructing the equation of a plane.

## Method

We construct two vectors starting at the same point:

$$
u=\overrightarrow{AB},
\qquad
v=\overrightarrow{AC}.
$$

Their cross product gives a normal vector to the plane. If this cross product is nonzero, the three points are not collinear and determine a unique plane.

Using the normal $n$ and the point $A$, we write the plane equation as

$$
n\cdot\bigl((x,y,z)-A\bigr)=0.
$$

## Solution

### 1. Construct two vectors in the plane

Subtract the coordinates of $A$ from those of $B$:

$$
\begin{aligned}
u=\overrightarrow{AB}
&=(0-1,\;1-0,\;0-0) \\
&=(-1,1,0).
\end{aligned}
$$

Similarly,

$$
\begin{aligned}
v=\overrightarrow{AC}
&=(0-1,\;0-0,\;1-0) \\
&=(-1,0,1).
\end{aligned}
$$

### 2. Find a normal vector using the cross product

Compute

$$
\begin{aligned}
n=u\times v
&=(1\cdot1-0\cdot0,\;
0\cdot(-1)-(-1)\cdot1,\;
(-1)\cdot0-1\cdot(-1)) \\
&=(1,1,1).
\end{aligned}
$$

The cross product is nonzero, so the two vectors are independent. Therefore, the three points determine a unique plane.

### 3. Construct the plane equation

Using $A=(1,0,0)$ and $n=(1,1,1)$, the point-normal equation is

$$
(1,1,1)\cdot(x-1,y,z)=0.
$$

Expanding and simplifying,

$$
\begin{aligned}
(x-1)+y+z&=0, \\
x+y+z&=1.
\end{aligned}
$$

Thus, the required plane is

$$
\Pi:x+y+z=1.
$$

Geometrically, the plane passes through the point at coordinate 1 on each of the three coordinate axes.

## Verification

### 1. Check all three points

For $A=(1,0,0)$,

$$
1+0+0=1.
$$

For $B=(0,1,0)$,

$$
0+1+0=1.
$$

For $C=(0,0,1)$,

$$
0+0+1=1.
$$

All three points satisfy the plane equation.

### 2. Check the normal vector

The normal must be perpendicular to both constructed directions:

$$
n\cdot u=(1,1,1)\cdot(-1,1,0)=-1+1+0=0,
$$

$$
n\cdot v=(1,1,1)\cdot(-1,0,1)=-1+0+1=0.
$$

These checks confirm that $x+y+z=1$ is the plane through $A,B,C$.
