# Exercise 13. Closest Point on a Plane

## Problem

Find the point on the plane $x+2y+2z=4$ closest to $P=(3,0,0)$. Give the distance and check that the segment joining the two points is perpendicular to the plane.

> **Why this exercise:** combines projection, distance, and the normal direction in one problem.

## Method

The closest point is the orthogonal projection of $P$ onto the plane. We find it by intersecting the plane with the line through $P$ in the normal direction.

The distance is the length of the resulting perpendicular segment. We then justify that this segment is shorter than the segment from $P$ to any other point of the plane.

## Solution

### 1. Identify the normal and construct the perpendicular line

For the plane

$$
x+2y+2z=4,
$$

a normal vector is

$$
n=(1,2,2).
$$

The line through $P=(3,0,0)$ in this direction is

$$
(x,y,z)=(3,0,0)+t(1,2,2).
$$

Thus,

$$
x=3+t,\qquad y=2t,\qquad z=2t.
$$

### 2. Find the intersection with the plane

Substitute these coordinates into the plane equation:

$$
(3+t)+2(2t)+2(2t)=4.
$$

Simplifying,

$$
\begin{aligned}
3+9t&=4, \\
9t&=1, \\
t&=\frac19.
\end{aligned}
$$

Therefore, the closest point is

$$
\begin{aligned}
H
&=(3,0,0)+\frac19(1,2,2) \\
&=\left(\frac{28}{9},\frac29,\frac29\right).
\end{aligned}
$$

### 3. Calculate the distance

The displacement from $P$ to $H$ is

$$
\overrightarrow{PH}
=H-P
=\left(\frac19,\frac29,\frac29\right)
=\frac19n.
$$

Its length is

$$
\begin{aligned}
d
&=\|\overrightarrow{PH}\| \\
&=\sqrt{\left(\frac19\right)^2+
\left(\frac29\right)^2+
\left(\frac29\right)^2} \\
&=\sqrt{\frac{1+4+4}{81}} \\
&=\frac13.
\end{aligned}
$$

### 4. Explain why H is the closest point

The vector $\overrightarrow{PH}$ is parallel to the normal, so the segment $PH$ is perpendicular to the plane.

For any other point $R$ in the plane, the vector $\overrightarrow{HR}$ lies along the plane and is perpendicular to $\overrightarrow{PH}$. The Pythagorean theorem gives

$$
\|P-R\|^2=\|P-H\|^2+\|H-R\|^2.
$$

The second term is nonnegative and is zero only when $R=H$. Therefore, $H$ is the unique closest point.

## Verification

### 1. Check that H lies in the plane

Substitute its coordinates:

$$
\frac{28}{9}+2\cdot\frac29+2\cdot\frac29
=\frac{28+4+4}{9}
=4.
$$

Thus, $H$ lies in the plane.

### 2. Check perpendicularity

We found

$$
\overrightarrow{PH}=\frac19(1,2,2)=\frac19n.
$$

Since the joining vector is a nonzero scalar multiple of the normal, it is perpendicular to the plane.

### 3. Check the distance using the point-to-plane formula

$$
\begin{aligned}
d
&=\frac{|3+2\cdot0+2\cdot0-4|}
{\sqrt{1^2+2^2+2^2}} \\
&=\frac{|-1|}{3} \\
&=\frac13.
\end{aligned}
$$

This agrees with the segment length. Hence, the closest point and distance are

$$
H=\left(\frac{28}{9},\frac29,\frac29\right),
\qquad
d=\frac13.
$$
