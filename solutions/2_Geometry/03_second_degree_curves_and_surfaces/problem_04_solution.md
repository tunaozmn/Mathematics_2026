# Exercise 4. Parabola

## Problem

For

$$
y^2=12x,
$$

identify the vertex, axis of symmetry, and opening direction. Find points on the parabola for $x=3$ and use them to make a sketch.

> **Why this exercise:** teaches how to move from the equation of a parabola to its basic geometry.

## Method

The canonical form

$$
y^2=4px
$$

describes a parabola with vertex at the origin and the $x$-axis as its axis of symmetry.

The sign of $p$ determines the opening direction: positive values give a parabola opening right, while negative values give one opening left.

We substitute the specified value of $x$ to obtain points for the sketch.

## Solution

### 1. Identify the vertex

Comparing

$$
y^2=12x
$$

with $y^2=4px$, we obtain

$$
4p=12,\qquad p=3.
$$

There are no coordinate shifts, so the vertex is

$$
V=(0,0).
$$

Indeed, writing the equation as

$$
x=\frac{y^2}{12}
$$

shows that the smallest possible value of $x$ is zero, attained only when $y=0$.

### 2. Identify the axis of symmetry

Replacing $y$ with $-y$ does not change the equation because

$$
(-y)^2=y^2.
$$

Therefore, whenever $(x,y)$ lies on the parabola, so does $(x,-y)$.

The axis of symmetry is consequently

$$
y=0,
$$

which is the $x$-axis.

### 3. Determine the opening direction

Since

$$
x=\frac{y^2}{12}\ge0,
$$

the curve lies entirely in the half-plane $x\ge0$.

As $|y|$ increases, $x$ increases. Thus, the parabola opens to the right, in the positive $x$ direction.

### 4. Find the points for x = 3

Substitute $x=3$:

$$
\begin{aligned}
y^2&=12\cdot3, \\
y^2&=36, \\
y&=\pm6.
\end{aligned}
$$

The two points are

$$
P=(3,6),
\qquad
Q=(3,-6).
$$

They are reflections of each other across the $x$-axis.

### 5. Construct the sketch

Mark the vertex $(0,0)$ and the points $(3,6)$ and $(3,-6)$.

Draw a smooth parabola through these points, symmetric about the $x$-axis and opening to the right. The upper and lower parts meet at the vertex.

The line $x=3$ meets the parabola at the two calculated points and can be used as a guide when placing them.

## Verification

The vertex satisfies the equation:

$$
0^2=12\cdot0=0.
$$

For $P=(3,6)$,

$$
6^2=36=12\cdot3.
$$

For $Q=(3,-6)$,

$$
(-6)^2=36=12\cdot3.
$$

Both points lie on the parabola and have equal horizontal coordinates with opposite vertical coordinates, confirming the symmetry used in the sketch.<img width="1440" height="1440" alt="problem_4_parabola" src="https://github.com/user-attachments/assets/21935eed-cced-4f6a-b386-8dd93b097a73" />
