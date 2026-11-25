# Exercise 6. Angle Between Planes

## Problem

Given

$$
\Pi_1:x+y+z=1,\qquad \Pi_2:x-y=2.
$$

First use the normal vectors to decide whether the planes are parallel. If not, compute the angle between them and explain why the normal vectors alone are enough for this calculation.

> **Why this exercise:** focuses attention on one mechanism—using normals to analyze position and angle—without also introducing the construction of the intersection line.

## Method

The coefficients of $x,y,z$ in a plane equation give a normal vector.

Two planes have parallel orientations exactly when their normal vectors are scalar multiples of each other.

The angle $\theta$ between two planes is conventionally the smaller angle, with $0\le\theta\le90^\circ$. It can be calculated using their normals:

$$
\cos\theta=
\frac{|n_1\cdot n_2|}{\|n_1\|\,\|n_2\|}.
$$

The absolute value ensures that the result does not depend on which orientation we choose for either normal.

## Solution

### 1. Identify the normal vectors

For the first plane,

$$
\Pi_1:x+y+z=1,
$$

a normal vector is

$$
n_1=(1,1,1).
$$

For the second plane,

$$
\Pi_2:x-y=2,
$$

the coefficient of $z$ is zero, so a normal vector is

$$
n_2=(1,-1,0).
$$

### 2. Check whether the planes are parallel

The normals are not scalar multiples of each other.

Indeed, every scalar multiple of $n_2$ has third coordinate zero, whereas $n_1$ has third coordinate 1.

Therefore, the planes are not parallel. They intersect along a line, but finding that line is unnecessary for calculating their angle.

### 3. Calculate the angle

First, compute the dot product:

$$
\begin{aligned}
n_1\cdot n_2
&=1\cdot1+1\cdot(-1)+1\cdot0 \\
&=1-1 \\
&=0.
\end{aligned}
$$

The lengths are

$$
\|n_1\|=\sqrt{1^2+1^2+1^2}=\sqrt3,
$$

$$
\|n_2\|=\sqrt{1^2+(-1)^2+0^2}=\sqrt2.
$$

Thus,

$$
\begin{aligned}
\cos\theta
&=\frac{|0|}{\sqrt3\sqrt2} \\
&=0.
\end{aligned}
$$

Therefore,

$$
\theta=\frac{\pi}{2}=90^\circ.
$$

The planes are perpendicular.

### 4. Explain why the normals are sufficient

A normal vector determines the orientation of a plane. The angle between two planes depends on their orientations, not their positions.

The constants on the right-hand sides determine where the planes are located. Changing these constants translates the planes without changing their normal directions or the angle between them.

Consequently, the two normal vectors contain all the information needed for the angle calculation.

## Verification

We can check the perpendicular arrangement directly using a direction contained in the first plane.

The vector $n_2=(1,-1,0)$ is a direction in $\Pi_1$ because moving by this vector changes $x+y+z$ by

$$
1+(-1)+0=0.
$$

At the same time, $n_2$ is normal to $\Pi_2$. Thus, the first plane contains a direction perpendicular to the second plane, confirming that the planes meet at a right angle.
