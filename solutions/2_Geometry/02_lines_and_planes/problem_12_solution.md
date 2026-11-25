# Exercise 12. Intersection Line of Two Planes

## Problem

Find a parametric equation of the line that is the intersection of

$$
x+y+z=3,\qquad x-y+z=1.
$$

Find its direction vector in two ways: from the system of equations and from the cross product of the normal vectors. Compare the results.

> **Why this exercise:** shows the equivalence of the algebraic and geometric approaches to constructing an intersection line.

## Method

A point on the intersection must satisfy both plane equations. We solve them together, choose a free variable, and express the solution as a parametric line.

Geometrically, the intersection direction must be perpendicular to both plane normals. Their cross product therefore gives another direction vector for the same line.

## Solution

### 1. Solve the two plane equations together

Subtract the second equation from the first:

$$
\begin{aligned}
(x+y+z)-(x-y+z)&=3-1, \\
2y&=2, \\
y&=1.
\end{aligned}
$$

Substitute $y=1$ into the first equation:

$$
\begin{aligned}
x+1+z&=3, \\
x+z&=2.
\end{aligned}
$$

Thus, the intersection is described by

$$
y=1,\qquad x+z=2.
$$

### 2. Write the parametric equation

Choose $z=t$, where $t$ is any real number. Then

$$
x=2-t,\qquad y=1,\qquad z=t.
$$

Therefore, the intersection line is

$$
L:(x,y,z)=(2,1,0)+t(-1,0,1),
\qquad t\in\mathbb{R}.
$$

From the system of equations, we have obtained the direction vector

$$
v=(-1,0,1).
$$

As $z$ increases by 1, $x$ decreases by 1 while $y$ stays fixed.

### 3. Find a direction using the plane normals

The normal vectors are

$$
n_1=(1,1,1),
\qquad
n_2=(1,-1,1).
$$

Compute their cross product:

$$
\begin{aligned}
n_1\times n_2
&=(1\cdot1-1\cdot(-1),\;
1\cdot1-1\cdot1,\;
1\cdot(-1)-1\cdot1) \\
&=(2,0,-2).
\end{aligned}
$$

This vector is nonzero, so the normals are not parallel. The planes therefore intersect in a line.

Because the cross product is perpendicular to both normals, it is parallel to both planes and gives the intersection direction.

### 4. Compare the direction vectors

The two results are

$$
v=(-1,0,1),
\qquad
n_1\times n_2=(2,0,-2).
$$

They satisfy

$$
n_1\times n_2=-2v.
$$

Thus, they are nonzero scalar multiples and describe the same line direction. Their lengths and orientations differ, but this does not change the set of points traced when the parameter ranges over all real numbers.

An equivalent parametrization is

$$
L:(x,y,z)=(2,1,0)+s(2,0,-2),
\qquad s\in\mathbb{R}.
$$

The parameter choices correspond through $t=-2s$.

## Verification

### 1. Check both plane equations

Substitute the general point $(2-t,1,t)$ into the first plane:

$$
(2-t)+1+t=3.
$$

For the second plane,

$$
(2-t)-1+t=1.
$$

Both equations hold for every real $t$, so every point of the proposed line lies in both planes.

Conversely, solving the two equations forced $y=1$ and $x=2-z$. Taking $t=z$ therefore includes every common point.

### 2. Check the direction against both normals

$$
n_1\cdot v=(1,1,1)\cdot(-1,0,1)=-1+0+1=0,
$$

$$
n_2\cdot v=(1,-1,1)\cdot(-1,0,1)=-1+0+1=0.
$$

The direction is perpendicular to both normals, confirming the agreement between the algebraic and geometric methods.
