# Exercise 6. Shifted Ellipse

## Problem

Reduce

$$
4x^2+9y^2-16x+18y-11=0
$$

to canonical form. Give the center and semiaxis lengths. Check that substituting the coordinates of the center into the left-hand side gives a value consistent with the form you obtained.

> **Why this exercise:** reinforces completing the square and recognizing a shift of the coordinate system.

## Method

We group terms by variable, factor out the coefficients of the squared terms, and complete the squares.

Then we divide by the positive constant on the right to obtain the canonical ellipse form:

$$
\frac{(x-h)^2}{a^2}+\frac{(y-k)^2}{b^2}=1.
$$

The center is $(h,k)$, and the horizontal and vertical semiaxis lengths are $a$ and $b$.

## Solution

### 1. Group the terms and factor

Starting from

$$
4x^2+9y^2-16x+18y-11=0,
$$

move the constant to the right and group the remaining terms:

$$
4(x^2-4x)+9(y^2+2y)=11.
$$

### 2. Complete the squares

Use the identities

$$
x^2-4x=(x-2)^2-4,
$$

$$
y^2+2y=(y+1)^2-1.
$$

Substituting gives

$$
4\bigl((x-2)^2-4\bigr)+9\bigl((y+1)^2-1\bigr)=11.
$$

Expand the constant terms:

$$
4(x-2)^2-16+9(y+1)^2-9=11.
$$

Therefore,

$$
4(x-2)^2+9(y+1)^2=36.
$$

### 3. Obtain the canonical form

Divide every term by 36:

$$
\frac{(x-2)^2}{9}+\frac{(y+1)^2}{4}=1.
$$

Both squared terms have positive coefficients, and the right-hand side is positive, so this equation describes an ellipse.

### 4. Identify the center and semiaxes

The center is

$$
C=(2,-1).
$$

The horizontal semiaxis length is

$$
a=\sqrt9=3,
$$

and the vertical semiaxis length is

$$
b=\sqrt4=2.
$$

Thus, the major axis is horizontal. The full horizontal and vertical axis lengths are 6 and 4.

Geometrically, this is the ellipse

$$
\frac{X^2}{9}+\frac{Y^2}{4}=1
$$

translated 2 units to the right and 1 unit downward, with

$$
X=x-2,\qquad Y=y+1.
$$

## Verification

### 1. Evaluate the original left-hand side at the center

Let

$$
F(x,y)=4x^2+9y^2-16x+18y-11.
$$

At $C=(2,-1)$,

$$
\begin{aligned}
F(2,-1)
&=4(2)^2+9(-1)^2-16(2)+18(-1)-11 \\
&=16+9-32-18-11 \\
&=-36.
\end{aligned}
$$

Completing the square also gives the identity

$$
F(x,y)=4(x-2)^2+9(y+1)^2-36.
$$

At the center, both squared terms vanish, so this expression also equals $-36$. The two evaluations agree.

The center is inside the ellipse, not on the curve. Therefore, its substitution is not expected to make the original left-hand side zero. In the canonical equation, the left-hand side at the center is 0, which is less than 1.

### 2. Check the semiaxis endpoints

Moving 3 units horizontally from the center gives $(5,-1)$. In canonical form,

$$
\frac{(5-2)^2}{9}+\frac{(-1+1)^2}{4}
=\frac99+0=1.
$$

Moving 2 units vertically from the center gives $(2,1)$. Then

$$
\frac{(2-2)^2}{9}+\frac{(1+1)^2}{4}
=0+\frac44=1.
$$

These checks confirm the center $(2,-1)$ and semiaxis lengths 3 and 2.
