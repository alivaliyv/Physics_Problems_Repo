# Problem Set 01 – Solutions

# Task 01 – Vectors and Linear Transformations

## Problem Statement

Given the vectors

$$
\vec a = (2,-1,3),
\qquad
\vec b = (1,4,-2)
$$

determine their lengths, the normalized vector $\hat a$, the dot product, the angle between them, the cross product, and the area of the parallelogram spanned by them.

For the matrix

$$
A =
\begin{pmatrix}
2 & 1 & 0 \\
0 & 1 & -1 \\
1 & 0 & 1
\end{pmatrix}
$$

determine $A\vec a$, the determinant $\det A$, and whether the transformation preserves orientation.

## Theory

For a vector $\vec v = (v_1,v_2,v_3)$, its Euclidean norm is

$$
|\vec v| = \sqrt{v_1^2 + v_2^2 + v_3^2}.
$$

A normalized vector has unit length:

$$
\hat v = \frac{\vec v}{|\vec v|}.
$$

The dot product of two vectors is

$$
\vec a \cdot \vec b = a_1 b_1 + a_2 b_2 + a_3 b_3.
$$

The angle $\theta$ between vectors is determined by

$$
\vec a \cdot \vec b = |\vec a| |\vec b| \cos \theta.
$$

The cross product is

$$
\vec a \times \vec b =
\begin{pmatrix}
a_2 b_3 - a_3 b_2 \\
a_3 b_1 - a_1 b_3 \\
a_1 b_2 - a_2 b_1
\end{pmatrix}.
$$

Its magnitude equals the area of the parallelogram spanned by the vectors:

$$
|\vec a \times \vec b| = |\vec a| |\vec b| \sin \theta.
$$

For a linear transformation represented by a matrix $A$, the determinant gives the oriented volume scaling factor. If $\det A > 0$, orientation is preserved. If $\det A < 0$, orientation is reversed.

## Step-by-Step Solution

### Vector lengths

For $\vec a = (2,-1,3)$,

$$
|\vec a| = \sqrt{2^2 + (-1)^2 + 3^2}
= \sqrt{4 + 1 + 9}
= \sqrt{14}.
$$

For $\vec b = (1,4,-2)$,

$$
|\vec b| = \sqrt{1^2 + 4^2 + (-2)^2}
= \sqrt{1 + 16 + 4}
= \sqrt{21}.
$$

### Normalized vector $\hat a$

By definition,

$$
\hat a = \frac{\vec a}{|\vec a|}.
$$

Therefore,

$$
\hat a = \frac{1}{\sqrt{14}} (2,-1,3)
=
\left(
\frac{2}{\sqrt{14}},
-\frac{1}{\sqrt{14}},
\frac{3}{\sqrt{14}}
\right).
$$

### Dot product

Compute

$$
\vec a \cdot \vec b
= 2 \cdot 1 + (-1) \cdot 4 + 3 \cdot (-2).
$$

Thus,

$$
\vec a \cdot \vec b = 2 - 4 - 6 = -8.
$$

### Angle between the vectors

Use

$$
\cos \theta = \frac{\vec a \cdot \vec b}{|\vec a| |\vec b|}.
$$

Substituting the values,

$$
\cos \theta = \frac{-8}{\sqrt{14}\sqrt{21}} = \frac{-8}{\sqrt{294}}.
$$

Hence,

$$
\theta = \arccos \left( \frac{-8}{\sqrt{294}} \right).
$$

Numerically,

$$
\sqrt{294} \approx 17.146,
\qquad
\cos \theta \approx -0.4666,
$$

so

$$
\theta \approx 2.056 \text{ rad} \approx 117.8^\circ.
$$

### Cross product

Using the determinant form,

$$
\vec a \times \vec b =
\begin{pmatrix}
(-1)(-2) - 3 \cdot 4 \\
3 \cdot 1 - 2(-2) \\
2 \cdot 4 - (-1)\cdot 1
\end{pmatrix}.
$$

Compute each component:

$$
\vec a \times \vec b =
\begin{pmatrix}
2 - 12 \\
3 + 4 \\
8 + 1
\end{pmatrix}
=
\begin{pmatrix}
-10 \\
7 \\
9
\end{pmatrix}.
$$

### Area of the parallelogram

The area is the magnitude of the cross product:

$$
|\vec a \times \vec b|
= \sqrt{(-10)^2 + 7^2 + 9^2}
= \sqrt{100 + 49 + 81}
= \sqrt{230}.
$$

### Matrix-vector product $A \vec a$

Compute row by row:

$$
A\vec a =
\begin{pmatrix}
2 & 1 & 0 \\
0 & 1 & -1 \\
1 & 0 & 1
\end{pmatrix}
\begin{pmatrix}
2 \\
-1 \\
3
\end{pmatrix}.
$$

First component:

$$
2 \cdot 2 + 1 \cdot (-1) + 0 \cdot 3 = 4 - 1 = 3.
$$

Second component:

$$
0 \cdot 2 + 1 \cdot (-1) + (-1)\cdot 3 = -1 - 3 = -4.
$$

Third component:

$$
1 \cdot 2 + 0 \cdot (-1) + 1 \cdot 3 = 2 + 3 = 5.
$$

Therefore,

$$
A\vec a =
\begin{pmatrix}
3 \\
-4 \\
5
\end{pmatrix}.
$$

### Determinant of $A$

Expand along the first row:

$$
\det A
=
2
\begin{vmatrix}
1 & -1 \\
0 & 1
\end{vmatrix}
-
1
\begin{vmatrix}
0 & -1 \\
1 & 1
\end{vmatrix}
+
0
\begin{vmatrix}
0 & 1 \\
1 & 0
\end{vmatrix}.
$$

Evaluate the minors:

$$
\begin{vmatrix}
1 & -1 \\
0 & 1
\end{vmatrix}
= 1 \cdot 1 - (-1)\cdot 0 = 1,
$$

$$
\begin{vmatrix}
0 & -1 \\
1 & 1
\end{vmatrix}
= 0 \cdot 1 - (-1)\cdot 1 = 1.
$$

Hence,

$$
\det A = 2 \cdot 1 - 1 \cdot 1 = 1.
$$

### Orientation of the transformation

Since

$$
\det A = 1 > 0,
$$

the transformation preserves orientation.

## Final Result

$$
|\vec a| = \sqrt{14},
\qquad
|\vec b| = \sqrt{21}
$$

$$
\hat a =
\left(
\frac{2}{\sqrt{14}},
-\frac{1}{\sqrt{14}},
\frac{3}{\sqrt{14}}
\right)
$$

$$
\vec a \cdot \vec b = -8
$$

$$
\theta = \arccos \left( \frac{-8}{\sqrt{294}} \right)
\approx 117.8^\circ
$$

$$
\vec a \times \vec b = (-10,7,9)
$$

$$
\text{Area} = \sqrt{230}
$$

$$
A\vec a = (3,-4,5)
$$

$$
\det A = 1
$$

The transformation preserves orientation.

## Interpretation

The negative dot product shows that the angle between $\vec a$ and $\vec b$ is obtuse. The nonzero cross product confirms that the vectors are not parallel and therefore span a genuine parallelogram with area $\sqrt{230}$. The determinant equal to $1$ means that the matrix transformation preserves both orientation and volume.

# Task 02 – Parametric Trajectory, Velocity, and Acceleration

## Problem Statement

For the parametric curve

$$
\vec r(t) = \bigl(t^2,\sin t,5\bigr),
$$

determine the velocity, acceleration, the speed at $t=1$, the scalar product $\vec v \cdot \vec a$, and the cross product $\vec v \times \vec a$. A visualization of the trajectory and selected velocity and acceleration vectors is also required.

## Theory

For a trajectory $\vec r(t)$, the velocity and acceleration are defined by

$$
\vec v(t) = \frac{d\vec r}{dt},
\qquad
\vec a(t) = \frac{d^2 \vec r}{dt^2}.
$$

The speed is the magnitude of the velocity:

$$
|\vec v(t)| = \sqrt{\vec v(t)\cdot \vec v(t)}.
$$

The scalar product $\vec v \cdot \vec a$ measures the rate of change of the squared speed:

$$
\frac{d}{dt} |\vec v|^2 = 2 \vec v \cdot \vec a.
$$

The cross product $\vec v \times \vec a$ is related to the turning of the motion in space.

## Step-by-Step Solution

### Position vector

The trajectory is

$$
\vec r(t) =
\begin{pmatrix}
t^2 \\
\sin t \\
5
\end{pmatrix}.
$$

### Velocity

Differentiate componentwise:

$$
\vec v(t)
=
\frac{d}{dt}
\begin{pmatrix}
t^2 \\
\sin t \\
5
\end{pmatrix}
=
\begin{pmatrix}
2t \\
\cos t \\
0
\end{pmatrix}.
$$

Thus,

$$
\vec v(t) = (2t,\cos t,0).
$$

### Acceleration

Differentiate again:

$$
\vec a(t)
=
\frac{d}{dt}
\begin{pmatrix}
2t \\
\cos t \\
0
\end{pmatrix}
=
\begin{pmatrix}
2 \\
-\sin t \\
0
\end{pmatrix}.
$$

Thus,

$$
\vec a(t) = (2,-\sin t,0).
$$

### Speed at $t=1$

At $t=1$,

$$
\vec v(1) = (2,\cos 1,0).
$$

Its magnitude is

$$
|\vec v(1)|
=
\sqrt{2^2 + (\cos 1)^2 + 0^2}
=
\sqrt{4 + \cos^2 1}.
$$

Numerically, since $\cos 1 \approx 0.5403$,

$$
|\vec v(1)| \approx \sqrt{4 + 0.2919} \approx \sqrt{4.2919} \approx 2.072.
$$

### Scalar product $\vec v \cdot \vec a$

Compute

$$
\vec v(t) \cdot \vec a(t)
=
(2t,\cos t,0)\cdot(2,-\sin t,0).
$$

Therefore,

$$
\vec v(t)\cdot \vec a(t)
=
4t - \sin t \cos t.
$$

Using the double-angle identity,

$$
\sin t \cos t = \frac{1}{2} \sin(2t),
$$

one may also write

$$
\vec v(t)\cdot \vec a(t) = 4t - \frac{1}{2}\sin(2t).
$$

### Cross product $\vec v \times \vec a$

Using the determinant formula,

$$
\vec v(t)\times \vec a(t)
=
\begin{pmatrix}
2t \\
\cos t \\
0
\end{pmatrix}
\times
\begin{pmatrix}
2 \\
-\sin t \\
0
\end{pmatrix}.
$$

Since both vectors lie in the $xy$ plane, only the $z$ component is nonzero:

$$
\vec v(t)\times \vec a(t)
=
\begin{pmatrix}
0 \\
0 \\
(2t)(-\sin t) - (\cos t)(2)
\end{pmatrix}.
$$

Hence,

$$
\vec v(t)\times \vec a(t)
=
\bigl(0,0,-2t\sin t - 2\cos t\bigr).
$$

Factoring out $-2$ gives

$$
\vec v(t)\times \vec a(t)
=
\bigl(0,0,-2(t\sin t + \cos t)\bigr).
$$

## Final Result

$$
\vec v(t) = (2t,\cos t,0)
$$

$$
\vec a(t) = (2,-\sin t,0)
$$

$$
|\vec v(1)| = \sqrt{4 + \cos^2 1} \approx 2.072
$$

$$
\vec v(t)\cdot \vec a(t) = 4t - \sin t \cos t
$$

$$
\vec v(t)\times \vec a(t) = \bigl(0,0,-2t\sin t - 2\cos t\bigr)
$$

## Interpretation

The motion takes place in the plane $z=5$. The $x$ coordinate grows quadratically, while the $y$ coordinate oscillates sinusoidally. The velocity and acceleration both remain in the same plane. The cross product points only in the $z$ direction, which reflects the planar nature of the motion. The value of $\vec v \cdot \vec a$ is not constant, so the speed changes with time.

### Visualization in HTML/JS

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Trajectory, Velocity, Acceleration</title>
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>
<body>
  <h2>Trajectory in the plane z = 5</h2>
  <canvas id="trajChart" width="700" height="450"></canvas>

  <script>
    const tMin = -2;
    const tMax = 2;
    const steps = 200;
    const points = [];
    const sampleTs = [-1.5, -0.5, 0.5, 1.5];

    function r(t) {
      return { x: t*t, y: Math.sin(t) };
    }

    function v(t) {
      return { x: 2*t, y: Math.cos(t) };
    }

    function a(t) {
      return { x: 2, y: -Math.sin(t) };
    }

    for (let i = 0; i <= steps; i++) {
      const t = tMin + (tMax - tMin) * i / steps;
      points.push(r(t));
    }

    const datasets = [
      {
        label: "Trajectory",
        data: points,
        parsing: false,
        showLine: true,
        pointRadius: 0
      }
    ];

    const scaleVel = 0.25;
    const scaleAcc = 0.25;

    sampleTs.forEach((t, idx) => {
      const p = r(t);
      const vv = v(t);
      const aa = a(t);

      datasets.push({
        label: `v(t=${t})`,
        data: [
          { x: p.x, y: p.y },
          { x: p.x + scaleVel * vv.x, y: p.y + scaleVel * vv.y }
        ],
        parsing: false,
        showLine: true,
        pointRadius: [4, 0]
      });

      datasets.push({
        label: `a(t=${t})`,
        data: [
          { x: p.x, y: p.y },
          { x: p.x + scaleAcc * aa.x, y: p.y + scaleAcc * aa.y }
        ],
        parsing: false,
        showLine: true,
        pointRadius: [4, 0]
      });
    });

    new Chart(document.getElementById("trajChart"), {
      type: "scatter",
      data: { datasets },
      options: {
        responsive: false,
        scales: {
          x: { type: "linear", title: { display: true, text: "x(t) = t^2" } },
          y: { title: { display: true, text: "y(t) = sin t" } }
        }
      }
    });
  </script>
</body>
</html>
```

# Task 03 – Integration of Motion

## Problem Statement

### Part A

Given

$$
\vec v(t) = \bigl(2t,3,-e^{-t}\bigr),
\qquad
\vec r(0) = (0,1,2),
$$

determine the position vector $\vec r(t)$ and the acceleration $\vec a(t)$.

### Part B

Given

$$
\vec a(t) = \bigl(4,-\sin t,0\bigr),
\qquad
\vec v(0) = (1,0,2),
\qquad
\vec r(0) = (0,0,0),
$$

determine $\vec v(t)$ and $\vec r(t)$.

## Theory

Velocity is the derivative of position:

$$
\vec v(t) = \frac{d\vec r}{dt}.
$$

Therefore position is obtained by integration:

$$
\vec r(t) = \vec r(0) + \int_0^t \vec v(\tau)\, d\tau.
$$

Similarly, acceleration is the derivative of velocity:

$$
\vec a(t) = \frac{d\vec v}{dt}.
$$

If acceleration is known, then

$$
\vec v(t) = \vec v(0) + \int_0^t \vec a(\tau)\, d\tau.
$$

## Step-by-Step Solution

### Part A – Position from velocity

The velocity is

$$
\vec v(t) = (2t,3,-e^{-t}).
$$

Then

$$
\vec r(t) = \vec r(0) + \int_0^t \vec v(\tau)\, d\tau.
$$

Insert the data:

$$
\vec r(t)
=
(0,1,2)
+
\int_0^t
\bigl(2\tau,3,-e^{-\tau}\bigr)\, d\tau.
$$

Integrate componentwise:

$$
\int_0^t 2\tau \, d\tau
=
\left[\tau^2\right]_0^t
=
t^2,
$$

$$
\int_0^t 3 \, d\tau
=
\left[3\tau\right]_0^t
=
3t,
$$

$$
\int_0^t -e^{-\tau} \, d\tau
=
\left[e^{-\tau}\right]_0^t
=
e^{-t} - 1.
$$

Thus,

$$
\vec r(t)
=
(0,1,2)
+
\bigl(t^2,3t,e^{-t}-1\bigr).
$$

Therefore,

$$
\vec r(t)
=
\bigl(t^2,1+3t,1+e^{-t}\bigr).
$$

To verify the third component:

$$
2 + (e^{-t}-1) = 1 + e^{-t}.
$$

### Part A – Acceleration

Differentiate $\vec v(t)$:

$$
\vec a(t)
=
\frac{d}{dt}(2t,3,-e^{-t})
=
(2,0,e^{-t}).
$$

### Part B – Velocity from acceleration

The acceleration is

$$
\vec a(t) = (4,-\sin t,0).
$$

Then

$$
\vec v(t)
=
\vec v(0)
+
\int_0^t \vec a(\tau)\, d\tau.
$$

Substitute the data:

$$
\vec v(t)
=
(1,0,2)
+
\int_0^t (4,-\sin \tau,0)\, d\tau.
$$

Compute the integrals:

$$
\int_0^t 4 \, d\tau = 4t,
$$

$$
\int_0^t -\sin \tau \, d\tau
=
\left[\cos \tau\right]_0^t
=
\cos t - 1,
$$

$$
\int_0^t 0 \, d\tau = 0.
$$

Hence,

$$
\vec v(t)
=
(1,0,2) + (4t,\cos t - 1,0).
$$

So,

$$
\vec v(t)
=
(1+4t,\cos t - 1,2).
$$

### Part B – Position from velocity

Now integrate velocity:

$$
\vec r(t)
=
\vec r(0) + \int_0^t \vec v(\tau)\, d\tau.
$$

Since $\vec r(0) = (0,0,0)$,

$$
\vec r(t)
=
\int_0^t (1+4\tau,\cos \tau - 1,2)\, d\tau.
$$

Integrate componentwise:

$$
\int_0^t (1+4\tau)\, d\tau
=
\left[\tau + 2\tau^2\right]_0^t
=
t + 2t^2,
$$

$$
\int_0^t (\cos \tau - 1)\, d\tau
=
\left[\sin \tau - \tau\right]_0^t
=
\sin t - t,
$$

$$
\int_0^t 2 \, d\tau = 2t.
$$

Therefore,

$$
\vec r(t)
=
\bigl(t+2t^2,\sin t - t,2t\bigr).
$$

## Final Result

### Part A

$$
\vec r(t) = \bigl(t^2,1+3t,1+e^{-t}\bigr)
$$

$$
\vec a(t) = (2,0,e^{-t})
$$

### Part B

$$
\vec v(t) = (1+4t,\cos t - 1,2)
$$

$$
\vec r(t) = \bigl(t+2t^2,\sin t - t,2t\bigr)
$$

## Interpretation

Part A shows direct reconstruction of motion from a known velocity field. The $z$ component approaches $1$ as $t \to \infty$ because $e^{-t} \to 0$. In Part B, the constant positive $x$ acceleration produces quadratic growth in the $x$ coordinate, while the $y$ motion reflects the oscillatory acceleration $-\sin t$.

# Task 04 – Geometry of Parametric Curves

## Problem Statement

For each parametric curve:

1. Eliminate the parameter if possible.
2. Determine the type of curve.
3. Determine the velocity and acceleration.
4. Check whether $|\vec v|$ or $|\vec a|$ is constant.

The curves are:

A) $x(t)=R\cos t$, $y(t)=R\sin t$

B) $x(t)=a\cos t$, $y(t)=b\sin t$

C) $x(t)=t$, $y(t)=t^2$

D) $x(t)=\cosh t$, $y(t)=\sinh t$

## Theory

For a planar curve $\vec r(t) = (x(t),y(t))$, the velocity and acceleration are

$$
\vec v(t) = (x'(t),y'(t)),
\qquad
\vec a(t) = (x''(t),y''(t)).
$$

The magnitudes are

$$
|\vec v(t)| = \sqrt{x'(t)^2 + y'(t)^2},
\qquad
|\vec a(t)| = \sqrt{x''(t)^2 + y''(t)^2}.
$$

## Step-by-Step Solution

### A) Circle

The curve is

$$
x(t)=R\cos t,
\qquad
y(t)=R\sin t.
$$

#### Elimination of the parameter

Using $\cos^2 t + \sin^2 t = 1$,

$$
\left(\frac{x}{R}\right)^2 + \left(\frac{y}{R}\right)^2 = 1.
$$

Hence,

$$
x^2 + y^2 = R^2.
$$

This is a circle of radius $R$ centered at the origin.

#### Velocity and acceleration

$$
\vec v(t) = (-R\sin t, R\cos t),
$$

$$
\vec a(t) = (-R\cos t, -R\sin t).
$$

#### Magnitudes

$$
|\vec v(t)|
=
\sqrt{R^2 \sin^2 t + R^2 \cos^2 t}
=
R.
$$

Thus the speed is constant.

Similarly,

$$
|\vec a(t)|
=
\sqrt{R^2 \cos^2 t + R^2 \sin^2 t}
=
R.
$$

The acceleration magnitude is also constant.

### B) Ellipse

The curve is

$$
x(t)=a\cos t,
\qquad
y(t)=b\sin t.
$$

#### Elimination of the parameter

Using

$$
\cos t = \frac{x}{a},
\qquad
\sin t = \frac{y}{b},
$$

and the identity $\cos^2 t + \sin^2 t = 1$,

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1.
$$

This is an ellipse centered at the origin.

#### Velocity and acceleration

$$
\vec v(t) = (-a\sin t, b\cos t),
$$

$$
\vec a(t) = (-a\cos t, -b\sin t).
$$

#### Magnitudes

$$
|\vec v(t)| = \sqrt{a^2 \sin^2 t + b^2 \cos^2 t}.
$$

This is constant only if $a=b$.

Also,

$$
|\vec a(t)| = \sqrt{a^2 \cos^2 t + b^2 \sin^2 t}.
$$

This is also constant only if $a=b$.

### C) Parabola

The curve is

$$
x(t)=t,
\qquad
y(t)=t^2.
$$

#### Elimination of the parameter

Since $x=t$, substitute into $y$:

$$
y=x^2.
$$

This is a parabola.

#### Velocity and acceleration

$$
\vec v(t) = (1,2t),
$$

$$
\vec a(t) = (0,2).
$$

#### Magnitudes

$$
|\vec v(t)| = \sqrt{1 + 4t^2}.
$$

This is not constant.

For acceleration,

$$
|\vec a(t)| = \sqrt{0^2 + 2^2} = 2.
$$

Thus the acceleration magnitude is constant.

### D) Hyperbola

The curve is

$$
x(t)=\cosh t,
\qquad
y(t)=\sinh t.
$$

#### Elimination of the parameter

Use the identity

$$
\cosh^2 t - \sinh^2 t = 1.
$$

Therefore,

$$
x^2 - y^2 = 1.
$$

This is a hyperbola.

#### Velocity and acceleration

$$
\vec v(t) = (\sinh t,\cosh t),
$$

$$
\vec a(t) = (\cosh t,\sinh t).
$$

#### Magnitudes

$$
|\vec v(t)|
=
\sqrt{\sinh^2 t + \cosh^2 t}
=
\sqrt{\cosh(2t)}.
$$

This is not constant.

Similarly,

$$
|\vec a(t)|
=
\sqrt{\cosh^2 t + \sinh^2 t}
=
\sqrt{\cosh(2t)}.
$$

This is not constant.

## Final Result

### A) Circle

$$
x^2 + y^2 = R^2
$$

$$
\vec v(t)=(-R\sin t,R\cos t),
\qquad
\vec a(t)=(-R\cos t,-R\sin t)
$$

$$
|\vec v| = R,
\qquad
|\vec a| = R
$$

### B) Ellipse

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1
$$

$$
\vec v(t)=(-a\sin t,b\cos t),
\qquad
\vec a(t)=(-a\cos t,-b\sin t)
$$

$$
|\vec v| = \sqrt{a^2 \sin^2 t + b^2 \cos^2 t}
$$

$$
|\vec a| = \sqrt{a^2 \cos^2 t + b^2 \sin^2 t}
$$

### C) Parabola

$$
y = x^2
$$

$$
\vec v(t)=(1,2t),
\qquad
\vec a(t)=(0,2)
$$

$$
|\vec v| = \sqrt{1+4t^2},
\qquad
|\vec a| = 2
$$

### D) Hyperbola

$$
x^2 - y^2 = 1
$$

$$
\vec v(t)=(\sinh t,\cosh t),
\qquad
\vec a(t)=(\cosh t,\sinh t)
$$

$$
|\vec v| = \sqrt{\cosh(2t)},
\qquad
|\vec a| = \sqrt{\cosh(2t)}
$$

## Interpretation

The circle is the only curve among the four with both constant speed and constant acceleration magnitude for the chosen parameterization. The ellipse reduces to the circle when $a=b$. The parabola has constant acceleration magnitude, but its speed grows with $|t|$. The hyperbola has neither constant speed nor constant acceleration magnitude, reflecting its non-periodic geometry.

# Task 05 – Trajectory Curvature and Normal Acceleration

## Problem Statement

For the ellipse

$$
x = a\cos t,
\qquad
y = b\sin t,
$$

determine the velocity and acceleration, the unit tangent vector, the tangential and normal components of acceleration, the normal acceleration magnitude, and the radius of curvature at $t=0$. Compare the result with the circular case $a=b$.

## Theory

For a planar motion, the velocity and acceleration are

$$
\vec v(t) = (x'(t),y'(t)),
\qquad
\vec a(t) = (x''(t),y''(t)).
$$

The unit tangent vector is

$$
\hat T(t) = \frac{\vec v(t)}{|\vec v(t)|}.
$$

The tangential component of acceleration is parallel to $\hat T$:

$$
\vec a_t = \left( \frac{\vec a \cdot \vec v}{|\vec v|^2} \right)\vec v.
$$

The normal component is

$$
\vec a_n = \vec a - \vec a_t.
$$

Its magnitude can also be obtained from

$$
a_n = \frac{|\vec v \times \vec a|}{|\vec v|}.
$$

For planar motion,

$$
R = \frac{v^2}{a_n}
$$

is the radius of curvature.

## Step-by-Step Solution

### Velocity and acceleration

The position vector is

$$
\vec r(t) = (a\cos t, b\sin t).
$$

Differentiate:

$$
\vec v(t) = (-a\sin t, b\cos t).
$$

Differentiate again:

$$
\vec a(t) = (-a\cos t, -b\sin t).
$$

### Speed

The speed is

$$
|\vec v(t)| = \sqrt{a^2 \sin^2 t + b^2 \cos^2 t}.
$$

### Unit tangent vector

Therefore,

$$
\hat T(t)
=
\frac{1}{\sqrt{a^2 \sin^2 t + b^2 \cos^2 t}}
(-a\sin t, b\cos t).
$$

### Tangential component of acceleration

First compute $\vec a \cdot \vec v$:

$$
\vec a \cdot \vec v
=
(-a\cos t)(-a\sin t) + (-b\sin t)(b\cos t).
$$

Hence,

$$
\vec a \cdot \vec v
=
a^2 \sin t \cos t - b^2 \sin t \cos t
=
(a^2 - b^2)\sin t \cos t.
$$

Also,

$$
|\vec v|^2 = a^2 \sin^2 t + b^2 \cos^2 t.
$$

Thus,

$$
\vec a_t
=
\left(
\frac{(a^2-b^2)\sin t \cos t}{a^2 \sin^2 t + b^2 \cos^2 t}
\right)
(-a\sin t, b\cos t).
$$

### Normal component of acceleration

The normal component is

$$
\vec a_n = \vec a - \vec a_t.
$$

A more compact formula for its magnitude is obtained from the cross product.

Embed the vectors in $\mathbb R^3$:

$$
\vec v = (-a\sin t,b\cos t,0),
\qquad
\vec a = (-a\cos t,-b\sin t,0).
$$

Then

$$
\vec v \times \vec a
=
\begin{pmatrix}
0 \\
0 \\
(-a\sin t)(-b\sin t) - (b\cos t)(-a\cos t)
\end{pmatrix}.
$$

So,

$$
\vec v \times \vec a
=
\begin{pmatrix}
0 \\
0 \\
ab(\sin^2 t + \cos^2 t)
\end{pmatrix}
=
\begin{pmatrix}
0 \\
0 \\
ab
\end{pmatrix}.
$$

Therefore,

$$
|\vec v \times \vec a| = ab.
$$

Hence,

$$
a_n(t)
=
\frac{|\vec v \times \vec a|}{|\vec v|}
=
\frac{ab}{\sqrt{a^2 \sin^2 t + b^2 \cos^2 t}}.
$$

### Radius of curvature at $t=0$

At $t=0$,

$$
\vec v(0) = (0,b),
\qquad
|\vec v(0)| = b.
$$

Also,

$$
a_n(0) = \frac{ab}{\sqrt{a^2 \cdot 0 + b^2 \cdot 1}} = \frac{ab}{b} = a.
$$

Now use

$$
R = \frac{v^2}{a_n}.
$$

At $t=0$,

$$
R(0) = \frac{b^2}{a}.
$$

### Comparison with the circle

If $a=b=R_0$, then the ellipse becomes a circle of radius $R_0$.

The normal acceleration becomes

$$
a_n = \frac{R_0^2}{\sqrt{R_0^2}} = R_0.
$$

Also,

$$
R(0) = \frac{R_0^2}{R_0} = R_0.
$$

Thus the radius of curvature equals the geometric radius, as expected for a circle.

## Final Result

$$
\vec v(t)=(-a\sin t,b\cos t)
$$

$$
\vec a(t)=(-a\cos t,-b\sin t)
$$

$$
\hat T(t)
=
\frac{1}{\sqrt{a^2 \sin^2 t + b^2 \cos^2 t}}
(-a\sin t,b\cos t)
$$

$$
\vec a_t
=
\left(
\frac{(a^2-b^2)\sin t \cos t}{a^2 \sin^2 t + b^2 \cos^2 t}
\right)
(-a\sin t,b\cos t)
$$

$$
a_n(t)
=
\frac{ab}{\sqrt{a^2 \sin^2 t + b^2 \cos^2 t}}
$$

$$
R(0)=\frac{b^2}{a}
$$

For the circle $a=b=R_0$,

$$
R(0)=R_0.
$$

## Interpretation

A greater curvature corresponds to a smaller radius of curvature and therefore, at fixed speed, to a greater normal acceleration because

$$
a_n = \frac{v^2}{R}.
$$

For the ellipse, the point $t=0$ is $(a,0)$, the end of the major semi-axis if $a>b$. There the radius of curvature is

$$
R(0)=\frac{b^2}{a},
$$

which is relatively small when $a$ is large compared with $b$. Therefore the ellipse is more strongly curved at the ends of the major semi-axis. Normal acceleration changes the direction of the velocity vector without directly changing its magnitude; for this reason it is interpreted as the part of the acceleration responsible for turning the motion.

# Task 06 – Curve Length and Numerical Integration

## Problem Statement

For the trajectory

$$
x(t)=t,
\qquad
y(t)=t^2,
\qquad
t \in [0,1],
$$

determine the velocity, the speed, and the arc length. Then formulate a numerical trapezoidal-rule approximation and provide an HTML/JS implementation with visualization and error analysis.

## Theory

For a parametric curve $\vec r(t)$, the arc length from $t=a$ to $t=b$ is

$$
s = \int_a^b |\vec r'(t)|\, dt.
$$

For the trapezoidal rule with $N$ subintervals and step size

$$
h = \frac{b-a}{N},
$$

the approximation is

$$
\int_a^b f(t)\, dt
\approx
h
\left[
\frac{f(t_0)}{2}
+
\sum_{k=1}^{N-1} f(t_k)
+
\frac{f(t_N)}{2}
\right].
$$

## Step-by-Step Solution

### Velocity

The position vector is

$$
\vec r(t) = (t,t^2).
$$

Differentiate:

$$
\vec v(t) = \frac{d\vec r}{dt} = (1,2t).
$$

### Speed

The speed is

$$
|\vec v(t)| = \sqrt{1^2 + (2t)^2} = \sqrt{1+4t^2}.
$$

### Arc length integral

Thus,

$$
s = \int_0^1 \sqrt{1+4t^2}\, dt.
$$

### Analytical evaluation

Use the substitution

$$
u = 2t,
\qquad
dt = \frac{du}{2}.
$$

The limits change as follows:

$$
t=0 \Rightarrow u=0,
\qquad
t=1 \Rightarrow u=2.
$$

Hence,

$$
s = \frac{1}{2} \int_0^2 \sqrt{1+u^2}\, du.
$$

Use the standard integral

$$
\int \sqrt{1+u^2}\, du
=
\frac{1}{2}
\left(
u\sqrt{1+u^2} + \ln\left|u+\sqrt{1+u^2}\right|
\right).
$$

Therefore,

$$
s
=
\frac{1}{2}
\cdot
\frac{1}{2}
\left[
u\sqrt{1+u^2} + \ln\left(u+\sqrt{1+u^2}\right)
\right]_0^2.
$$

So,

$$
s
=
\frac{1}{4}
\left(
2\sqrt{5} + \ln(2+\sqrt{5})
\right).
$$

At $u=0$, the logarithmic term is $\ln 1 = 0$, so no extra constant remains.

Thus,

$$
s
=
\frac{\sqrt{5}}{2}
+
\frac{1}{4}\ln(2+\sqrt{5}).
$$

Numerically,

$$
s \approx 1.47894.
$$

### Trapezoidal-rule approximation

Let

$$
f(t)=\sqrt{1+4t^2}.
$$

For $N$ subintervals on $[0,1]$,

$$
h = \frac{1}{N},
\qquad
t_k = kh.
$$

Then

$$
s_N
=
h
\left[
\frac{f(0)}{2}
+
\sum_{k=1}^{N-1} f(t_k)
+
\frac{f(1)}{2}
\right].
$$

The numerical error is

$$
E_N = |s_N - s|.
$$

## Final Result

$$
\vec v(t) = (1,2t)
$$

$$
|\vec v(t)| = \sqrt{1+4t^2}
$$

$$
s = \int_0^1 \sqrt{1+4t^2}\, dt
$$

$$
s
=
\frac{\sqrt{5}}{2}
+
\frac{1}{4}\ln(2+\sqrt{5})
\approx 1.47894
$$

Trapezoidal approximation:

$$
s_N
=
\frac{1}{N}
\left[
\frac{f(0)}{2}
+
\sum_{k=1}^{N-1} f\left(\frac{k}{N}\right)
+
\frac{f(1)}{2}
\right]
$$

with

$$
f(t)=\sqrt{1+4t^2}.
$$

## Interpretation

The length of the parabola segment is larger than the straight-line distance between the endpoints because the curve bends upward as $t$ increases. The speed grows monotonically with $t$, so equal parameter intervals do not correspond to equal spatial distances. The trapezoidal rule converges as $N$ increases because the integrand is smooth on the closed interval $[0,1]$.

### HTML/JS Implementation

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Arc Length of y = x^2 on [0,1]</title>
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>
<body>
  <h2>Arc length of the curve x=t, y=t^2</h2>

  <label for="N">Number of trapezoids N:</label>
  <input type="range" id="N" min="2" max="200" value="20" />
  <span id="Nval">20</span>

  <p id="results"></p>

  <canvas id="curveChart" width="700" height="350"></canvas>
  <canvas id="errorChart" width="700" height="350"></canvas>

  <script>
    const exact = Math.sqrt(5)/2 + 0.25*Math.log(2 + Math.sqrt(5));

    function f(t) {
      return Math.sqrt(1 + 4*t*t);
    }

    function trapezoidal(N) {
      const h = 1 / N;
      let sum = 0.5 * f(0) + 0.5 * f(1);
      for (let k = 1; k < N; k++) {
        sum += f(k * h);
      }
      return h * sum;
    }

    function curvePoints() {
      const pts = [];
      for (let i = 0; i <= 200; i++) {
        const t = i / 200;
        pts.push({ x: t, y: t*t });
      }
      return pts;
    }

    function sampleCurvePoints(N) {
      const pts = [];
      for (let k = 0; k <= N; k++) {
        const t = k / N;
        pts.push({ x: t, y: t*t });
      }
      return pts;
    }

    const curveChart = new Chart(document.getElementById("curveChart"), {
      type: "scatter",
      data: {
        datasets: [
          {
            label: "Curve",
            data: curvePoints(),
            parsing: false,
            showLine: true,
            pointRadius: 0
          },
          {
            label: "Trapezoid nodes",
            data: sampleCurvePoints(20),
            parsing: false,
            showLine: true,
            pointRadius: 3
          }
        ]
      },
      options: {
        responsive: false,
        scales: {
          x: { type: "linear", title: { display: true, text: "x" } },
          y: { title: { display: true, text: "y" } }
        }
      }
    });

    const errorData = [];
    for (let N = 2; N <= 200; N++) {
      const approx = trapezoidal(N);
      errorData.push({ x: N, y: Math.abs(approx - exact) });
    }

    new Chart(document.getElementById("errorChart"), {
      type: "scatter",
      data: {
        datasets: [
          {
            label: "Error |s_N - s|",
            data: errorData,
            parsing: false,
            showLine: true,
            pointRadius: 0
          }
        ]
      },
      options: {
        responsive: false,
        scales: {
          x: { type: "linear", title: { display: true, text: "N" } },
          y: { title: { display: true, text: "Absolute error" } }
        }
      }
    });

    function update() {
      const N = Number(document.getElementById("N").value);
      document.getElementById("Nval").textContent = N;
      const approx = trapezoidal(N);
      const error = Math.abs(approx - exact);

      document.getElementById("results").innerHTML =
        `Exact length: ${exact.toFixed(8)}<br>` +
        `Trapezoidal approximation: ${approx.toFixed(8)}<br>` +
        `Absolute error: ${error.toExponential(6)}`;

      curveChart.data.datasets[1].data = sampleCurvePoints(N);
      curveChart.update();
    }

    document.getElementById("N").addEventListener("input", update);
    update();
  </script>
</body>
</html>
```

# Task 07 – Work of a Force Along a Trajectory

## Problem Statement

Given the force field

$$
\vec F(x,y) = (y,2x)
$$

and the trajectory

$$
x=t,
\qquad
y=t^2,
\qquad
t \in [0,1],
$$

determine the velocity and calculate the work

$$
W = \int_C \vec F \cdot d\vec r.
$$

Also express the integral as a Riemann sum and formulate a numerical implementation.

## Theory

For a parametrized curve $\vec r(t)$, the line integral of a force is

$$
W = \int_{t_0}^{t_1} \vec F(\vec r(t)) \cdot \vec r'(t)\, dt.
$$

A Riemann-sum approximation has the form

$$
W \approx \sum_{k=0}^{N-1} \vec F(\vec r(t_k)) \cdot \Delta \vec r_k.
$$

## Step-by-Step Solution

### Velocity vector

The trajectory is

$$
\vec r(t) = (t,t^2).
$$

Differentiate:

$$
\vec v(t) = \vec r'(t) = (1,2t).
$$

### Force along the trajectory

Substitute $x=t$ and $y=t^2$ into $\vec F(x,y)$:

$$
\vec F(\vec r(t)) = (t^2, 2t).
$$

### Work integral

Now compute

$$
W = \int_0^1 \vec F(\vec r(t)) \cdot \vec r'(t)\, dt.
$$

The dot product is

$$
\vec F(\vec r(t)) \cdot \vec r'(t)
=
(t^2,2t)\cdot(1,2t)
=
t^2 + 4t^2
=
5t^2.
$$

Hence,

$$
W = \int_0^1 5t^2\, dt.
$$

Integrating,

$$
W = 5 \left[\frac{t^3}{3}\right]_0^1 = \frac{5}{3}.
$$

### Riemann-sum form

Partition $[0,1]$ into $N$ subintervals:

$$
\Delta t = \frac{1}{N},
\qquad
t_k = \frac{k}{N}.
$$

Then

$$
\Delta \vec r_k \approx \vec r'(t_k)\Delta t.
$$

Thus,

$$
W
\approx
\sum_{k=0}^{N-1}
\vec F(\vec r(t_k))\cdot \vec r'(t_k)\Delta t.
$$

Since

$$
\vec F(\vec r(t_k))\cdot \vec r'(t_k) = 5 t_k^2,
$$

the approximation becomes

$$
W_N
=
\sum_{k=0}^{N-1} 5\left(\frac{k}{N}\right)^2 \frac{1}{N}.
$$

As $N \to \infty$,

$$
W_N \to \frac{5}{3}.
$$

## Final Result

$$
\vec v(t) = (1,2t)
$$

$$
\vec F(\vec r(t)) = (t^2,2t)
$$

$$
W = \int_0^1 5t^2\, dt = \frac{5}{3}
$$

Riemann sum:

$$
W_N
=
\sum_{k=0}^{N-1} 5\left(\frac{k}{N}\right)^2 \frac{1}{N}
$$

and

$$
\lim_{N \to \infty} W_N = \frac{5}{3}.
$$

## Interpretation

The force does positive work along the entire path because the scalar product $\vec F \cdot \vec v = 5t^2$ is nonnegative on $[0,1]$. Therefore the force transfers energy to the moving particle throughout the motion.

### HTML/JS Implementation

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Work Along a Curve</title>
</head>
<body>
  <h2>Work of the force F(x,y) = (y, 2x)</h2>

  <label for="N">Number of intervals N:</label>
  <input id="N" type="range" min="2" max="500" value="20" />
  <span id="Nval">20</span>

  <p id="output"></p>

  <script>
    const exact = 5 / 3;

    function r(t) {
      return { x: t, y: t*t };
    }

    function v(t) {
      return { x: 1, y: 2*t };
    }

    function F(x, y) {
      return { x: y, y: 2*x };
    }

    function riemannWork(N) {
      const dt = 1 / N;
      let sum = 0;
      for (let k = 0; k < N; k++) {
        const t = k / N;
        const pos = r(t);
        const vel = v(t);
        const force = F(pos.x, pos.y);
        sum += (force.x * vel.x + force.y * vel.y) * dt;
      }
      return sum;
    }

    function update() {
      const N = Number(document.getElementById("N").value);
      document.getElementById("Nval").textContent = N;
      const approx = riemannWork(N);
      const error = Math.abs(approx - exact);

      document.getElementById("output").innerHTML =
        `Analytical result: ${exact.toFixed(8)}<br>` +
        `Riemann-sum approximation: ${approx.toFixed(8)}<br>` +
        `Absolute error: ${error.toExponential(6)}`;
    }

    document.getElementById("N").addEventListener("input", update);
    update();
  </script>
</body>
</html>
```

# Task 08 – First-Order Differential Equation

## Problem Statement

Solve the differential equation

$$
\frac{dy}{dt} = -k y
$$

and provide an HTML/JS visualization for different values of $k$ and initial conditions $y(0)$.

## Theory

This is a first-order linear differential equation with separable variables. It may be rewritten as

$$
\frac{1}{y}\, dy = -k\, dt.
$$

Integrating both sides yields the general solution.

## Step-by-Step Solution

### Separation of variables

Start from

$$
\frac{dy}{dt} = -k y.
$$

Assume $y \neq 0$ and separate variables:

$$
\frac{1}{y} dy = -k\, dt.
$$

Integrate:

$$
\int \frac{1}{y}\, dy = \int -k\, dt.
$$

Therefore,

$$
\ln |y| = -kt + C.
$$

Exponentiate:

$$
|y| = e^{C} e^{-kt}.
$$

Since $e^C$ is a positive constant, absorb the sign into a new constant $C_1$:

$$
y(t) = C_1 e^{-kt}.
$$

### Application of the initial condition

If

$$
y(0)=y_0,
$$

then

$$
y_0 = C_1 e^0 = C_1.
$$

Thus,

$$
y(t)=y_0 e^{-kt}.
$$

## Final Result

General solution:

$$
y(t)=C e^{-kt}
$$

Solution with initial condition $y(0)=y_0$:

$$
y(t)=y_0 e^{-kt}
$$

## Interpretation

If $k>0$, the solution decays exponentially toward zero. If $k<0$, the solution grows exponentially. If $k=0$, the solution is constant. The parameter $k$ therefore controls the characteristic time scale of decay or growth.

### HTML/JS Implementation

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Exponential Decay and Growth</title>
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>
<body>
  <h2>Solution of dy/dt = -k y</h2>

  <label for="k">k:</label>
  <input id="k" type="range" min="-3" max="3" step="0.1" value="1" />
  <span id="kVal">1</span>

  <label for="y0">y(0):</label>
  <input id="y0" type="range" min="-5" max="5" step="0.1" value="2" />
  <span id="y0Val">2</span>

  <canvas id="chart" width="700" height="400"></canvas>

  <script>
    function solution(t, k, y0) {
      return y0 * Math.exp(-k * t);
    }

    const chart = new Chart(document.getElementById("chart"), {
      type: "scatter",
      data: {
        datasets: [{
          label: "y(t)",
          data: [],
          parsing: false,
          showLine: true,
          pointRadius: 0
        }]
      },
      options: {
        responsive: false,
        scales: {
          x: { type: "linear", title: { display: true, text: "t" } },
          y: { title: { display: true, text: "y(t)" } }
        }
      }
    });

    function update() {
      const k = Number(document.getElementById("k").value);
      const y0 = Number(document.getElementById("y0").value);
      document.getElementById("kVal").textContent = k;
      document.getElementById("y0Val").textContent = y0;

      const data = [];
      for (let i = 0; i <= 300; i++) {
        const t = 5 * i / 300;
        data.push({ x: t, y: solution(t, k, y0) });
      }

      chart.data.datasets[0].data = data;
      chart.update();
    }

    document.getElementById("k").addEventListener("input", update);
    document.getElementById("y0").addEventListener("input", update);
    update();
  </script>
</body>
</html>
```

# Task 09 – Harmonic Oscillator

## Problem Statement

Solve the equation

$$
\frac{d^2 x}{dt^2} + \omega^2 x = 0
$$

find the general solution, determine the solution for given initial conditions, and provide an HTML/JS visualization of $x(t)$, $x'(t)$, and $x''(t)$.

## Theory

This is the equation of the simple harmonic oscillator. The standard method is to solve the characteristic equation

$$
\lambda^2 + \omega^2 = 0.
$$

The roots are purely imaginary:

$$
\lambda = \pm i\omega.
$$

Therefore the motion is oscillatory.

## Step-by-Step Solution

### General solution

The general solution is

$$
x(t) = C_1 \cos(\omega t) + C_2 \sin(\omega t).
$$

Differentiate:

$$
x'(t) = -C_1 \omega \sin(\omega t) + C_2 \omega \cos(\omega t),
$$

$$
x''(t) = -C_1 \omega^2 \cos(\omega t) - C_2 \omega^2 \sin(\omega t).
$$

Thus,

$$
x''(t) = -\omega^2 x(t),
$$

which verifies the differential equation.

### Solution for initial conditions

Let

$$
x(0) = x_0,
\qquad
x'(0)=v_0.
$$

From the general solution,

$$
x(0) = C_1 \cos 0 + C_2 \sin 0 = C_1.
$$

Hence,

$$
C_1 = x_0.
$$

Now evaluate the derivative at $t=0$:

$$
x'(0)
=
-C_1 \omega \sin 0 + C_2 \omega \cos 0
=
C_2 \omega.
$$

Thus,

$$
C_2 = \frac{v_0}{\omega}.
$$

Therefore the solution satisfying the initial conditions is

$$
x(t) = x_0 \cos(\omega t) + \frac{v_0}{\omega}\sin(\omega t).
$$

Its derivatives are

$$
x'(t) = -x_0 \omega \sin(\omega t) + v_0 \cos(\omega t),
$$

$$
x''(t) = -\omega^2 x_0 \cos(\omega t) - \omega v_0 \sin(\omega t).
$$

Using the equation of motion, one may also write

$$
x''(t) = -\omega^2 x(t).
$$

## Final Result

General solution:

$$
x(t) = C_1 \cos(\omega t) + C_2 \sin(\omega t)
$$

For initial conditions $x(0)=x_0$ and $x'(0)=v_0$:

$$
x(t) = x_0 \cos(\omega t) + \frac{v_0}{\omega}\sin(\omega t)
$$

$$
x'(t) = -x_0 \omega \sin(\omega t) + v_0 \cos(\omega t)
$$

$$
x''(t) = -\omega^2 x(t)
$$

## Interpretation

The system oscillates periodically around the equilibrium point $x=0$. The parameter $\omega$ controls the angular frequency, so larger $\omega$ produces faster oscillations. The acceleration is always directed toward the equilibrium position and is proportional to the displacement with opposite sign.

### HTML/JS Implementation

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Harmonic Oscillator</title>
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>
<body>
  <h2>Harmonic oscillator</h2>

  <label for="omega">omega:</label>
  <input id="omega" type="range" min="0.5" max="5" step="0.1" value="2" />
  <span id="omegaVal">2</span>

  <label for="x0">x(0):</label>
  <input id="x0" type="range" min="-5" max="5" step="0.1" value="1" />
  <span id="x0Val">1</span>

  <label for="v0">x'(0):</label>
  <input id="v0" type="range" min="-5" max="5" step="0.1" value="0" />
  <span id="v0Val">0</span>

  <canvas id="xChart" width="700" height="300"></canvas>
  <canvas id="vChart" width="700" height="300"></canvas>
  <canvas id="aChart" width="700" height="300"></canvas>

  <script>
    function x(t, omega, x0, v0) {
      return x0 * Math.cos(omega * t) + (v0 / omega) * Math.sin(omega * t);
    }

    function v(t, omega, x0, v0) {
      return -x0 * omega * Math.sin(omega * t) + v0 * Math.cos(omega * t);
    }

    function a(t, omega, x0, v0) {
      return -omega * omega * x(t, omega, x0, v0);
    }

    function makeChart(canvasId, label, yLabel) {
      return new Chart(document.getElementById(canvasId), {
        type: "scatter",
        data: {
          datasets: [{
            label,
            data: [],
            parsing: false,
            showLine: true,
            pointRadius: 0
          }]
        },
        options: {
          responsive: false,
          scales: {
            x: { type: "linear", title: { display: true, text: "t" } },
            y: { title: { display: true, text: yLabel } }
          }
        }
      });
    }

    const xChart = makeChart("xChart", "x(t)", "x");
    const vChart = makeChart("vChart", "x'(t)", "x'");
    const aChart = makeChart("aChart", "x''(t)", "x''");

    function buildData(fn, omega, x0, v0) {
      const data = [];
      for (let i = 0; i <= 500; i++) {
        const t = 10 * i / 500;
        data.push({ x: t, y: fn(t, omega, x0, v0) });
      }
      return data;
    }

    function update() {
      const omega = Number(document.getElementById("omega").value);
      const x0 = Number(document.getElementById("x0").value);
      const v0 = Number(document.getElementById("v0").value);

      document.getElementById("omegaVal").textContent = omega;
      document.getElementById("x0Val").textContent = x0;
      document.getElementById("v0Val").textContent = v0;

      xChart.data.datasets[0].data = buildData(x, omega, x0, v0);
      vChart.data.datasets[0].data = buildData(v, omega, x0, v0);
      aChart.data.datasets[0].data = buildData(a, omega, x0, v0);

      xChart.update();
      vChart.update();
      aChart.update();
    }

    document.getElementById("omega").addEventListener("input", update);
    document.getElementById("x0").addEventListener("input", update);
    document.getElementById("v0").addEventListener("input", update);
    update();
  </script>
</body>
</html>
```

# Task 10 – Angular Momentum in Circular Motion

## Problem Statement

For the motion

$$
\vec r(t)=\bigl(R\cos(\omega t),R\sin(\omega t),0\bigr),
$$

determine the velocity, calculate the angular momentum

$$
\vec L(t) = m\, \vec r(t)\times \vec v(t),
$$

show that its magnitude is constant, interpret its direction, and verify the torque relation for a centripetal force.

## Theory

Angular momentum with respect to the origin is

$$
\vec L = \vec r \times \vec p = m\, \vec r \times \vec v.
$$

Torque is defined by

$$
\vec \tau = \vec r \times \vec F.
$$

In general,

$$
\vec \tau = \frac{d\vec L}{dt}.
$$

## Step-by-Step Solution

### Velocity

Differentiate the position vector:

$$
\vec v(t)
=
\frac{d}{dt}
\bigl(R\cos(\omega t),R\sin(\omega t),0\bigr).
$$

Thus,

$$
\vec v(t)
=
\bigl(-R\omega \sin(\omega t), R\omega \cos(\omega t), 0\bigr).
$$

### Angular momentum

Compute the cross product:

$$
\vec r \times \vec v
=
\begin{pmatrix}
R\cos(\omega t) \\
R\sin(\omega t) \\
0
\end{pmatrix}
\times
\begin{pmatrix}
-R\omega \sin(\omega t) \\
R\omega \cos(\omega t) \\
0
\end{pmatrix}.
$$

Only the $z$ component is nonzero:

$$
(\vec r \times \vec v)_z
=
R\cos(\omega t)\cdot R\omega \cos(\omega t)
-
R\sin(\omega t)\cdot \bigl(-R\omega \sin(\omega t)\bigr).
$$

Therefore,

$$
(\vec r \times \vec v)_z
=
R^2 \omega \cos^2(\omega t) + R^2 \omega \sin^2(\omega t)
=
R^2 \omega.
$$

Hence,

$$
\vec r \times \vec v = (0,0,R^2\omega).
$$

Multiplying by $m$ gives

$$
\vec L(t) = (0,0,mR^2\omega).
$$

### Magnitude of angular momentum

The magnitude is

$$
|\vec L| = mR^2\omega.
$$

This is constant because $m$, $R$, and $\omega$ are constants.

### Direction of $\vec L$

The vector points along the positive $z$ axis when $\omega > 0$, corresponding to counterclockwise motion in the $xy$ plane. This agrees with the right-hand rule: curling the fingers in the direction of motion makes the thumb point along $\vec L$.

If $\omega < 0$, the direction reverses to the negative $z$ axis.

### Optional part – Centripetal force and torque

For uniform circular motion, the acceleration is

$$
\vec a(t) = \frac{d\vec v}{dt}
=
\bigl(-R\omega^2 \cos(\omega t), -R\omega^2 \sin(\omega t), 0\bigr).
$$

Thus the centripetal force is

$$
\vec F = m\vec a
=
\bigl(-mR\omega^2 \cos(\omega t), -mR\omega^2 \sin(\omega t), 0\bigr).
$$

This force is parallel to $-\vec r(t)$, so

$$
\vec \tau = \vec r \times \vec F = \vec 0.
$$

Now differentiate angular momentum:

$$
\frac{d\vec L}{dt}
=
\frac{d}{dt}(0,0,mR^2\omega)
=
\vec 0.
$$

Hence,

$$
\vec \tau = \frac{d\vec L}{dt} = \vec 0.
$$

## Final Result

$$
\vec v(t)=\bigl(-R\omega \sin(\omega t),R\omega \cos(\omega t),0\bigr)
$$

$$
\vec L(t)=(0,0,mR^2\omega)
$$

$$
|\vec L|=mR^2\omega
$$

For the centripetal force,

$$
\vec F(t)=\bigl(-mR\omega^2 \cos(\omega t),-mR\omega^2 \sin(\omega t),0\bigr)
$$

$$
\vec \tau = \vec r \times \vec F = \vec 0
$$

and

$$
\frac{d\vec L}{dt} = \vec 0.
$$

Therefore,

$$
\vec \tau = \frac{d\vec L}{dt}.
$$

## Interpretation

Uniform circular motion has constant angular momentum because the position and velocity vectors remain perpendicular and their magnitudes remain constant. The angular momentum vector is perpendicular to the plane of motion. A purely centripetal force produces no torque about the origin because it always points along the radius vector. Therefore the angular momentum remains conserved.