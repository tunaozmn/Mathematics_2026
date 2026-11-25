# Exercise 2. Circle by Completing the Square

## Problem

Reduce

$$
x^2+y^2-6x+4y-3=0
$$

to canonical form. Find the center and radius, then substitute two simple points from the circle into both forms of the equation.

> **Why this exercise:** practices completing the square as a transition from a general equation to the geometry of the object.

## Method

We group the terms involving each variable and complete the square.

The canonical equation of a circle is

$$
(x-h)^2+(y-k)^2=r^2,
$$

where $(h,k)$ is the center and $r>0$ is the radius.

After identifying these values, we choose two points by moving one radius horizontally from the center and check them in both equations.

## Solution

### 1. Group the terms

Starting from

$$
x^2+y^2-6x+4y-3=0,
$$

move the constant to the right and group by variable:

$$
(x^2-6x)+(y^2+4y)=3.
$$

### 2. Complete the squares

For the terms involving $x$,

$$
x^2-6x=(x-3)^2-9.
$$

For the terms involving $y$,

$$
y^2+4y=(y+2)^2-4.
$$

Substitute these identities:

$$
(x-3)^2-9+(y+2)^2-4=3.
$$

Adding 13 to both sides gives the canonical form:

$$
(x-3)^2+(y+2)^2=16.
$$

### 3. Identify the center and radius

Comparing with $(x-h)^2+(y-k)^2=r^2$, we obtain

$$
h=3,\qquad k=-2,\qquad r=\sqrt{16}=4.
$$

Therefore, the circle has center

$$
C=(3,-2)
$$

and radius 4.

The sign in $y+2=y-(-2)$ shows that the center's second coordinate is $-2$.

### 4. Choose two simple points

Move 4 units to the right and left of the center:

$$
P=(3+4,-2)=(7,-2),
$$

$$
Q=(3-4,-2)=(-1,-2).
$$

Each point is exactly one radius from the center.

## Verification

### 1. Check P in both forms

For $P=(7,-2)$, the canonical equation gives

$$
(7-3)^2+(-2+2)^2=4^2+0^2=16.
$$

In the original equation,

$$
\begin{aligned}
7^2+(-2)^2-6\cdot7+4(-2)-3
&=49+4-42-8-3 \\
&=0.
\end{aligned}
$$

Thus, $P$ satisfies both forms.

### 2. Check Q in both forms

For $Q=(-1,-2)$, the canonical equation gives

$$
(-1-3)^2+(-2+2)^2=(-4)^2+0^2=16.
$$

In the original equation,

$$
\begin{aligned}
(-1)^2+(-2)^2-6(-1)+4(-2)-3
&=1+4+6-8-3 \\
&=0.
\end{aligned}
$$

Thus, $Q$ also satisfies both forms.

### 3. Confirm algebraic equivalence

Expanding the canonical equation gives

$$
\begin{aligned}
(x-3)^2+(y+2)^2&=16, \\
x^2-6x+9+y^2+4y+4&=16, \\
x^2+y^2-6x+4y-3&=0.
\end{aligned}
$$

This recovers the original equation, confirming the center $(3,-2)$ and radius 4.
