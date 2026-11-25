# Exercise 5. Relative Position of Two Lines

## Problem

Analyze the position of

$$
L_1:(x,y,z)=(1,1,0)+t(1,2,1),
$$

$$
L_2:(x,y,z)=(2,0,1)+s(0,1,-1).
$$

If they intersect, give the intersection point. If not, determine whether they are parallel or skew. Justify the classification.

> **Why this exercise:** teaches how to distinguish qualitatively different relationships between lines in space.

## Method

First, compare the direction vectors. If they are scalar multiples of each other, the lines are parallel or coincident.

If the directions are not parallel, equate the corresponding coordinates to test for an intersection. A common point must satisfy all three coordinate equations using the same pair of parameter values.

Two lines in space that are neither parallel nor intersecting are skew.

## Solution

### 1. Compare the direction vectors

The direction vectors are

$$
v_1=(1,2,1),
\qquad
v_2=(0,1,-1).
$$

They are not scalar multiples. In particular, every scalar multiple of $v_2$ has first coordinate zero, while $v_1$ has first coordinate 1.

Therefore, the lines are not parallel and cannot coincide.

### 2. Write the coordinate equations

For $L_1$,

$$
\begin{cases}
x=1+t, \\
y=1+2t, \\
z=t.
\end{cases}
$$

For $L_2$,

$$
\begin{cases}
x=2, \\
y=s, \\
z=1-s.
\end{cases}
$$

An intersection would require

$$
\begin{cases}
1+t=2, \\
1+2t=s, \\
t=1-s.
\end{cases}
$$

The parameters $t$ and $s$ are independent; they do not have to equal each other.

### 3. Test for an intersection

The first equation gives

$$
t=1.
$$

Substitute into the second equation:

$$
s=1+2\cdot1=3.
$$

Now check the third equation with these parameter values:

$$
t=1,
\qquad
1-s=1-3=-2.
$$

Since $1\ne-2$, the third equation is not satisfied.

The first two equations force the only possible parameter pair, but that pair fails the third equation. Therefore, the lines do not intersect.

### 4. Classify the lines

The lines have nonparallel direction vectors and no common point. Hence, they are skew.

Geometrically, they do not lie in a common plane: two nonparallel lines in the same plane would intersect.

## Verification

The only point on $L_1$ whose first coordinate is 2 occurs at $t=1$:

$$
\begin{aligned}
L_1(1)
&=(1,1,0)+(1,2,1) \\
&=(2,3,1).
\end{aligned}
$$

On $L_2$, matching the second coordinate 3 requires $s=3$:

$$
\begin{aligned}
L_2(3)
&=(2,0,1)+3(0,1,-1) \\
&=(2,3,-2).
\end{aligned}
$$

These points have different third coordinates, confirming that no intersection exists. Together with the nonparallel directions, this verifies that the lines are skew.
