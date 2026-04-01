# Problem Set 03 – Solutions
Mechanics II: Dynamics and Energy

---

# Task 01 – Newton's Second Law (Constant Force)

## Problem Statement

A constant force acts on a body:

$$
\vec F = (6, 2)\ \mathrm{N}, \quad m = 2\ \mathrm{kg}
$$

Initial conditions:

$$
\vec v(0) = (1, -1), \quad \vec r(0) = (0,0)
$$

---

## Theory

Newton’s second law:

$$
\vec F = m \vec a
$$

Work-energy theorem:

$$
W = \Delta T
$$

---

## Step-by-Step Solution

Acceleration:

$$
\vec a = \frac{\vec F}{m} = (3,1)
$$

Velocity:

$$
\vec v(t) = \vec v_0 + \vec a t = (1+3t,\ -1+t)
$$

Position:

$$
\vec r(t) =
\begin{pmatrix}
t + \frac{3}{2}t^2 \\
- t + \frac{1}{2}t^2
\end{pmatrix}
$$

Work at $t=3$:

Displacement:

$$
\vec r(3) = (16.5,\ 1.5)
$$

Work:

$$
W = \vec F \cdot \vec r = 6\cdot16.5 + 2\cdot1.5 = 102
$$

---

## Final Result

$$
W = 102\ \mathrm{J}
$$

---

## Interpretation

Work equals change in kinetic energy → consistency verified.

---

## Visualization

Trajectory plot:

**See:** `task01_trajectory.html`

---

# Task 02 – Inclined Plane with Friction

## Theory

Forces:

- Gravity: $mg$
- Normal: $N$
- Friction: $f = \mu N$

---

## Solution

Acceleration:

$$
a = g(\sin\alpha - \mu \cos\alpha)
$$

Time:

$$
t = \sqrt{\frac{2h}{g(\sin\alpha - \mu\cos\alpha)}}
$$

Final velocity:

$$
v = \sqrt{2gh(1 - \mu \cot\alpha)}
$$

---

## Interpretation

Energy decreases due to friction → non-conservative system.

---

# Task 03 – Work of Variable Force

## Theory

Force:

$$
F(x) = -kx
$$

---

## Solution

Equation of motion:

$$
m\ddot x + kx = 0
$$

Work:

$$
W = \int_0^{x_0} (-kx)\,dx = -\frac{k}{2}x_0^2
$$

Potential energy:

$$
U(x) = \frac{1}{2}kx^2
$$

---

## Interpretation

Classic harmonic oscillator potential.

---

## Visualization

**See:** `task03_potential.html`

---

# Task 04 – Conservation of Energy

## Solution

Total energy:

$$
E = \frac{1}{2}mv^2 + mgh
$$

Velocity:

$$
v = \sqrt{2g(h_0 - h)}
$$

Condition:

$$
\frac{T}{E} = 0.75
\Rightarrow h = \frac{h_0}{4}
$$

---

## Interpretation

Energy conversion from potential → kinetic.

---

# Task 05 – Elastic Collision

## Solution

Final velocities:

$$
v_1' = \frac{m_1 - m_2}{m_1 + m_2} v_1
$$

$$
v_2' = \frac{2m_1}{m_1 + m_2} v_1
$$

Special cases:

- $m_1 = m_2$: velocities exchange
- $m_2 \gg m_1$: reflection

---

## Interpretation

Momentum + energy conservation fully determine outcome.

---

# Task 06 – Motion with Linear Drag

## Solution

Equation:

$$
m\frac{dv}{dt} = -kv
$$

Solution:

$$
v(t) = v_0 e^{-kt/m}
$$

Position:

$$
x(t) = \frac{mv_0}{k}(1 - e^{-kt/m})
$$

---

## Interpretation

Velocity decays exponentially.

---

## Visualization

**See:** `task06_decay.html`

---

# Task 07 – Vertical Throw with Drag

## Solution

Velocity:

$$
v(t) = \left(v_0 + \frac{mg}{k}\right)e^{-kt/m} - \frac{mg}{k}
$$

Maximum height: solve $v=0$

---

## Visualization

**See:** `task07_simulation.html`

---

# Task 08 – Harmonic Oscillator

## Solution

General solution:

$$
x(t) = A\cos(\omega t + \phi)
$$

Frequency:

$$
\omega = \sqrt{\frac{k}{m}}
$$

Energy:

$$
E = \frac{1}{2}mv^2 + \frac{1}{2}kx^2 = const
$$

---

## Interpretation

Periodic motion in phase space ellipse.

---

## Visualization

**See:** `task08_phase.html`

---

# Task 09 – Conservative Field

## Solution

Force:

$$
\vec F = -\nabla U = (-kx, -ky)
$$

Motion: 2D harmonic oscillator

---

## Visualization

**See:** `task09_2d_motion.html`

---

# Task 10 – Numerical Model

## Solution

Force:

$$
F = -kx - 4\lambda x^3
$$

Equation:

$$
m\ddot x = -kx - 4\lambda x^3
$$

---

## Visualization

**See:** `task10_phase.html`
