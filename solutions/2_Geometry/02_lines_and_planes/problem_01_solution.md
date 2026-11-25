# Exercise 1. Line Through Two Points

## Problem

Find the equation of the line through $A=(1,2)$ and $B=(4,-1)$ in parametric and general form. Identify a direction vector and an example of a normal vector. Check that both points satisfy the equation you obtain.

> **Why this exercise:** teaches how to move between equivalent descriptions of a line and connect them with the appropriate vectors.

## Method

Subtracting the coordinates of two distinct points gives a direction vector for their line.

A parametric equation has the form

$$
(x,y)=A+tv,\qquad t\in\mathbb{R},
$$

where $v$ is a nonzero direction vector.

A normal vector $n$ is perpendicular to $v$. Using this normal and a point on the line, we obtain the general equation from

$$
n\cdot\bigl((x,y)-A\bigr)=0.
$$

## Solution

### 1. Find a direction vector

Compute the displacement from $A$ to $B$:

$$
\begin{aligned}
\overrightarrow{AB}
&=(4-1,\;-1-2) \\
&=(3,-3).
\end{aligned}
$$

Any nonzero scalar multiple gives the same line direction. Dividing by 3, we may use

$$
v=(1,-1).
$$

### 2. Write the parametric equation

Using $A=(1,2)$ as the starting point,

$$
(x,y)=(1,2)+t(1,-1),
\qquad t\in\mathbb{R}.
$$

Equivalently,

$$
\begin{cases}
x=1+t, \\
y=2-t,
\end{cases}
\qquad t\in\mathbb{R}.
$$

As $t$ varies over all real numbers, this describes the entire line.

### 3. Find a normal vector

Choose

$$
n=(1,1).
$$

Its dot product with the direction vector is

$$
n\cdot v=1\cdot1+1\cdot(-1)=0.
$$

Thus, $n$ is perpendicular to the line and is a valid normal vector.

### 4. Obtain the general equation

For a point $(x,y)$ on the line, the displacement from $A$ must be perpendicular to $n$:

$$
n\cdot(x-1,y-2)=0.
$$

Expanding,

$$
\begin{aligned}
1(x-1)+1(y-2)&=0, \\
x+y-3&=0.
\end{aligned}
$$

Therefore, the general form is

$$
x+y-3=0.
$$

The coefficients of $x$ and $y$ are the coordinates of the normal vector $(1,1)$.

## Verification

### 1. Check both points in the general equation

For $A=(1,2)$,

$$
1+2-3=0.
$$

For $B=(4,-1)$,

$$
4+(-1)-3=0.
$$

Both points satisfy the equation.

### 2. Check both points in the parametric equation

At $t=0$,

$$
(1,2)+0(1,-1)=(1,2)=A.
$$

At $t=3$,

$$
(1,2)+3(1,-1)=(4,-1)=B.
$$

### 3. Confirm that the two forms are equivalent

Substitute $x=1+t$ and $y=2-t$ into the general equation:

$$
(1+t)+(2-t)-3=0.
$$

Thus, every point in the parametric description satisfies the general equation.

Conversely, if $x+y-3=0$, set $t=x-1$. Then $x=1+t$ and

$$
y=3-x=3-(1+t)=2-t.
$$

Therefore, both forms describe exactly the same line.
