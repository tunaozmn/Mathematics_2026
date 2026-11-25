# Exercise 9. Ellipsoid and Its Cross-Sections

## Problem

Consider

$$
\frac{x^2}{9}+\frac{y^2}{4}+\frac{z^2}{16}=1.
$$

Give the semiaxis lengths, describe the cross-section $z=0$, and explain how the cross-sections $z=c$ change for $|c|<4$.

> **Why this exercise:** teaches how to understand a 3D surface through a family of simpler 2D cross-sections.

## Method

An ellipsoid in canonical form has positive squared terms whose denominators are the squares of its semiaxis lengths.

To find a horizontal cross-section, we fix $z=c$ and substitute this value into the equation. The remaining equation describes the intersection in the plane $z=c$.

## Solution

### 1. Identify the center and semiaxis lengths

The equation is already in canonical form. There are no coordinate shifts, so the center is

$$
O=(0,0,0).
$$

The semiaxis lengths are

$$
a_x=\sqrt9=3,\qquad
a_y=\sqrt4=2,\qquad
a_z=\sqrt{16}=4.
$$

Thus, the ellipsoid extends farthest along the z-axis and least along the y-axis.

Its intercepts with the coordinate axes are

$$
(\pm3,0,0),\qquad
(0,\pm2,0),\qquad
(0,0,\pm4).
$$

### 2. Describe the cross-section z = 0

Substitute $z=0$:

$$
\frac{x^2}{9}+\frac{y^2}{4}=1.
$$

This is an ellipse in the xy-plane, centered at $(0,0,0)$, with semiaxis lengths 3 along the x-axis and 2 along the y-axis.

Its endpoints along those directions are

$$
(\pm3,0,0),
\qquad
(0,\pm2,0).
$$

### 3. Find the cross-section z = c

Substitute $z=c$ into the surface equation:

$$
\frac{x^2}{9}+\frac{y^2}{4}+\frac{c^2}{16}=1.
$$

Rearrange:

$$
\frac{x^2}{9}+\frac{y^2}{4}=1-\frac{c^2}{16}.
$$

For $|c|<4$, the right-hand side is positive. Dividing by it gives

$$
\frac{x^2}{9\left(1-\frac{c^2}{16}\right)}
+
\frac{y^2}{4\left(1-\frac{c^2}{16}\right)}
=1.
$$

Therefore, the section is an ellipse in the plane $z=c$, centered at

$$
(0,0,c).
$$

Its semiaxis lengths are

$$
a_x(c)=3\sqrt{1-\frac{c^2}{16}},
\qquad
a_y(c)=2\sqrt{1-\frac{c^2}{16}}.
$$

### 4. Explain how the cross-sections change

Both semiaxis lengths are multiplied by the same factor,

$$
\sqrt{1-\frac{c^2}{16}}.
$$

Consequently, all sections with $|c|<4$ have the same shape and orientation. Their semiaxis ratio remains

$$
\frac{a_x(c)}{a_y(c)}=\frac32.
$$

The section is largest at $c=0$, where the scale factor is 1. As $|c|$ increases toward 4, both semiaxis lengths decrease toward zero.

Since the formulas depend on $c^2$, the sections at heights $c$ and $-c$ have equal sizes.

At the boundary values $c=\pm4$, the section reduces to a single point:

$$
(0,0,4)\qquad\text{or}\qquad(0,0,-4).
$$

For $|c|>4$, the right-hand side is negative, while the left-hand side is nonnegative. Thus, no cross-section exists there.

## Verification

### 1. Check a specific section

Choose $c=2$. Then

$$
1-\frac{c^2}{16}=1-\frac4{16}=\frac34.
$$

The section equation becomes

$$
\frac{x^2}{27/4}+\frac{y^2}{3}=1,
\qquad z=2.
$$

Its semiaxis lengths are

$$
a_x=\frac{3\sqrt3}{2},
\qquad
a_y=\sqrt3.
$$

Check the endpoint $\left(\frac{3\sqrt3}{2},0,2\right)$ in the original equation:

$$
\frac{\left(\frac{3\sqrt3}{2}\right)^2}{9}
+\frac{0^2}{4}
+\frac{2^2}{16}
=\frac34+0+\frac14=1.
$$

### 2. Check the general semiaxis formula

An endpoint of the horizontal semiaxis of the section at height $c$ is

$$
\left(3\sqrt{1-\frac{c^2}{16}},0,c\right).
$$

Substituting it into the ellipsoid equation gives

$$
\frac{9\left(1-\frac{c^2}{16}\right)}9
+0+\frac{c^2}{16}
=1.
$$

This confirms the cross-section formula and its changing scale.
