# Exercise 8. Intersection Point of a Line and a Plane

## Problem

Find the intersection point of

$$
(x,y,z)=(1,0,2)+t(1,2,-1)
$$

with the plane $x+y+z=4$. Check the result by substituting it into both descriptions.

> **Why this exercise:** practices the most important computational case of the line–plane relationship.

## Method

We express the line coordinates in terms of $t$ and substitute them into the plane equation.

Solving the resulting equation determines the parameter value at the intersection. We then substitute that value back into the line to obtain the point.

## Solution

### 1. Write the coordinate equations of the line

The parametric equation gives

$$
\begin{cases}
x=1+t, \\
y=2t, \\
z=2-t.
\end{cases}
$$

The line direction and plane normal are

$$
v=(1,2,-1),
\qquad
n=(1,1,1).
$$

Their dot product is

$$
n\cdot v=1+2-1=2\ne0.
$$

Therefore, the line intersects the plane at exactly one point.

### 2. Substitute into the plane equation

A point on the line lies in the plane when

$$
(1+t)+2t+(2-t)=4.
$$

Simplifying,

$$
\begin{aligned}
3+2t&=4, \\
2t&=1, \\
t&=\frac12.
\end{aligned}
$$

### 3. Calculate the intersection point

Substitute $t=\frac12$ into the line coordinates:

$$
\begin{aligned}
x&=1+\frac12=\frac32, \\
y&=2\cdot\frac12=1, \\
z&=2-\frac12=\frac32.
\end{aligned}
$$

Thus, the intersection point is

$$
P=\left(\frac32,1,\frac32\right).
$$

## Verification

### 1. Check that P lies on the line

Using $t=\frac12$ in the original vector equation,

$$
\begin{aligned}
(1,0,2)+\frac12(1,2,-1)
&=\left(1+\frac12,\;0+1,\;2-\frac12\right) \\
&=\left(\frac32,1,\frac32\right) \\
&=P.
\end{aligned}
$$

The same parameter value produces all three coordinates, confirming that $P$ lies on the line.

### 2. Check that P lies in the plane

Substitute the coordinates into $x+y+z=4$:

$$
\frac32+1+\frac32=3+1=4.
$$

Therefore, $P$ belongs to both the line and the plane. Since $n\cdot v\ne0$, it is their unique intersection point.
