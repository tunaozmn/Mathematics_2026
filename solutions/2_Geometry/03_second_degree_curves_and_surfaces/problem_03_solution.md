# Exercise 3. Ellipse

## Problem

For

$$
\frac{x^2}{25}+\frac{y^2}{9}=1,
$$

find the semiaxis lengths, the intercepts with the coordinate axes, and make a sketch. Explain along which axis the ellipse is more stretched and how this is visible in the equation.

> **Why this exercise:** teaches how to read the size and orientation of an ellipse without additional conceptual machinery.

## Method

For an ellipse in the form

$$
\frac{x^2}{a^2}+\frac{y^2}{b^2}=1,
$$

the center is the origin, and the semiaxis lengths along the coordinate axes are $a$ and $b$.

We obtain the intercepts by setting one coordinate equal to zero. These points, together with the symmetry of the equation, determine the basic sketch.

## Solution

### 1. Identify the center and semiaxis lengths

Comparing the given equation with the canonical form gives

$$
a^2=25,\qquad b^2=9.
$$

Taking the positive square roots,

$$
a=5,\qquad b=3.
$$

Thus, the ellipse has:

- Center $(0,0)$.
- Horizontal semiaxis length 5.
- Vertical semiaxis length 3.

The full horizontal axis has length 10, and the full vertical axis has length 6.

### 2. Find the x-axis intercepts

On the $x$-axis, $y=0$. Therefore,

$$
\begin{aligned}
\frac{x^2}{25}&=1, \\
x^2&=25, \\
x&=\pm5.
\end{aligned}
$$

The intercepts are

$$
(-5,0)\qquad\text{and}\qquad(5,0).
$$

### 3. Find the y-axis intercepts

On the $y$-axis, $x=0$. Therefore,

$$
\begin{aligned}
\frac{y^2}{9}&=1, \\
y^2&=9, \\
y&=\pm3.
\end{aligned}
$$

The intercepts are

$$
(0,-3)\qquad\text{and}\qquad(0,3).
$$

### 4. Explain the orientation and shape

The ellipse is more stretched along the $x$-axis because its horizontal semiaxis, 5, is longer than its vertical semiaxis, 3.

This is visible in the equation: the denominator beneath $x^2$ is larger than the denominator beneath $y^2$. These denominators are the squares of the corresponding semiaxis lengths.

The major axis is therefore horizontal, and the minor axis is vertical.

Because both variables are squared, changing the sign of either coordinate leaves the equation unchanged. Hence, the ellipse is symmetric about both coordinate axes.

### 5. Construct the sketch

Mark the center and the four intercepts:

$$
(0,0),\qquad
(\pm5,0),\qquad
(0,\pm3).
$$

Draw a smooth closed oval through the four intercepts, symmetric about both axes and wider horizontally than vertically.

Use the same coordinate scale on both axes so that the semiaxis lengths are represented accurately.

## Verification

At the horizontal intercepts,

$$
\frac{(\pm5)^2}{25}+\frac{0^2}{9}
=\frac{25}{25}=1.
$$

At the vertical intercepts,

$$
\frac{0^2}{25}+\frac{(\pm3)^2}{9}
=\frac99=1.
$$

Thus, all four intercepts satisfy the equation.

Also, both terms in the original equation are nonnegative, so each is at most 1:

$$
\frac{x^2}{25}\le1,
\qquad
\frac{y^2}{9}\le1.
$$

Therefore,

$$
|x|\le5,\qquad |y|\le3.
$$

These bounds agree with the intercepts and confirm the horizontal and vertical extent of the sketch.<img width="1620" height="1170" alt="problem_3_ellipse" src="https://github.com/user-attachments/assets/31bed50a-93cb-4363-9d08-19760e3780e1" />
