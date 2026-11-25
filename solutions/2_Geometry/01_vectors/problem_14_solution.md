# Exercise 14. Closest Point on a Line

## Problem

Given a point $P=(4,1)$ and a line through the origin with direction $v=(1,2)$. Using projection, find the closest point on the line, the distance from $P$ to the line, and verify that the appropriate vector is perpendicular to the direction of the line.

> **Why this exercise:** shows projection as a complete solution to a minimum-distance problem.

## Method

Let $O=(0,0)$ and use the position vector

$$
p=\overrightarrow{OP}=(4,1).
$$

The closest point $Q$ is obtained by projecting $p$ onto the direction $v$:

$$
\overrightarrow{OQ}=\frac{p\cdot v}{v\cdot v}\,v.
$$

The vector from $Q$ to $P$ is perpendicular to the line, and its length is the distance from $P$ to the line.

## Solution

### 1. Calculate the projection coefficient

The required dot products are

$$
p\cdot v=4\cdot1+1\cdot2=6,
$$

and

$$
v\cdot v=1^2+2^2=5.
$$

Therefore,

$$
\frac{p\cdot v}{v\cdot v}=\frac65.
$$

### 2. Find the closest point

The projected position vector is

$$
\begin{aligned}
\overrightarrow{OQ}
&=\frac65(1,2) \\
&=\left(\frac65,\frac{12}{5}\right).
\end{aligned}
$$

Thus, the closest point is

$$
Q=\left(\frac65,\frac{12}{5}\right).
$$

Since its position vector is a scalar multiple of $v$, this point lies on the given line.

### 3. Find the perpendicular displacement

Subtract the coordinates of $Q$ from those of $P$:

$$
\begin{aligned}
\overrightarrow{QP}
&=P-Q \\
&=\left(4-\frac65,\;1-\frac{12}{5}\right) \\
&=\left(\frac{14}{5},-\frac75\right).
\end{aligned}
$$

Check its dot product with the line direction:

$$
\begin{aligned}
\overrightarrow{QP}\cdot v
&=\frac{14}{5}\cdot1-\frac75\cdot2 \\
&=\frac{14}{5}-\frac{14}{5} \\
&=0.
\end{aligned}
$$

Therefore, the segment from $Q$ to $P$ is perpendicular to the line.

### 4. Calculate the distance

The distance is the length of this perpendicular displacement:

$$
\begin{aligned}
d
&=\|\overrightarrow{QP}\| \\
&=\sqrt{\left(\frac{14}{5}\right)^2+
\left(-\frac75\right)^2} \\
&=\sqrt{\frac{196+49}{25}} \\
&=\frac{\sqrt{245}}5 \\
&=\frac{7\sqrt5}{5}.
\end{aligned}
$$

### 5. Explain why Q is the closest point

Let $R$ be any other point on the line. The vector $\overrightarrow{QR}$ is parallel to the line, while $\overrightarrow{QP}$ is perpendicular to it.

Thus, triangle $PQR$ is right-angled at $Q$. By the Pythagorean theorem,

$$
\|P-R\|^2=\|P-Q\|^2+\|Q-R\|^2.
$$

Since $\|Q-R\|^2$ is nonnegative,

$$
\|P-R\|^2\ge\|P-Q\|^2.
$$

Equality occurs only when $R=Q$. Therefore, $Q$ is the unique closest point on the line.

## Verification

The line has equation $y=2x$. For the proposed point $Q$,

$$
\frac{12}{5}=2\cdot\frac65,
$$

so $Q$ is on the line.

The perpendicularity calculation above gives

$$
\overrightarrow{QP}\cdot v=0.
$$

Finally, adding the projected vector and the perpendicular remainder reconstructs $p$:

$$
\begin{aligned}
\overrightarrow{OQ}+\overrightarrow{QP}
&=\left(\frac65,\frac{12}{5}\right)
+\left(\frac{14}{5},-\frac75\right) \\
&=(4,1) \\
&=p.
\end{aligned}
$$

These checks confirm the closest point and the distance:

$$
Q=\left(\frac65,\frac{12}{5}\right),
\qquad
d=\frac{7\sqrt5}{5}.
$$
