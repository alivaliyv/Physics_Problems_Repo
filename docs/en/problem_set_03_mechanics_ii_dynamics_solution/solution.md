# Problem Set 3 – Mechanics II: Dynamics and Energy — Solutions

> **Visualizations** (open in browser):
> - Task 01 → [`viz_01_trajectory.html`](viz_01_trajectory.html)
> - Task 03 → [`viz_03_spring_graphs.html`](viz_03_spring_graphs.html)
> - Task 07 → [`viz_07_drag_simulation.html`](viz_07_drag_simulation.html)
> - Task 08 → [`viz_08_phase_space.html`](viz_08_phase_space.html)
> - Task 09 → [`viz_09_2d_potential.html`](viz_09_2d_potential.html)
> - Task 10 → [`viz_10_anharmonic.html`](viz_10_anharmonic.html)

---

# Task 01 – Newton's Second Law (Constant Force)

## Problem Statement

A constant force $\vec{F} = (6,\,2)\ \mathrm{N}$ acts on a body of mass $m = 2\ \mathrm{kg}$.
Initial conditions: $\vec{v}(0) = (1,\,-1)\ \mathrm{m/s}$, $\vec{r}(0) = (0,0)\ \mathrm{m}$.

## Theory

Newton's second law for a constant force gives constant acceleration. The kinematic equations for constant acceleration integrate directly:

$$
\vec{a} = \frac{\vec{F}}{m}, \qquad \vec{v}(t) = \vec{v}(0) + \vec{a}\,t, \qquad \vec{r}(t) = \vec{r}(0) + \vec{v}(0)\,t + \frac{1}{2}\vec{a}\,t^2
$$

The work–energy theorem states that the net work done equals the change in kinetic energy:

$$
W = \Delta T = \frac{1}{2}m|\vec{v}(t)|^2 - \frac{1}{2}m|\vec{v}(0)|^2
$$

## Step-by-Step Solution

**Acceleration.**

$$
\vec{a} = \frac{\vec{F}}{m} = \frac{(6,\,2)}{2} = (3,\,1)\ \mathrm{m/s^2}
$$

**Velocity.**

$$
\vec{v}(t) = \vec{v}(0) + \vec{a}\,t = (1,\,-1) + (3,\,1)\,t = (1+3t,\; -1+t)\ \mathrm{m/s}
$$

**Position.**

$$
\vec{r}(t) = \vec{v}(0)\,t + \frac{1}{2}\vec{a}\,t^2 = \left(t + \frac{3}{2}t^2,\; -t + \frac{1}{2}t^2\right) \mathrm{m}
$$

**Work done at $t = 3\ \mathrm{s}$.**

First, compute position at $t=3$:

$$
\vec{r}(3) = \left(3 + \frac{27}{2},\; -3 + \frac{9}{2}\right) = \left(\frac{33}{2},\; \frac{3}{2}\right)\ \mathrm{m}
$$

Work via force and displacement:

$$
W = \vec{F} \cdot \Delta\vec{r} = (6,\,2)\cdot\left(\frac{33}{2},\,\frac{3}{2}\right) = 6\cdot\frac{33}{2} + 2\cdot\frac{3}{2} = 99 + 3 = 102\ \mathrm{J}
$$

**Verification via work–energy theorem.**

$$
\vec{v}(0) = (1,\,-1) \implies |\vec{v}(0)|^2 = 2\ \mathrm{m^2/s^2}
$$

$$
\vec{v}(3) = (10,\,2) \implies |\vec{v}(3)|^2 = 104\ \mathrm{m^2/s^2}
$$

$$
\Delta T = \frac{1}{2}\cdot 2\cdot(104 - 2) = 102\ \mathrm{J} \quad \checkmark
$$

## Final Result

$$
\vec{a} = (3,\,1)\ \mathrm{m/s^2}
$$

$$
\vec{v}(t) = (1+3t,\;-1+t)\ \mathrm{m/s}
$$

$$
\vec{r}(t) = \left(t+\tfrac{3}{2}t^2,\;-t+\tfrac{1}{2}t^2\right)\ \mathrm{m}
$$

$$
W(t=3\,\mathrm{s}) = 102\ \mathrm{J}
$$

## Interpretation

The trajectory is parabolic because the motion is governed by two simultaneous linear (in $t$) velocity components; eliminating $t$ yields a quadratic relation between $x$ and $y$. The work–energy theorem is confirmed: the total work of 102 J is entirely converted to an increase in kinetic energy.

---

# Task 02 – Inclined Plane with Friction

## Problem Statement

A body of mass $m$ slides down an inclined plane with angle $\alpha$ and coefficient of kinetic friction $\mu$. Determine: forces, acceleration, descent time from height $h$, final velocity, and energy consistency.

## Theory

On an inclined plane, the weight $m\vec{g}$ decomposes into a component along the slope and a component perpendicular to it. The normal force balances the perpendicular component. Kinetic friction opposes motion.

## Step-by-Step Solution

**Forces acting on the body.**

Normal force:

$$
N = mg\cos\alpha
$$

Gravitational component along slope (positive down the slope):

$$
F_{\parallel} = mg\sin\alpha
$$

Kinetic friction (opposing motion, i.e., up the slope):

$$
f = \mu N = \mu mg\cos\alpha
$$

**Acceleration.**

Applying Newton's second law along the slope:

$$
ma = mg\sin\alpha - \mu mg\cos\alpha
$$

$$
a = g(\sin\alpha - \mu\cos\alpha)
$$

For motion to occur: $\tan\alpha > \mu$.

**Descent time from height $h$.**

The length of the slope is $L = h/\sin\alpha$. Starting from rest under constant acceleration:

$$
L = \frac{1}{2}a\,t^2 \implies t = \sqrt{\frac{2L}{a}} = \sqrt{\frac{2h}{a\sin\alpha}} = \sqrt{\frac{2h}{g\sin\alpha(\sin\alpha - \mu\cos\alpha)}}
$$

**Final velocity.**

$$
v^2 = 2aL = 2g(\sin\alpha - \mu\cos\alpha)\cdot\frac{h}{\sin\alpha}
$$

$$
v = \sqrt{2gh\left(1 - \mu\cot\alpha\right)}
$$

**Energy balance check.**

Energy input (loss of potential energy): $mgh$.

Energy lost to friction (friction force $\times$ displacement):

$$
W_f = \mu mg\cos\alpha \cdot \frac{h}{\sin\alpha} = \mu mgh\cot\alpha
$$

Kinetic energy at the bottom:

$$
T = mgh - \mu mgh\cot\alpha = mgh(1 - \mu\cot\alpha)
$$

Since $T = \frac{1}{2}mv^2$, this gives $v = \sqrt{2gh(1-\mu\cot\alpha)}$, consistent with the kinematic result. $\checkmark$

## Final Result

$$
a = g(\sin\alpha - \mu\cos\alpha)
$$

$$
t = \sqrt{\frac{2h}{g\sin\alpha(\sin\alpha - \mu\cos\alpha)}}
$$

$$
v = \sqrt{2gh(1 - \mu\cot\alpha)}
$$

## Interpretation

Friction reduces the effective acceleration and dissipates part of the potential energy into heat. As $\mu \to \tan\alpha$ the acceleration vanishes (body on the verge of sliding). As $\alpha \to 90°$, the result approaches free fall: $v = \sqrt{2gh}$.

---

# Task 03 – Work of a Variable Force

## Problem Statement

Given the one-dimensional force $F(x) = -kx$. Analyze the equation of motion, compute the work from $0$ to $x_0$, interpret as potential energy, and verify $F = -dU/dx$.

## Theory

A force of the form $F = -kx$ is a restoring force (Hooke's law). It is conservative — its work depends only on the endpoints, not the path. The potential energy associated with a conservative force satisfies:

$$
U(x) = -\int F(x)\,dx
$$

## Step-by-Step Solution

**Equation of motion.**

$$
m\ddot{x} = -kx \implies \ddot{x} + \omega^2 x = 0, \qquad \omega = \sqrt{\frac{k}{m}}
$$

General solution (simple harmonic motion):

$$
x(t) = A\cos(\omega t) + B\sin(\omega t)
$$

where $A$, $B$ are determined by initial conditions.

**Work done from $0$ to $x_0$.**

$$
W = \int_0^{x_0} F(x)\,dx = \int_0^{x_0} (-kx)\,dx = -\frac{1}{2}kx_0^2
$$

The force does negative work when displacing the body from the equilibrium — the spring stores energy.

**Potential energy.**

Define $U$ such that the work done by the force equals the decrease in potential energy:

$$
W = -\Delta U = -(U(x_0) - U(0))
$$

Choosing $U(0) = 0$:

$$
U(x_0) = \frac{1}{2}kx_0^2
$$

In general:

$$
U(x) = \frac{1}{2}kx^2
$$

**Verification.**

$$
-\frac{dU}{dx} = -\frac{d}{dx}\left(\frac{1}{2}kx^2\right) = -kx = F(x) \quad \checkmark
$$

## Final Result

$$
x(t) = A\cos(\omega t) + B\sin(\omega t), \qquad \omega = \sqrt{\frac{k}{m}}
$$

$$
W_{0 \to x_0} = -\frac{1}{2}kx_0^2
$$

$$
U(x) = \frac{1}{2}kx^2
$$

## Interpretation

The work is negative because the spring force opposes the displacement. The stored potential energy $\frac{1}{2}kx^2$ is released when the body returns to equilibrium — this is the mechanism of oscillation.

---

# Task 04 – Conservation of Energy

## Problem Statement

A body falls from height $h$ without air resistance. Analyze total energy, velocity as a function of height, compare with Newton's law solution, and find the height at which kinetic energy is 75% of total energy.

## Theory

For a conservative system (no dissipation), the total mechanical energy $E = T + U$ is constant. With the ground as the reference level:

$$
U(y) = mgy, \qquad T(y) = \frac{1}{2}mv^2(y)
$$

## Step-by-Step Solution

**Total energy.**

At the initial height $y = h$ with $v = 0$:

$$
E = T(h) + U(h) = 0 + mgh = mgh
$$

At height $y < h$:

$$
E = \frac{1}{2}mv^2(y) + mgy = mgh
$$

**Velocity as a function of height.**

$$
\frac{1}{2}mv^2 = mg(h - y) \implies v(y) = \sqrt{2g(h - y)}
$$

**Comparison with Newton's second law.**

From $m\ddot{y} = -mg$:

$$
v^2 = v_0^2 + 2(-g)(y - h) = 2g(h - y) \quad \checkmark
$$

Both approaches yield the same result.

**Height at which $T = 0.75\,E$.**

$$
\frac{T}{E} = \frac{mg(h-y)}{mgh} = \frac{h - y}{h} = 0.75
$$

$$
h - y = 0.75h \implies y = 0.25h = \frac{h}{4}
$$

## Final Result

$$
E = mgh \quad (\text{conserved})
$$

$$
v(y) = \sqrt{2g(h-y)}
$$

$$
T = 0.75\,E \text{ at } y = \frac{h}{4}
$$

## Interpretation

As the body falls, potential energy is continuously converted to kinetic energy at a constant total. Three-quarters of the height is converted to kinetic energy already at one quarter of the total height — the body accelerates rapidly during the first part of the fall and is already fast by the time it reaches $h/4$.

---

# Task 05 – Momentum and One-Dimensional Elastic Collision

## Problem Statement

Two bodies with masses $m_1$, $m_2$ and initial velocities $v_1$, $v_2$ undergo a head-on elastic collision.

## Theory

An elastic collision conserves both momentum and kinetic energy:

$$
m_1 v_1 + m_2 v_2 = m_1 v_1' + m_2 v_2'
$$

$$
\frac{1}{2}m_1 v_1^2 + \frac{1}{2}m_2 v_2^2 = \frac{1}{2}m_1 v_1'^2 + \frac{1}{2}m_2 v_2'^2
$$

The energy equation factors as a difference of squares, yielding an elegant additional relation.

## Step-by-Step Solution

**Derivation of post-collision velocities.**

From momentum conservation:

$$
m_1(v_1 - v_1') = m_2(v_2' - v_2) \tag{1}
$$

From energy conservation (factoring):

$$
m_1(v_1 - v_1')(v_1 + v_1') = m_2(v_2' - v_2)(v_2' + v_2) \tag{2}
$$

Dividing (2) by (1) (assuming $v_1 \neq v_1'$):

$$
v_1 + v_1' = v_2' + v_2 \implies v_1 - v_2 = -(v_1' - v_2')
$$

This states that the relative velocity of approach equals the relative velocity of separation — a hallmark of elastic collisions.

Solving the linear system formed by this relation and equation (1):

$$
v_1' = \frac{(m_1 - m_2)\,v_1 + 2m_2\,v_2}{m_1 + m_2}
$$

$$
v_2' = \frac{(m_2 - m_1)\,v_2 + 2m_1\,v_1}{m_1 + m_2}
$$

**Special case $m_1 = m_2$.**

$$
v_1' = v_2, \qquad v_2' = v_1
$$

The bodies exchange velocities completely.

**Limiting case $m_2 \gg m_1$.**

$$
v_1' \approx -v_1 + 2v_2, \qquad v_2' \approx v_2
$$

The light body bounces back; the heavy body is essentially unaffected.

## Final Result

$$
v_1' = \frac{(m_1 - m_2)\,v_1 + 2m_2\,v_2}{m_1 + m_2}, \qquad v_2' = \frac{(m_2 - m_1)\,v_2 + 2m_1\,v_1}{m_1 + m_2}
$$

## Interpretation

The key insight is the relative-velocity reversal: $v_1 - v_2 = -(v_1' - v_2')$. This converts the nonlinear energy equation into a linear one, making the system easily solvable. The equal-mass case is frequently exploited in Newton's cradle and billiard physics.

---

# Task 06 – Motion with Linear Drag

## Problem Statement

The drag force $F = -kv$ acts on a body. Initial conditions: $v(0) = v_0$, $x(0) = 0$.

## Theory

Linear drag produces an exponential decay of velocity. The equation is a first-order linear ODE:

$$
m\frac{dv}{dt} = -kv
$$

## Step-by-Step Solution

**Solving the velocity ODE.**

Separating variables:

$$
\frac{dv}{v} = -\frac{k}{m}\,dt \implies \ln v = -\frac{k}{m}t + C
$$

Applying $v(0) = v_0$:

$$
v(t) = v_0\,e^{-t/\tau}, \qquad \tau = \frac{m}{k}
$$

Here $\tau$ is the characteristic time after which velocity falls to $v_0/e \approx 0.368\,v_0$.

**Position by integration.**

$$
x(t) = \int_0^t v_0\,e^{-s/\tau}\,ds = v_0\tau\left(1 - e^{-t/\tau}\right) = \frac{mv_0}{k}\left(1 - e^{-t/\tau}\right)
$$

**Limit as $t \to \infty$.**

$$
\lim_{t\to\infty} v(t) = 0
$$

$$
\lim_{t\to\infty} x(t) = \frac{mv_0}{k}
$$

The body travels a finite total distance $x_\infty = mv_0/k$ and asymptotically comes to rest.

**Comparison with drag-free motion.**

Without drag: $v = v_0$, $x = v_0 t$ (linear, unbounded). With drag, velocity decays exponentially and displacement is bounded.

## Final Result

$$
v(t) = v_0\,e^{-t/\tau}, \qquad \tau = \frac{m}{k}
$$

$$
x(t) = \frac{mv_0}{k}\left(1 - e^{-t/\tau}\right)
$$

$$
x_\infty = \frac{mv_0}{k}
$$

## Interpretation

Linear drag converts all kinetic energy into heat over an infinite time interval but over a finite distance. The parameter $\tau$ characterizes the "memory" of the initial velocity: a heavier body (large $m$) or a weaker drag (small $k$) retains its velocity longer.

---

# Task 07 – Vertical Throw with Drag

## Problem Statement

Equation of motion: $m\,\dot{v} = -mg - kv$, with $v(0) = v_0 > 0$, $x(0) = 0$.

## Theory

This is a first-order linear ODE with constant coefficients. The terminal velocity $v_T$ is the steady-state solution where acceleration vanishes.

## Step-by-Step Solution

**Analytical solution.**

Rewrite the equation:

$$
\dot{v} + \frac{k}{m}v = -g
$$

The homogeneous solution is $C\,e^{-t/\tau}$ where $\tau = m/k$. The particular (steady-state) solution is found by setting $\dot{v} = 0$:

$$
v_T = -\frac{mg}{k}
$$

General solution (sum of homogeneous and particular):

$$
v(t) = v_T + (v_0 - v_T)\,e^{-t/\tau} = -\frac{mg}{k} + \left(v_0 + \frac{mg}{k}\right)e^{-t/\tau}
$$

**Position by integration.**

$$
x(t) = v_T\,t + \tau(v_0 - v_T)\left(1 - e^{-t/\tau}\right)
$$

$$
x(t) = -\frac{mg}{k}\,t + \frac{m}{k}\left(v_0 + \frac{mg}{k}\right)\left(1 - e^{-t/\tau}\right)
$$

**Maximum height.**

At maximum height, $v(t^*) = 0$:

$$
e^{-t^*/\tau} = \frac{mg/k}{v_0 + mg/k} \implies t^* = \tau\ln\!\left(1 + \frac{kv_0}{mg}\right)
$$

Substituting back gives $x_{\max} = x(t^*)$.

**Comparison with drag-free case.**

Without drag: $v = v_0 - gt$, $x = v_0 t - \frac{1}{2}gt^2$, $t^*_0 = v_0/g$, $x_{\max,0} = v_0^2/(2g)$.

With drag the maximum height is always less and the time to reach it is shorter, since the drag force adds to gravity on the way up.

**Numerical simulation** is implemented in [`viz_07_drag_simulation.html`](viz_07_drag_simulation.html).

## Final Result

$$
v(t) = -\frac{mg}{k} + \left(v_0 + \frac{mg}{k}\right)e^{-t/\tau}
$$

$$
x(t) = -\frac{mg}{k}\,t + \frac{m}{k}\left(v_0 + \frac{mg}{k}\right)\left(1 - e^{-t/\tau}\right)
$$

$$
t^* = \frac{m}{k}\ln\!\left(1 + \frac{kv_0}{mg}\right)
$$

## Interpretation

The terminal velocity $v_T = -mg/k$ represents the asymptotic downward speed when drag and gravity balance. The analytical and numerical solutions coincide — the visualization confirms the correctness of the closed-form result.

---

# Task 08 – Harmonic Oscillator (Formal Dynamics)

## Problem Statement

$$
m\ddot{x} + kx = 0
$$

Solve, find natural frequency, write energy as function of time, show conservation, interpret in phase space.

## Theory

The harmonic oscillator is the archetypal model of oscillatory motion. Its phase-space trajectory (plot of $v$ vs. $x$) is an ellipse — a closed orbit corresponding to periodic, energy-conserving motion.

## Step-by-Step Solution

**General solution.**

The characteristic equation $m\lambda^2 + k = 0$ gives $\lambda = \pm i\omega$ with:

$$
\omega_0 = \sqrt{\frac{k}{m}}
$$

General solution:

$$
x(t) = A\cos(\omega_0 t) + B\sin(\omega_0 t)
$$

Equivalently, using amplitude $C$ and phase $\phi$:

$$
x(t) = C\cos(\omega_0 t + \phi), \qquad C = \sqrt{A^2 + B^2}
$$

**Velocity.**

$$
\dot{x}(t) = -C\omega_0\sin(\omega_0 t + \phi)
$$

**Energy as a function of time.**

Kinetic energy:

$$
T(t) = \frac{1}{2}m\dot{x}^2 = \frac{1}{2}m C^2\omega_0^2\sin^2(\omega_0 t + \phi) = \frac{1}{2}kC^2\sin^2(\omega_0 t + \phi)
$$

Potential energy:

$$
U(t) = \frac{1}{2}kx^2 = \frac{1}{2}kC^2\cos^2(\omega_0 t + \phi)
$$

Total energy:

$$
E = T + U = \frac{1}{2}kC^2\left(\sin^2(\omega_0 t + \phi) + \cos^2(\omega_0 t + \phi)\right) = \frac{1}{2}kC^2
$$

Energy is constant — independent of time. $\checkmark$

**Phase space interpretation.**

In the phase plane $(x, \dot{x})$:

$$
\frac{x^2}{C^2} + \frac{\dot{x}^2}{(C\omega_0)^2} = 1
$$

This is an ellipse with semi-axes $C$ and $C\omega_0$. The system traces this ellipse periodically with period $T = 2\pi/\omega_0$.

Phase portrait: [`viz_08_phase_space.html`](viz_08_phase_space.html).

## Final Result

$$
x(t) = C\cos(\omega_0 t + \phi), \qquad \omega_0 = \sqrt{\frac{k}{m}}
$$

$$
E = \frac{1}{2}kC^2 = \text{const}
$$

## Interpretation

Kinetic and potential energy oscillate sinusoidally with frequency $2\omega_0$, but always sum to the constant total $E$. The phase-space ellipse is a visual representation of this conservation: the system cannot leave the ellipse determined by its initial energy.

---

# Task 09 – Potential and Conservative Field

## Problem Statement

$$
U(x,y) = \frac{k}{2}(x^2 + y^2)
$$

Determine the force, write equations of motion, determine the type of motion, total energy, and interpret geometrically. Interactive visualization: [`viz_09_2d_potential.html`](viz_09_2d_potential.html).

## Theory

The force derived from a scalar potential via the gradient operator:

$$
\vec{F} = -\nabla U = -\left(\frac{\partial U}{\partial x},\,\frac{\partial U}{\partial y}\right)
$$

## Step-by-Step Solution

**Force field.**

$$
F_x = -\frac{\partial U}{\partial x} = -kx, \qquad F_y = -\frac{\partial U}{\partial y} = -ky
$$

$$
\vec{F}(x,y) = -k(x,\,y) = -k\vec{r}
$$

The force always points toward the origin with magnitude $k|\vec{r}|$ — a two-dimensional Hookean restoring force.

**Equations of motion.**

$$
m\ddot{x} = -kx, \qquad m\ddot{y} = -ky
$$

The two equations are completely decoupled. Each coordinate undergoes independent simple harmonic motion with the same frequency:

$$
\omega_0 = \sqrt{\frac{k}{m}}
$$

**Solutions.**

$$
x(t) = A\cos(\omega_0 t + \phi_x), \qquad y(t) = B\cos(\omega_0 t + \phi_y)
$$

**Type of motion.**

Since both coordinates oscillate at the same frequency $\omega_0$, the trajectory is a Lissajous figure with frequency ratio 1:1. The general orbit is an ellipse (including the degenerate cases: line segment when $\phi_x = \phi_y$, and circle when $A = B$ and $|\phi_x - \phi_y| = \pi/2$).

**Total energy.**

$$
E = \frac{1}{2}m(\dot{x}^2 + \dot{y}^2) + \frac{k}{2}(x^2 + y^2)
$$

Since each decoupled oscillator conserves its own energy, the total energy $E = E_x + E_y$ is conserved.

**Geometric interpretation.**

The equipotential curves $U = \text{const}$ are circles: $x^2 + y^2 = 2U/k$. The force field is radially symmetric, always pointing inward. The trajectories (ellipses) are closed, consistent with the conservative nature of the field.

## Final Result

$$
\vec{F} = -k(x,\,y)
$$

$$
x(t) = A\cos(\omega_0 t + \phi_x), \quad y(t) = B\cos(\omega_0 t + \phi_y), \quad \omega_0 = \sqrt{\frac{k}{m}}
$$

$$
E = \frac{1}{2}m(\dot{x}^2 + \dot{y}^2) + \frac{k}{2}(x^2 + y^2) = \text{const}
$$

## Interpretation

This is the two-dimensional isotropic harmonic oscillator. Its symmetry (same $\omega_0$ in both directions) results in closed elliptical orbits. The potential bowl $U(x,y)$ is a paraboloid of revolution — a 3D parabolic surface — and the particle rolls in closed loops around the minimum at the origin.

---

# Task 10 – Numerical Model of an Anharmonic Oscillator

## Problem Statement

$$
U(x) = \frac{k}{2}x^2 + \lambda x^4
$$

Determine the force, write and numerically solve the equation of motion, investigate the effect of initial energy, visualize $x(t)$ and the phase portrait.

## Theory

The quartic correction $\lambda x^4$ makes the potential steeper than the harmonic case (for $\lambda > 0$). The restoring force is stronger at large amplitudes, so the oscillation frequency increases with amplitude — unlike the harmonic oscillator where frequency is amplitude-independent.

## Step-by-Step Solution

**Force.**

$$
F(x) = -\frac{dU}{dx} = -kx - 4\lambda x^3
$$

**Equation of motion.**

$$
m\ddot{x} = -kx - 4\lambda x^3
$$

This is a nonlinear ODE; no closed-form general solution exists (unlike the pure harmonic case). Numerical integration is required.

**Numerical method — 4th-order Runge–Kutta.**

Rewrite as a first-order system with $v = \dot{x}$:

$$
\dot{x} = v, \qquad \dot{v} = -\frac{k}{m}x - \frac{4\lambda}{m}x^3
$$

At each step $h$:

$$
\begin{align}
k_1 &= h\,f(t_n,\,x_n,\,v_n) \\
k_2 &= h\,f\!\left(t_n + \tfrac{h}{2},\,x_n + \tfrac{l_1}{2},\,v_n + \tfrac{k_1}{2}\right) \\
k_3 &= h\,f\!\left(t_n + \tfrac{h}{2},\,x_n + \tfrac{l_2}{2},\,v_n + \tfrac{k_2}{2}\right) \\
k_4 &= h\,f(t_n + h,\,x_n + l_3,\,v_n + k_3)
\end{align}
$$

where $l_i$ are the corresponding updates for $x$ and $f$ is the acceleration function.

**Effect of initial energy.**

- For small amplitudes ($\lambda x^4 \ll \frac{k}{2}x^2$): nearly harmonic oscillation, approximately constant frequency $\omega_0 = \sqrt{k/m}$.
- For large amplitudes: the quartic term dominates; frequency increases; waveform distorts from sinusoidal.
- For $\lambda < 0$: the potential has a double-well structure — qualitatively different dynamics (tunneling between wells, separatrix in phase space).

**Phase portrait.**

The phase portrait $(x, v)$ consists of closed curves (periodic orbits) for bounded motion. As energy increases, orbits expand and their shape departs from the ellipse of the harmonic oscillator.

Interactive visualization: [`viz_10_anharmonic.html`](viz_10_anharmonic.html).

## Final Result

$$
F(x) = -kx - 4\lambda x^3
$$

$$
m\ddot{x} = -kx - 4\lambda x^3 \quad (\text{solved numerically via RK4})
$$

## Interpretation

The anharmonic oscillator bridges the exactly solvable harmonic model and the chaotic nonlinear world. For $\lambda > 0$ the system remains periodic but with amplitude-dependent frequency — a key departure from linearity with measurable consequences in real oscillators (e.g., pendulums at large angles, molecular vibrations).