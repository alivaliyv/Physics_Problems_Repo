# Problem Set 02 - Solutions

# Task 01 - Uniform and Uniformly Accelerated Motion

## Problem Statement

The equation of motion is

$$
x(t) = x_0 + v_0 t + \frac{1}{2} a t^2
$$

Determine $v(t)$ and $a(t)$. For $x_0 = 0$, $v_0 = 5\,\mathrm{m/s}$, $a = -2\,\mathrm{m/s^2}$, determine the stopping time and maximum displacement. Visualize $x(t)$, $v(t)$, and $a(t)$.

## Theory

For one-dimensional motion,

$$
v(t) = \frac{dx}{dt}
$$

and

$$
a(t) = \frac{dv}{dt} = \frac{d^2x}{dt^2}
$$

If the acceleration is constant, the position is a quadratic function of time, the velocity is linear in time, and the acceleration is constant.

## Step-by-Step Solution

Differentiate the given position function:

$$
\begin{align}
v(t) &= \frac{d}{dt}\left(x_0 + v_0 t + \frac{1}{2} a t^2\right) \\
     &= v_0 + at
\end{align}
$$

Differentiate once more:

$$
\begin{align}
a(t) &= \frac{d}{dt}(v_0 + at) \\
     &= a
\end{align}
$$

For the numerical data,

$$
v(t) = 5 - 2t
$$

The stopping time is obtained from $v(t_s)=0$:

$$
5 - 2t_s = 0
$$

so

$$
t_s = \frac{5}{2} = 2.5\,\mathrm{s}
$$

Since $a<0$, the velocity decreases linearly. For $t \ge 0$, the maximum velocity occurs at the initial moment,

$$
v_{\max} = v(0)=5\,\mathrm{m/s}
$$

The displacement is maximal when the velocity first becomes zero. Therefore,

$$
x_{\max} = x(t_s)
$$

Using $x_0=0$ and $t_s=2.5\,\mathrm{s}$,

$$
\begin{align}
x_{\max} &= 5(2.5) + \frac{1}{2}(-2)(2.5)^2 \\
         &= 12.5 - 6.25 \\
         &= 6.25\,\mathrm{m}
\end{align}
$$

## Final Result

$$
v(t)=v_0+at
$$

$$
a(t)=a
$$

For $x_0=0$, $v_0=5\,\mathrm{m/s}$, $a=-2\,\mathrm{m/s^2}$:

$$
t_s = 2.5\,\mathrm{s}
$$

$$
v_{\max}=5\,\mathrm{m/s}
$$

$$
x_{\max}=6.25\,\mathrm{m}
$$

## Interpretation

The motion begins in the positive direction, slows down uniformly, stops after $2.5\,\mathrm{s}$, and reaches a turning point at $x=6.25\,\mathrm{m}$. After that instant, the particle would reverse direction if the same acceleration continued.

---

# Task 02 - Projectile Motion

## Problem Statement

A body is launched with initial speed $v_0$ at angle $\alpha$ to the horizontal in a uniform gravitational field without air resistance. Determine the equations of motion, time of flight, maximum height, range, and the angle of maximum range.

## Theory

Projectile motion decomposes into two independent motions:

- horizontal motion with constant velocity,
- vertical motion with constant acceleration $-g$.

The initial velocity components are

$$
v_{0x}=v_0\cos\alpha
$$

and

$$
v_{0y}=v_0\sin\alpha
$$

## Step-by-Step Solution

The horizontal motion satisfies

$$
a_x=0
$$

Hence,

$$
x(t)=v_0\cos\alpha\, t
$$

The vertical motion satisfies

$$
a_y=-g
$$

Hence,

$$
y(t)=v_0\sin\alpha\, t - \frac{1}{2}gt^2
$$

### Time of flight

The projectile returns to the launch level when $y(T)=0$:

$$
v_0\sin\alpha\, T - \frac{1}{2}gT^2 = 0
$$

Factoring out $T$ gives

$$
T\left(v_0\sin\alpha - \frac{1}{2}gT\right)=0
$$

Ignoring the trivial solution $T=0$,

$$
T = \frac{2v_0\sin\alpha}{g}
$$

### Maximum height

The maximum height occurs when the vertical velocity vanishes:

$$
v_y(t)=v_0\sin\alpha - gt
$$

Set $v_y=0$:

$$
t_H = \frac{v_0\sin\alpha}{g}
$$

Insert this into $y(t)$:

$$
\begin{align}
H_{\max} &= v_0\sin\alpha\left(\frac{v_0\sin\alpha}{g}\right) - \frac{1}{2}g\left(\frac{v_0\sin\alpha}{g}\right)^2 \\
         &= \frac{v_0^2\sin^2\alpha}{g} - \frac{1}{2}\frac{v_0^2\sin^2\alpha}{g} \\
         &= \frac{v_0^2\sin^2\alpha}{2g}
\end{align}
$$

### Range

The range is the horizontal distance at time $T$:

$$
\begin{align}
R &= x(T) \\
  &= v_0\cos\alpha \cdot \frac{2v_0\sin\alpha}{g} \\
  &= \frac{2v_0^2\sin\alpha\cos\alpha}{g}
\end{align}
$$

Using $2\sin\alpha\cos\alpha = \sin 2\alpha$,

$$
R = \frac{v_0^2\sin 2\alpha}{g}
$$

### Angle of maximum range

The range is maximal when $\sin 2\alpha = 1$, so

$$
2\alpha = 90^\circ
$$

and therefore

$$
\alpha = 45^\circ
$$

## Final Result

$$
x(t)=v_0\cos\alpha\, t
$$

$$
y(t)=v_0\sin\alpha\, t - \frac{1}{2}gt^2
$$

$$
T = \frac{2v_0\sin\alpha}{g}
$$

$$
H_{\max}=\frac{v_0^2\sin^2\alpha}{2g}
$$

$$
R = \frac{v_0^2\sin 2\alpha}{g}
$$

$$
\alpha_{\max\,range}=45^\circ
$$

## Interpretation

The horizontal and vertical motions are independent. The trajectory is a parabola. Larger launch angles increase the height but decrease the horizontal speed. The optimal compromise for maximum range on level ground is $45^\circ$.

### HTML Visualization

Open [projectile_motion_animation.html](./projectile_motion_animation.html).

---

# Task 03 - Elimination of Time and Interpretation of Acceleration

## Problem Statement

The trajectory is given parametrically by

$$
x(t)=2t^2, \qquad y(t)=3t^3
$$

Eliminate the parameter and determine the velocity and acceleration.

## Theory

A parametric curve can often be rewritten in Cartesian form by expressing $t$ in terms of one variable and substituting into the other.

The velocity and acceleration vectors are

$$
\vec v(t)=\left(\frac{dx}{dt},\frac{dy}{dt}\right)
$$

and

$$
\vec a(t)=\left(\frac{d^2x}{dt^2},\frac{d^2y}{dt^2}\right)
$$

## Step-by-Step Solution

From

$$
x=2t^2
$$

it follows that

$$
t^2=\frac{x}{2}
$$

Since

$$
y=3t^3 = 3t\,t^2
$$

one can write

$$
y^2 = 9t^6 = 9\left(\frac{x}{2}\right)^3
$$

Therefore,

$$
y^2 = \frac{9}{8}x^3
$$

This is the Cartesian equation of the trajectory.

Now differentiate:

$$
\vec v(t)=\left(4t,9t^2\right)
$$

Its magnitude is

$$
|\vec v(t)| = \sqrt{(4t)^2+(9t^2)^2} = \sqrt{16t^2+81t^4}
$$

Differentiate again:

$$
\vec a(t)=\left(4,18t\right)
$$

Its magnitude is

$$
|\vec a(t)| = \sqrt{4^2+(18t)^2} = \sqrt{16+324t^2}
$$

Since $\vec a(t)$ depends on $t$, the acceleration is not constant.

## Final Result

$$
y^2 = \frac{9}{8}x^3
$$

$$
\vec v(t)=\begin{pmatrix}4t \\ 9t^2\end{pmatrix}
$$

$$
|\vec v(t)|=\sqrt{16t^2+81t^4}
$$

$$
\vec a(t)=\begin{pmatrix}4 \\ 18t\end{pmatrix}
$$

$$
|\vec a(t)|=\sqrt{16+324t^2}
$$

## Interpretation

The trajectory is a cusp-like algebraic curve. The horizontal acceleration is constant, but the vertical acceleration increases linearly with time. Therefore the total acceleration is not constant.

---

# Task 04 - Circular Motion

## Problem Statement

A body moves on a circle of radius $R$ with angular velocity $\omega$. Determine the position, velocity, and acceleration vectors and show that the acceleration is centripetal.

## Theory

Uniform circular motion can be represented by trigonometric functions. The position vector is

$$
\vec r(t)=R\bigl(\cos(\omega t),\sin(\omega t)\bigr)
$$

Differentiation gives tangential velocity and inward acceleration.

## Step-by-Step Solution

The position vector is

$$
\vec r(t)=\begin{pmatrix}R\cos(\omega t) \\ R\sin(\omega t)\end{pmatrix}
$$

Differentiate:

$$
\vec v(t)=\begin{pmatrix}-R\omega\sin(\omega t) \\ R\omega\cos(\omega t)\end{pmatrix}
$$

Differentiate again:

$$
\vec a(t)=\begin{pmatrix}-R\omega^2\cos(\omega t) \\ -R\omega^2\sin(\omega t)\end{pmatrix}
$$

This can be written as

$$
\vec a(t)=-\omega^2\vec r(t)
$$

Hence the acceleration is always antiparallel to the radius vector, so it points toward the center.

The magnitudes are

$$
|\vec r(t)|=R
$$

$$
|\vec v(t)|=R\omega
$$

$$
|\vec a(t)|=R\omega^2
$$

## Final Result

$$
\vec r(t)=\begin{pmatrix}R\cos(\omega t) \\ R\sin(\omega t)\end{pmatrix}
$$

$$
\vec v(t)=\begin{pmatrix}-R\omega\sin(\omega t) \\ R\omega\cos(\omega t)\end{pmatrix}
$$

$$
\vec a(t)=\begin{pmatrix}-R\omega^2\cos(\omega t) \\ -R\omega^2\sin(\omega t)\end{pmatrix}
$$

$$
\vec a(t)=-\omega^2\vec r(t)
$$

## Interpretation

The velocity is always tangent to the circle and has constant magnitude. The acceleration has constant magnitude as well, but its direction continuously changes so that it always points toward the center. This is the defining feature of centripetal acceleration.

### HTML Visualization

Open [circular_motion_visualization.html](./circular_motion_visualization.html).

---

# Task 05 - Elliptical Motion

## Problem Statement

The motion is given by

$$
x(t)=a\cos(\omega t), \qquad y(t)=b\sin(\omega t)
$$

Determine the velocity and acceleration, decide whether the speed is constant, and determine where the speed is maximal.

## Theory

An ellipse can be described parametrically. Unlike circular motion, the distance from the origin and the speed are not generally constant unless $a=b$.

## Step-by-Step Solution

Differentiate the coordinates:

$$
\vec v(t)=\begin{pmatrix}-a\omega\sin(\omega t) \\ b\omega\cos(\omega t)\end{pmatrix}
$$

Thus,

$$
|\vec v(t)| = \omega\sqrt{a^2\sin^2(\omega t)+b^2\cos^2(\omega t)}
$$

Differentiate again:

$$
\vec a(t)=\begin{pmatrix}-a\omega^2\cos(\omega t) \\ -b\omega^2\sin(\omega t)\end{pmatrix}
$$

and therefore

$$
|\vec a(t)| = \omega^2\sqrt{a^2\cos^2(\omega t)+b^2\sin^2(\omega t)}
$$

The speed is constant only if $a=b$, in which case the ellipse becomes a circle.

To find the maximum speed, examine

$$
a^2\sin^2(\omega t)+b^2\cos^2(\omega t)
$$

If $a>b$, this expression is maximal when $\sin^2(\omega t)=1$, so the points are

$$
(x,y)=(0,\pm b)
$$

and

$$
|\vec v|_{\max}=a\omega
$$

If $b>a$, the maximum occurs when $\cos^2(\omega t)=1$, that is at

$$
(x,y)=(\pm a,0)
$$

and

$$
|\vec v|_{\max}=b\omega
$$

## Final Result

$$
\vec v(t)=\begin{pmatrix}-a\omega\sin(\omega t) \\ b\omega\cos(\omega t)\end{pmatrix}
$$

$$
\vec a(t)=\begin{pmatrix}-a\omega^2\cos(\omega t) \\ -b\omega^2\sin(\omega t)\end{pmatrix}
$$

$$
|\vec v(t)| = \omega\sqrt{a^2\sin^2(\omega t)+b^2\cos^2(\omega t)}
$$

$$
|\vec a(t)| = \omega^2\sqrt{a^2\cos^2(\omega t)+b^2\sin^2(\omega t)}
$$

## Interpretation

The speed is not constant on an ellipse unless the ellipse is actually a circle. The particle moves fastest near the ends of the minor axis, where the tangent direction aligns with the longer semi-axis contribution.

---

# Task 06 - Cycloid: Trajectory of a Point on a Rolling Circle

## Problem Statement

The cycloid is defined by

$$
x(t)=R(\omega t-\sin(\omega t)), \qquad y(t)=R(1-\cos(\omega t))
$$

Determine the velocity and acceleration, the moments when the point stops, and the maximum values of speed and acceleration.

## Theory

A cycloid is generated by a point on the rim of a circle rolling without slipping. The translational and rotational contributions combine to create cusps where the point instantaneously comes to rest.

## Step-by-Step Solution

Differentiate the coordinates:

$$
\vec v(t)=\begin{pmatrix}R\omega(1-\cos(\omega t)) \\ R\omega\sin(\omega t)\end{pmatrix}
$$

Differentiate again:

$$
\vec a(t)=\begin{pmatrix}R\omega^2\sin(\omega t) \\ R\omega^2\cos(\omega t)\end{pmatrix}
$$

The speed is

$$
\begin{align}
|\vec v(t)| &= R\omega\sqrt{(1-\cos(\omega t))^2+\sin^2(\omega t)} \\
             &= R\omega\sqrt{2-2\cos(\omega t)} \\
             &= 2R\omega\left|\sin\left(\frac{\omega t}{2}\right)\right|
\end{align}
$$

The point stops when $|\vec v|=0$, so

$$
\sin\left(\frac{\omega t}{2}\right)=0
$$

Hence,

$$
\omega t = 2\pi n, \qquad n \in \mathbb{Z}
$$

These are the cusp points where the marked point touches the ground.

The maximum speed occurs when

$$
\left|\sin\left(\frac{\omega t}{2}\right)\right|=1
$$

Therefore,

$$
|\vec v|_{\max}=2R\omega
$$

The acceleration magnitude is

$$
|\vec a(t)| = R\omega^2\sqrt{\sin^2(\omega t)+\cos^2(\omega t)} = R\omega^2
$$

Thus,

$$
|\vec a|_{\max}=R\omega^2
$$

## Final Result

$$
\vec v(t)=\begin{pmatrix}R\omega(1-\cos(\omega t)) \\ R\omega\sin(\omega t)\end{pmatrix}
$$

$$
\vec a(t)=\begin{pmatrix}R\omega^2\sin(\omega t) \\ R\omega^2\cos(\omega t)\end{pmatrix}
$$

$$
|\vec v(t)|=2R\omega\left|\sin\left(\frac{\omega t}{2}\right)\right|
$$

$$
|\vec a(t)|=R\omega^2
$$

The stopping instants are

$$
\omega t = 2\pi n
$$

## Interpretation

The point alternates between complete rest at the cusp and maximum speed at the top of the rolling circle. The acceleration magnitude stays constant even though the speed does not.

### HTML Visualization

Open [cycloid_animation.html](./cycloid_animation.html).

---

# Task 07 - 2D Motion with a Given Acceleration

## Problem Statement

Given

$$
\vec a=(2,-3)
$$

with initial conditions

$$
\vec v(0)=(1,0), \qquad \vec r(0)=(0,0)
$$

Determine $\vec v(t)$ and $\vec r(t)$.

## Theory

For constant vector acceleration, integrate componentwise.

## Step-by-Step Solution

Velocity is obtained from

$$
\vec v(t)=\vec v(0)+\vec a t
$$

Hence,

$$
\vec v(t)=\begin{pmatrix}1+2t \\ -3t\end{pmatrix}
$$

Position is obtained by integrating velocity:

$$
\vec r(t)=\vec r(0)+\int_0^t \vec v(\tau)\,d\tau
$$

Therefore,

$$
\vec r(t)=\begin{pmatrix}t+t^2 \\ -\frac{3}{2}t^2\end{pmatrix}
$$

To eliminate time, use

$$
x=t+t^2
$$

and

$$
y=-\frac{3}{2}t^2
$$

The trajectory is a parabola in the plane.

## Final Result

$$
\vec v(t)=\begin{pmatrix}1+2t \\ -3t\end{pmatrix}
$$

$$
\vec r(t)=\begin{pmatrix}t+t^2 \\ -\frac{3}{2}t^2\end{pmatrix}
$$

## Interpretation

The particle initially moves to the right. The positive $x$-acceleration increases the horizontal speed, while the negative $y$-acceleration causes a downward bend. The path is parabolic.

### HTML Visualization

Open [accelerated_2d_motion.html](./accelerated_2d_motion.html).

---

# Task 08 - Relative Motion

## Problem Statement

Body $A$ has velocity

$$
\vec v_A=(3,1)
$$

and body $B$ has velocity

$$
\vec v_B=(1,-2)
$$

Determine the relative velocity and the direction of relative motion.

## Theory

The velocity of $A$ relative to $B$ is

$$
\vec v_{A/B}=\vec v_A-\vec v_B
$$

## Step-by-Step Solution

Compute the relative velocity:

$$
\vec v_{A/B}=(3,1)-(1,-2)=(2,3)
$$

The direction angle relative to the positive $x$-axis is

$$
\theta = \arctan\left(\frac{3}{2}\right)
$$

Numerically,

$$
\theta \approx 56.3^\circ
$$

Similarly,

$$
\vec v_{B/A}=\vec v_B-\vec v_A=(-2,-3)
$$

## Final Result

$$
\vec v_{A/B}=(2,3)
$$

$$
\theta = \arctan\left(\frac{3}{2}\right) \approx 56.3^\circ
$$

## Interpretation

In the laboratory frame both bodies move uniformly along straight lines. In the frame of body $B$, body $A$ also moves uniformly along a straight line with velocity $(2,3)$. Relative motion subtracts the common drift of the chosen reference frame.

### HTML Visualization

Open [relative_motion_frames.html](./relative_motion_frames.html).

---

# Task 09 - Change of Reference Frame: Heliocentric to Geocentric Description

## Problem Statement

Earth and Mars move on circles around the Sun:

$$
\vec r_Z(t)=R_Z\bigl(\cos(\omega_Z t),\sin(\omega_Z t)\bigr)
$$

$$
\vec r_M(t)=R_M\bigl(\cos(\omega_M t),\sin(\omega_M t)\bigr)
$$

Determine the motion of Mars relative to Earth.

## Theory

Changing reference frame means subtracting the position vector of the new origin.

## Step-by-Step Solution

The relative position of Mars with respect to Earth is

$$
\vec r_{M/Z}(t)=\vec r_M(t)-\vec r_Z(t)
$$

Hence,

$$
\vec r_{M/Z}(t)=\begin{pmatrix}
R_M\cos(\omega_M t)-R_Z\cos(\omega_Z t) \\
R_M\sin(\omega_M t)-R_Z\sin(\omega_Z t)
\end{pmatrix}
$$

So the explicit components are

$$
x_{M/Z}(t)=R_M\cos(\omega_M t)-R_Z\cos(\omega_Z t)
$$

and

$$
y_{M/Z}(t)=R_M\sin(\omega_M t)-R_Z\sin(\omega_Z t)
$$

## Final Result

$$
\vec r_{M/Z}(t)=\begin{pmatrix}
R_M\cos(\omega_M t)-R_Z\cos(\omega_Z t) \\
R_M\sin(\omega_M t)-R_Z\sin(\omega_Z t)
\end{pmatrix}
$$

## Interpretation

Although both planets move on simple circles in the heliocentric frame, the geocentric description becomes more complicated. The resulting relative curve explains why planetary motion can appear to contain loops and retrograde segments when viewed from Earth.

### HTML Visualization

Open [mars_earth_reference_frames.html](./mars_earth_reference_frames.html).

---

# Task 10 - Analysis of Motion from Numerical Data

## Problem Statement

Given

$$
x(t)=t+\frac{1}{20}t^2
$$

for $t\in[0,10]$ with step size $\Delta t=0.1$, approximate velocity and acceleration numerically and compare with the analytical result.

## Theory

For sampled data, derivatives can be approximated by finite differences.

Forward difference for velocity:

$$
v_i \approx \frac{x_{i+1}-x_i}{\Delta t}
$$

Central difference for velocity:

$$
v_i \approx \frac{x_{i+1}-x_{i-1}}{2\Delta t}
$$

Central difference for acceleration:

$$
a_i \approx \frac{x_{i+1}-2x_i+x_{i-1}}{\Delta t^2}
$$

## Step-by-Step Solution

The analytical derivatives are

$$
v(t)=\frac{dx}{dt}=1+\frac{1}{10}t
$$

and

$$
a(t)=\frac{d^2x}{dt^2}=\frac{1}{10}
$$

At the discrete points $t_i=i\Delta t$ with $\Delta t=0.1$,

$$
x_i=t_i+\frac{1}{20}t_i^2
$$

Using the central difference for velocity,

$$
v_i \approx \frac{x_{i+1}-x_{i-1}}{2\Delta t}
$$

Substitute the quadratic function into the finite difference. Because the exact function is quadratic, the central second difference reproduces the constant acceleration exactly:

$$
a_i \approx \frac{x_{i+1}-2x_i+x_{i-1}}{\Delta t^2}=0.1
$$

For the velocity, the central difference also reproduces the derivative exactly for this quadratic polynomial at interior points:

$$
v_i = 1+0.1t_i
$$

At the boundaries, one-sided formulas produce small truncation errors of order $\Delta t$.

If the step size is reduced, the boundary errors decrease proportionally for first-order one-sided formulas and quadratically for second-order central formulas in the interior.

## Final Result

Analytical solution:

$$
v(t)=1+0.1t
$$

$$
a(t)=0.1
$$

For the sampled quadratic data, central finite differences recover the exact interior values of both velocity and acceleration.

## Interpretation

Finite differences are especially accurate for low-degree polynomials. This example shows that the numerical method can reproduce the exact derivative in the interior when the function is sufficiently simple and the stencil matches the polynomial structure.
