# Exercise 2. Distance as the Length of a Vector

## Problem

The points are $A=(1,2,3)$ and $B=(4,-2,6)$.

1. Construct $\overrightarrow{AB}$.
2. Compute its length.
3. Compute the distance between the points using the coordinate formula.
4. Explain why both calculations give the same result.

> **Why this exercise:** shows that the point-distance formula comes directly from the length of a difference vector.

## Method

The displacement vector from $A$ to $B$ is obtained by subtracting the coordinates of the starting point from those of the endpoint:

$$
\overrightarrow{AB}=B-A.
$$

For a vector $v=(v_1,v_2,v_3)$, its Euclidean length is

$$
\|v\|=\sqrt{v_1^2+v_2^2+v_3^2}.
$$

The distance between two points is the length of the displacement connecting them.

## Solution

### 1. Construct the displacement vector

Subtract the coordinates of $A$ from those of $B$:

$$
\begin{aligned}
\overrightarrow{AB}
&=(4-1,\;-2-2,\;6-3) \\
&=(3,-4,3).
\end{aligned}
$$

Thus, moving from $A$ to $B$ changes the first coordinate by 3, the second by $-4$, and the third by 3.

### 2. Compute the vector's length

Apply the Euclidean length formula:

$$
\begin{aligned}
\|\overrightarrow{AB}\|
&=\sqrt{3^2+(-4)^2+3^2} \\
&=\sqrt{9+16+9} \\
&=\sqrt{34}.
\end{aligned}
$$

### 3. Compute the distance using coordinates

For points $A=(a_1,a_2,a_3)$ and $B=(b_1,b_2,b_3)$, the distance formula is

$$
d(A,B)=
\sqrt{(b_1-a_1)^2+(b_2-a_2)^2+(b_3-a_3)^2}.
$$

Substituting the given coordinates,

$$
\begin{aligned}
d(A,B)
&=\sqrt{(4-1)^2+(-2-2)^2+(6-3)^2} \\
&=\sqrt{3^2+(-4)^2+3^2} \\
&=\sqrt{34}.
\end{aligned}
$$

### 4. Explain why the results agree

The coordinates of $\overrightarrow{AB}$ are exactly the coordinate differences used in the distance formula. Therefore, the two calculations evaluate the same expression:

$$
d(A,B)=\|B-A\|=\|\overrightarrow{AB}\|.
$$

Geometrically, the coordinate changes occur along three mutually perpendicular axes. The Pythagorean theorem gives the straight-line length by taking the square root of the sum of their squares.

The vector describes both the displacement's direction and its length, while the distance records only the length.

## Verification

Adding the displacement to the starting point recovers the endpoint:

$$
\begin{aligned}
A+\overrightarrow{AB}
&=(1,2,3)+(3,-4,3) \\
&=(4,-2,6) \\
&=B.
\end{aligned}
$$

Reversing the direction gives

$$
\overrightarrow{BA}=(-3,4,-3)=-\overrightarrow{AB}.
$$

Its length is unchanged:

$$
\|\overrightarrow{BA}\|
=\sqrt{(-3)^2+4^2+(-3)^2}
=\sqrt{34}.
$$

This agrees with the fact that the distance from $A$ to $B$ equals the distance from $B$ to $A$.
