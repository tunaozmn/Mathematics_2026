# Exercise 7. Classifying a Second-Degree Equation

## Problem

Determine the type of object described by:

1. $4x^2+9y^2=36$,
2. $x^2-y^2=1$,
3. $x^2-4y=0$,
4. $x^2+y^2+1=0$.

In the last case, explain why there are no real points.

> **Why this exercise:** develops quick recognition of the curve type and checking whether real solutions exist.

## Method

We rearrange each equation into a familiar canonical form and inspect the squared terms.

A sum of positive squared terms may describe an ellipse, while a difference of squared terms may describe a hyperbola. A squared variable related to a linear variable gives a parabola.

We also check whether the equation admits real solutions. Recognizing a pattern is not enough if the signs make the equation impossible over the real numbers.

## Solution

### 1. Classify the first equation

The equation is

$$
4x^2+9y^2=36.
$$

Divide by 36:

$$
\frac{x^2}{9}+\frac{y^2}{4}=1.
$$

This is an ellipse centered at $(0,0)$, with horizontal semiaxis length 3 and vertical semiaxis length 2.

The squared terms have positive coefficients, and the unequal denominators give different lengths along the two coordinate axes.

Its intercepts are

$$
(\pm3,0),\qquad(0,\pm2).
$$

### 2. Classify the second equation

The equation

$$
x^2-y^2=1
$$

is already in canonical hyperbola form:

$$
\frac{x^2}{1}-\frac{y^2}{1}=1.
$$

It describes a hyperbola centered at $(0,0)$.

The positive term is $x^2$, so the branches open to the left and right. Its vertices are

$$
(-1,0)\qquad\text{and}\qquad(1,0),
$$

and its asymptotes are

$$
y=x\qquad\text{and}\qquad y=-x.
$$

The opposite signs of the squared terms distinguish it from an ellipse.

### 3. Classify the third equation

Rearrange

$$
x^2-4y=0
$$

as

$$
x^2=4y.
$$

This matches the parabola form $x^2=4py$, with $p=1$.

Therefore, it describes a parabola with:

- Vertex $(0,0)$.
- Axis of symmetry $x=0$, the $y$-axis.
- Opening direction upward, along positive $y$.

Only $x$ is squared, while $y$ appears linearly. Also,

$$
y=\frac{x^2}{4}\ge0,
$$

which confirms the opening direction.

### 4. Classify the fourth equation

Rearranging gives

$$
x^2+y^2=-1.
$$

For all real $x$ and $y$,

$$
x^2\ge0,\qquad y^2\ge0.
$$

Consequently,

$$
x^2+y^2\ge0,
$$

so it cannot equal $-1$.

Thus, the equation has no real points: its real solution set is empty. Although the squared terms resemble a circle equation, there is no real radius whose square is $-1$.

### 5. Summarize the results

| Equation | Classification | Main identifying feature |
| --- | --- | --- |
| $4x^2+9y^2=36$ | Ellipse | Sum of positive squared terms with unequal scales |
| $x^2-y^2=1$ | Hyperbola | Difference of squared terms |
| $x^2-4y=0$ | Parabola | One squared variable and one linear variable |
| $x^2+y^2+1=0$ | No real points | A sum of squares would have to be negative |

## Verification

For the ellipse, the point $(3,0)$ satisfies

$$
4\cdot3^2+9\cdot0^2=36.
$$

For the hyperbola, the point $(1,0)$ satisfies

$$
1^2-0^2=1.
$$

For the parabola, the point $(2,1)$ satisfies

$$
2^2-4\cdot1=0.
$$

For the final equation, its left-hand side always satisfies

$$
x^2+y^2+1\ge1>0.
$$

It therefore never equals zero, confirming that there are no real points.
