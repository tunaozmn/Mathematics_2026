# Exercise 14. Contrast: Intersection and Parallelism

## Problem

From the point $P=(0,0,1)$, two lines are drawn with direction vectors

$$
v_1=(2,1,-1),\qquad v_2=(2,1,0).
$$

For each line, analyze its position relative to the plane $z=0$.

For the line that intersects the plane, find the intersection point. For the other line, explain how you can recognize parallelism without solving an equation.

> **Why this exercise:** compares two very similar data sets that lead to different outcomes and forces recognition of the geometric condition before calculation.

## Method

The plane $z=0$ has normal vector

$$
n=(0,0,1).
$$

For a line with direction vector $v$, the dot product $n\cdot v$ is its third coordinate. It measures how the height $z$ changes as the parameter changes.

If this dot product is nonzero, the line intersects the plane once. If it is zero, the height remains constant, and the starting point determines whether the line lies in the plane or is parallel with no common points.

## Solution

### 1. Write the two line equations

The first line is

$$
L_1:(x,y,z)=(0,0,1)+t(2,1,-1),
$$

so

$$
x=2t,\qquad y=t,\qquad z=1-t.
$$

The second line is

$$
L_2:(x,y,z)=(0,0,1)+s(2,1,0),
$$

so

$$
x=2s,\qquad y=s,\qquad z=1.
$$

### 2. Analyze the first line

Compute the dot product with the plane normal:

$$
n\cdot v_1=(0,0,1)\cdot(2,1,-1)=-1.
$$

Since it is nonzero, $L_1$ intersects the plane at exactly one point.

To find that point, impose $z=0$:

$$
1-t=0,\qquad t=1.
$$

Substitute into the line:

$$
\begin{aligned}
Q
&=(0,0,1)+(2,1,-1) \\
&=(2,1,0).
\end{aligned}
$$

Thus, the unique intersection point is

$$
Q=(2,1,0).
$$

### 3. Analyze the second line

For the second direction,

$$
n\cdot v_2=(0,0,1)\cdot(2,1,0)=0.
$$

Thus, $v_2$ is parallel to the plane. Its zero third coordinate means that moving along the line never changes the height.

The starting point has $z=1$, so every point of $L_2$ also has $z=1$. No point can satisfy $z=0$.

Therefore, $L_2$ is parallel to the plane with no common points. This conclusion follows directly from the direction and starting point, without solving for a parameter.

### 4. Compare the two cases

| Line | Normal-direction dot product | Height along the line | Position relative to the plane |
| --- | --- | --- | --- |
| $L_1$ | $-1$ | $z=1-t$ | One intersection at $(2,1,0)$ |
| $L_2$ | $0$ | $z=1$ | Parallel with no common points |

Both lines start at the same point, but only the first has a component in the normal direction. That component allows its height to change until it reaches the plane.

## Verification

For the first line, the point $Q=(2,1,0)$ is obtained at $t=1$ and has third coordinate zero. It therefore belongs to both $L_1$ and the plane.

For the second line, a general point is

$$
(2s,s,1).
$$

Its third coordinate is 1 for every real $s$, so it never lies in the plane $z=0$. This confirms the parallel, disjoint case.
