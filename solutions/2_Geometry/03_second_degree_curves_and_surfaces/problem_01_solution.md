# Exercise 1. Recognizing Curves from Canonical Form

## Problem

Recognize the curves

$$
x^2+y^2=9,
$$

$$
\frac{x^2}{16}+\frac{y^2}{9}=1,
$$

$$
y^2=8x,
$$

$$
\frac{x^2}{9}-\frac{y^2}{4}=1.
$$

For each one, identify the most important features and make a sketch. Explain which parts of the equation let you recognize the type of curve.

> **Why this exercise:** builds the basic dictionary: canonical equation → type of curve → shape and scale.

## Method

We compare each equation with a standard form:

- Equal positive coefficients of $x^2$ and $y^2$ indicate a circle.
- A sum of positive squared terms with different denominators indicates an ellipse.
- One squared variable related to a linear variable indicates a parabola.
- A difference of squared terms equal to 1 indicates a hyperbola.

The constants determine the size, orientation, and key points used in the sketches.

## Solution

### 1. Recognize the circle

The equation

$$
x^2+y^2=9
$$

matches the circle form

$$
(x-h)^2+(y-k)^2=r^2.
$$

Therefore, its center and radius are

$$
(h,k)=(0,0),
\qquad
r=\sqrt9=3.
$$

Its intercepts are

$$
(3,0),\quad(-3,0),\quad(0,3),\quad(0,-3).
$$

Both squared coordinates have the same coefficient, so neither coordinate direction is stretched more than the other. Every point is exactly 3 units from the origin.

For the sketch, mark the four intercepts and draw a circle centered at the origin through them.

### 2. Recognize the ellipse

The equation

$$
\frac{x^2}{16}+\frac{y^2}{9}=1
$$

matches the ellipse form

$$
\frac{x^2}{a^2}+\frac{y^2}{b^2}=1.
$$

Its center is $(0,0)$, and its semiaxis lengths are

$$
a=4 \text{ along the }x\text{-axis},
\qquad
b=3 \text{ along the }y\text{-axis}.
$$

Its intercepts are

$$
(4,0),\quad(-4,0),\quad(0,3),\quad(0,-3).
$$

The full horizontal and vertical axis lengths are 8 and 6. The ellipse is therefore wider horizontally.

The two positive squared terms produce a closed curve. The unequal denominators distinguish this ellipse from a circle.

For the sketch, mark the intercepts and connect them with a smooth oval symmetric about both coordinate axes.

### 3. Recognize the parabola

The equation

$$
y^2=8x
$$

matches the form

$$
y^2=4px.
$$

Since $4p=8$, we have $p=2$. Its features are:

- Vertex: $(0,0)$.
- Axis of symmetry: the $x$-axis.
- Opening direction: positive $x$.
- Focus: $(2,0)$.
- Directrix: $x=-2$.

Only $y$ is squared, while $x$ appears linearly. This identifies a parabola.

Because $y^2\ge0$, every point has $x\ge0$. Replacing $y$ with $-y$ leaves the equation unchanged, explaining the symmetry about the $x$-axis.

To obtain points for the sketch, set $x=2$:

$$
y^2=16,
\qquad
y=\pm4.
$$

Thus, the parabola passes through $(2,4)$ and $(2,-4)$. Draw a smooth curve through these points and the vertex, opening to the right.

### 4. Recognize the hyperbola

The equation

$$
\frac{x^2}{9}-\frac{y^2}{4}=1
$$

matches the hyperbola form

$$
\frac{x^2}{a^2}-\frac{y^2}{b^2}=1.
$$

Here,

$$
a=3,\qquad b=2.
$$

The center is $(0,0)$. Since the positive squared term involves $x$, the two branches open to the left and right.

Setting $y=0$ gives the vertices:

$$
x^2=9,
\qquad
x=\pm3.
$$

Thus, the vertices are $(-3,0)$ and $(3,0)$.

There are no $y$-axis intercepts: setting $x=0$ would require

$$
-\frac{y^2}{4}=1,
$$

which has no real solution.

The asymptotes are

$$
y=\pm\frac{b}{a}x
=\pm\frac23x.
$$

For the sketch, draw these two lines as dashed guides. Draw the branches through the vertices, approaching the asymptotes as they extend away from the center.

## Verification

For the circle, the marked intercepts satisfy the equation. For example,

$$
3^2+0^2=9,
\qquad
0^2+3^2=9.
$$

For the ellipse,

$$
\frac{4^2}{16}+\frac{0^2}{9}=1,
\qquad
\frac{0^2}{16}+\frac{3^2}{9}=1.
$$

For the parabola, the vertex satisfies $0=0$, and the two marked points satisfy

$$
(\pm4)^2=16=8\cdot2.
$$

For the hyperbola, both vertices satisfy

$$
\frac{(\pm3)^2}{9}-\frac{0^2}{4}=1.
$$

Its asymptote slopes also follow from

$$
y^2=\frac49x^2-4.
$$

For $x\ne0$, dividing by $x^2$ gives

$$
\left(\frac{y}{x}\right)^2=\frac49-\frac4{x^2}.
$$

As $|x|$ grows, the final term tends to zero, so the branch directions approach slopes $\pm\frac23$, consistent with the sketch.<img width="2160" height="1980" alt="problem_1_sketches" src="https://github.com/user-attachments/assets/57c034bc-501e-4f35-8fc0-42323e6eaca1" />
