# Exercise 11. Plane Containing a Line and a Point

## Problem

Find the equation of the plane containing

$$
(x,y,z)=(1,0,2)+t(1,1,-1)
$$

and the point $P=(0,2,1)$. Check that both the entire line and the point lie in the plane you obtain.

> **Why this exercise:** requires independently constructing two linearly independent directions in the plane.

## Method

A plane containing the line must contain its direction vector.

We obtain a second direction by connecting a point on the line to $P$. If these two directions are independent, their cross product gives a nonzero normal vector and determines a unique plane.

We then use this normal and a known point to write the plane equation.

## Solution

### 1. Construct two directions in the plane

From the line equation, choose the point

$$
A=(1,0,2)
$$

and the direction vector

$$
v=(1,1,-1).
$$

A second vector in the required plane is

$$
\begin{aligned}
w=\overrightarrow{AP}
&=(0-1,\;2-0,\;1-2) \\
&=(-1,2,-1).
\end{aligned}
$$

These vectors are not scalar multiples. If $w=cv$, the first coordinate would require $c=-1$, while the second would require $c=2$.

Thus, the two directions are independent. In particular, $P$ does not lie on the given line, and together they determine a unique plane.

### 2. Find a normal vector

Compute the cross product:

$$
\begin{aligned}
n=v\times w
&=\bigl(
1\cdot(-1)-(-1)\cdot2,\;
(-1)\cdot(-1)-1\cdot(-1),\;
1\cdot2-1\cdot(-1)
\bigr) \\
&=(-1+2,\;1+1,\;2+1) \\
&=(1,2,3).
\end{aligned}
$$

Therefore, a normal vector is

$$
n=(1,2,3).
$$

### 3. Write the plane equation

Using the point $A=(1,0,2)$, the point-normal equation is

$$
(1,2,3)\cdot(x-1,y,z-2)=0.
$$

Expanding,

$$
\begin{aligned}
(x-1)+2y+3(z-2)&=0, \\
x+2y+3z-7&=0.
\end{aligned}
$$

Thus, the required plane is

$$
\Pi:x+2y+3z=7.
$$

## Verification

### 1. Check the entire line

A general point on the line has coordinates

$$
x=1+t,\qquad y=t,\qquad z=2-t.
$$

Substitute these into the plane equation:

$$
\begin{aligned}
x+2y+3z
&=(1+t)+2t+3(2-t) \\
&=1+t+2t+6-3t \\
&=7.
\end{aligned}
$$

This holds for every real $t$, so the entire line lies in the plane.

### 2. Check the point P

Substitute $P=(0,2,1)$:

$$
0+2\cdot2+3\cdot1=4+3=7.
$$

Therefore, $P$ also lies in the plane.

### 3. Check the normal direction

The normal is perpendicular to both constructed directions:

$$
n\cdot v=1\cdot1+2\cdot1+3\cdot(-1)=0,
$$

$$
n\cdot w=1\cdot(-1)+2\cdot2+3\cdot(-1)=0.
$$

These checks confirm that $x+2y+3z=7$ is the plane containing both the given line and the point.
