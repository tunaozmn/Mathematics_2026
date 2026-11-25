# Exercise 5. Hyperbola and Asymptotes

## Problem

For

$$
\frac{x^2}{16}-\frac{y^2}{9}=1,
$$

find the intercepts with the $x$-axis, the asymptotes, and make a sketch. Explain why the asymptotes describe the behavior of the curve far from the center.

> **Why this exercise:** shows the role of asymptotes in understanding the global shape of a hyperbola.

## Method

The canonical form

$$
\frac{x^2}{a^2}-\frac{y^2}{b^2}=1
$$

describes a hyperbola centered at the origin with branches opening left and right.

Its $x$-axis intercepts are $(\pm a,0)$, and its asymptotes are

$$
y=\pm\frac{b}{a}x.
$$

We obtain the intercepts directly by setting $y=0$ and explain the asymptotes by examining the equation for large coordinate values.

## Solution

### 1. Identify the basic features

Comparing the given equation with the canonical form,

$$
a^2=16,\qquad b^2=9,
$$

so

$$
a=4,\qquad b=3.
$$

The center is $(0,0)$. The positive squared term involves $x$, so the branches open in the positive and negative $x$ directions.

The equation is unchanged when either coordinate changes sign, so the curve is symmetric about both coordinate axes.

### 2. Find the x-axis intercepts

Set $y=0$:

$$
\begin{aligned}
\frac{x^2}{16}&=1, \\
x^2&=16, \\
x&=\pm4.
\end{aligned}
$$

Therefore, the intercepts are

$$
(-4,0)\qquad\text{and}\qquad(4,0).
$$

These points are also the vertices of the hyperbola.

There are no $y$-axis intercepts because setting $x=0$ would give

$$
-\frac{y^2}{9}=1,
$$

which has no real solution.

### 3. Find the asymptotes

Using $a=4$ and $b=3$, the asymptotes are

$$
y=\frac34x
\qquad\text{and}\qquad
y=-\frac34x.
$$

Their slopes can also be obtained by setting the quadratic part equal to zero:

$$
\frac{x^2}{16}-\frac{y^2}{9}=0.
$$

Rearranging gives

$$
y^2=\frac9{16}x^2,
$$

which describes the two lines above.

### 4. Explain the behavior far from the center

Rearrange the original equation:

$$
y^2=\frac9{16}(x^2-16).
$$

For $x\ge4$, the upper part of the right branch is

$$
y=\frac34\sqrt{x^2-16}.
$$

Compare it with the line $y=\frac34x$. Their vertical separation is

$$
\begin{aligned}
\frac34x-y
&=\frac34\left(x-\sqrt{x^2-16}\right) \\
&=\frac34\cdot
\frac{16}{x+\sqrt{x^2-16}} \\
&=\frac{12}{x+\sqrt{x^2-16}}.
\end{aligned}
$$

As $x$ increases without bound, the denominator increases without bound, so this separation tends to zero.

Thus, the curve approaches the line $y=\frac34x$. By symmetry, the other parts approach the corresponding asymptotes in the same way.

This explains why the asymptotes describe the shape far from the center, even though they are not part of the hyperbola.

### 5. Construct the sketch

Mark the center $(0,0)$ and the vertices $(-4,0)$ and $(4,0)$.

Draw a guide rectangle with corners $(\pm4,\pm3)$. The lines through opposite corners are the asymptotes, with slopes $\pm\frac34$.

Draw two smooth branches through the vertices, opening left and right and approaching the dashed asymptotes.

The curve has no points with $-4<x<4$, because its equation requires

$$
\frac{x^2}{16}=1+\frac{y^2}{9}\ge1.
$$

## Verification

At either vertex,

$$
\frac{(\pm4)^2}{16}-\frac{0^2}{9}=1.
$$

As an additional point check, set $y=3$:

$$
\begin{aligned}
\frac{x^2}{16}-1&=1, \\
x^2&=32, \\
x&=\pm4\sqrt2.
\end{aligned}
$$

Substituting gives

$$
\frac{(\pm4\sqrt2)^2}{16}-\frac{3^2}{9}
=2-1=1.
$$

Finally, points on either asymptote satisfy

$$
\frac{x^2}{16}-\frac{\left(\pm\frac34x\right)^2}{9}
=0,
$$

rather than 1. Therefore, the hyperbola never meets these lines, while the separation calculation shows that its branches approach them.<img width="1800" height="1260" alt="problem_5_hyperbola" src="https://github.com/user-attachments/assets/0c30c3a2-95fd-4c26-8332-802e244e65f0" />
