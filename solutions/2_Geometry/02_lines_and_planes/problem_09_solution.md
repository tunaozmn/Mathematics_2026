# Exercise 9. Distances

## Problem

Compute:

1. the distance from $P=(2,3)$ to the line $3x+4y-10=0$,
2. the distance from $Q=(2,-1,3)$ to the plane $2x-2y+z-4=0$.

Compare the two formulas and explain their common connection with the normal direction.

> **Why this exercise:** organizes two similar formulas through one geometric idea.

## Method

The distance from a point $(x_0,y_0)$ to a line $ax+by+c=0$ is

$$
d=\frac{|ax_0+by_0+c|}{\sqrt{a^2+b^2}}.
$$

The distance from a point $(x_0,y_0,z_0)$ to a plane $ax+by+cz+d_0=0$ is

$$
d=\frac{|ax_0+by_0+cz_0+d_0|}{\sqrt{a^2+b^2+c^2}}.
$$

In both formulas, the denominator is the length of the normal vector. Dividing by it converts the equation's value at the point into a perpendicular distance. The absolute value makes the distance nonnegative.

## Solution

### 1. Find the distance from P to the line

The line is

$$
3x+4y-10=0,
$$

so its normal vector is

$$
n=(3,4).
$$

Its length is

$$
\|n\|=\sqrt{3^2+4^2}=5.
$$

Evaluate the left-hand side at $P=(2,3)$:

$$
3\cdot2+4\cdot3-10=6+12-10=8.
$$

Therefore,

$$
d(P,L)=\frac{|8|}{5}=\frac85.
$$

### 2. Find the distance from Q to the plane

The plane is

$$
2x-2y+z-4=0,
$$

so its normal vector is

$$
m=(2,-2,1).
$$

Its length is

$$
\|m\|=\sqrt{2^2+(-2)^2+1^2}=3.
$$

Evaluate the left-hand side at $Q=(2,-1,3)$:

$$
2\cdot2-2(-1)+3-4=4+2+3-4=5.
$$

Therefore,

$$
d(Q,\Pi)=\frac{|5|}{3}=\frac53.
$$

### 3. Explain the common geometric mechanism

Both a line in the plane and a plane in space can be written as

$$
n\cdot X=k,
$$

using an appropriate nonzero normal vector $n$.

Let $R$ be the point whose distance is required, and let $S$ be any point on the line or plane. Since $n\cdot S=k$,

$$
n\cdot(R-S)=n\cdot R-k.
$$

The component of $R-S$ in the unit normal direction has magnitude

$$
\left|(R-S)\cdot\frac{n}{\|n\|}\right|
=\frac{|n\cdot R-k|}{\|n\|}.
$$

This is the perpendicular distance. The two distance formulas therefore use the same principle; only the number of coordinates changes.

## Verification

### 1. Check the distance to the line

Move from $P$ in the normal direction to reach the line:

$$
\begin{aligned}
H
&=P-\frac{8}{25}(3,4) \\
&=\left(\frac{26}{25},\frac{43}{25}\right).
\end{aligned}
$$

Substitute into the line equation:

$$
3\cdot\frac{26}{25}+4\cdot\frac{43}{25}-10
=\frac{250}{25}-10=0.
$$

Thus, $H$ lies on the line. Also,

$$
P-H=\frac{8}{25}(3,4),
$$

so the displacement is normal to the line and has length

$$
\|P-H\|=\frac{8}{25}\cdot5=\frac85.
$$

### 2. Check the distance to the plane

Similarly, move from $Q$ along the plane normal:

$$
\begin{aligned}
K
&=Q-\frac59(2,-2,1) \\
&=\left(\frac89,\frac19,\frac{22}{9}\right).
\end{aligned}
$$

Substitute into the plane equation:

$$
2\cdot\frac89-2\cdot\frac19+\frac{22}{9}-4
=\frac{36}{9}-4=0.
$$

Thus, $K$ lies in the plane. The displacement is

$$
Q-K=\frac59(2,-2,1),
$$

which is normal to the plane and has length

$$
\|Q-K\|=\frac59\cdot3=\frac53.
$$

These perpendicular displacements confirm both calculated distances.
