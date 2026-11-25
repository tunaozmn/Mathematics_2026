# Exercise 15. Complete Classification of a Line Relative to a Plane

## Problem

Let

$$
L:p+tv,\qquad \Pi:n\cdot x=d.
$$

State the conditions distinguishing the three cases: one intersection point, parallel with no common points, and the line contained in the plane. Then illustrate each case with your own simple numerical example.

> **Why this exercise:** requires formulating a general mathematical criterion instead of carrying out one isolated calculation.

## Method

Assume $v\ne0$ and $n\ne0$, so the expressions describe a line and a plane.

A point on the line belongs to the plane exactly when

$$
n\cdot(p+tv)=d.
$$

Expanding gives

$$
n\cdot p+t(n\cdot v)=d.
$$

Thus, the classification depends on whether the coefficient $n\cdot v$ is zero and, if it is, whether $n\cdot p=d$.

## Solution

### 1. One intersection point

If

$$
n\cdot v\ne0,
$$

we can solve uniquely for the parameter:

$$
t=\frac{d-n\cdot p}{n\cdot v}.
$$

Therefore, the line intersects the plane at exactly one point,

$$
q=p+\frac{d-n\cdot p}{n\cdot v}\,v.
$$

Geometrically, the line has a nonzero component in the normal direction, so it crosses the plane.

For example, take

$$
L_1:(x,y,z)=(0,0,1)+t(1,0,-1),
\qquad
\Pi:z=0.
$$

Here,

$$
n=(0,0,1),\qquad n\cdot v=-1\ne0.
$$

The plane condition is

$$
1-t=0,
$$

so $t=1$. The intersection point is

$$
q=(1,0,0).
$$

### 2. Parallel with no common points

If

$$
n\cdot v=0
\qquad\text{and}\qquad
n\cdot p\ne d,
$$

the intersection equation reduces to the false statement

$$
n\cdot p=d.
$$

No parameter value can satisfy it. Therefore, the line is parallel to the plane with no common points.

Geometrically, moving along the line does not change its position in the normal direction, and its starting point is outside the plane.

For example, take

$$
L_2:(x,y,z)=(0,0,1)+t(1,0,0),
\qquad
\Pi:z=0.
$$

Here,

$$
n\cdot v=0,
\qquad
n\cdot p=1\ne0=d.
$$

Every point of the line has $z=1$, so the line never meets the plane.

### 3. The line is contained in the plane

If

$$
n\cdot v=0
\qquad\text{and}\qquad
n\cdot p=d,
$$

the intersection equation holds for every real $t$:

$$
n\cdot(p+tv)=d+t\cdot0=d.
$$

Therefore, every point of the line lies in the plane.

Geometrically, the line starts in the plane and moves in a direction parallel to it.

For example, take

$$
L_3:(x,y,z)=(0,1,0)+t(1,0,0),
\qquad
\Pi:z=0.
$$

Here,

$$
n\cdot v=0,
\qquad
n\cdot p=0=d.
$$

Every point of the line has $z=0$, so the entire line is contained in the plane.

### 4. Summarize the classification

| Conditions | Relative position | Common points |
| --- | --- | --- |
| $n\cdot v\ne0$ | The line crosses the plane | Exactly one |
| $n\cdot v=0$ and $n\cdot p\ne d$ | Parallel and disjoint | None |
| $n\cdot v=0$ and $n\cdot p=d$ | The line lies in the plane | Every point of the line |

These cases are exhaustive: $n\cdot v$ is either nonzero or zero. In the zero case, the starting point either satisfies the plane equation or does not.

## Verification

For the first example,

$$
L_1(t)=(t,0,1-t).
$$

Its third coordinate equals zero only at $t=1$, confirming exactly one intersection.

For the second example,

$$
L_2(t)=(t,0,1).
$$

Its third coordinate is never zero, confirming that there are no common points.

For the third example,

$$
L_3(t)=(t,1,0).
$$

Its third coordinate is zero for every real $t$, confirming that the entire line lies in the plane.
