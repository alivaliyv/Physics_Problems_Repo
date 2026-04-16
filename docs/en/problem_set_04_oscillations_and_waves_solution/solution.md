# Problem Set 04 – Solutions

## File Map

The following standalone visualization files accompany this notebook:

- `problem_set_04_vis_problem_05_beats.html`
- `problem_set_04_vis_problem_06_damped_oscillator.html`
- `problem_set_04_vis_problem_07_resonance.html`
- `problem_set_04_vis_problem_08_coupled_springs.html`
- `problem_set_04_vis_problem_09_chain_of_springs.html`
- `problem_set_04_vis_problem_10_double_pendulum_ensemble.html`

---

# Task 01 – Harmonic Motion: Motion Parameters

## Problem Statement

The harmonic motion is described by

$$
x(t) = A \cos(\omega t + \varphi)
$$

Determine the period $T$, the frequency $f$, the maximum velocity, and the maximum acceleration. Then evaluate these quantities for $A = 0.2\ \mathrm{m}$ and $f = 2\ \mathrm{Hz}$.

## Theory

For harmonic motion, the angular frequency, period, and frequency satisfy

$$
\omega = 2 \pi f = \frac{2 \pi}{T}
$$

Hence,

$$
T = \frac{2 \pi}{\omega},
\qquad
f = \frac{1}{T} = \frac{\omega}{2 \pi}
$$

Velocity and acceleration are obtained by differentiation.

## Step-by-Step Solution

The displacement is

$$
x(t) = A \cos(\omega t + \varphi)
$$

The velocity is

$$
v(t) = \frac{dx}{dt} = - A \omega \sin(\omega t + \varphi)
$$

Its magnitude is maximal when $\sin(\omega t + \varphi) = \pm 1$, therefore

$$
v_{\max} = A \omega
$$

The acceleration is

$$
a(t) = \frac{d^2x}{dt^2} = - A \omega^2 \cos(\omega t + \varphi)
$$

Its magnitude is maximal when $\cos(\omega t + \varphi) = \pm 1$, hence

$$
a_{\max} = A \omega^2
$$

For $A = 0.2\ \mathrm{m}$ and $f = 2\ \mathrm{Hz}$,

$$
\omega = 2 \pi f = 2 \pi \cdot 2 = 4 \pi\ \mathrm{rad/s}
$$

Numerically,

$$
\omega \approx 12.57\ \mathrm{rad/s}
$$

Then

$$
v_{\max} = A \omega = 0.2 \cdot 4 \pi = 0.8 \pi\ \mathrm{m/s}
$$

$$
v_{\max} \approx 2.51\ \mathrm{m/s}
$$

and

$$
a_{\max} = A \omega^2 = 0.2 \cdot (4 \pi)^2 = 3.2 \pi^2\ \mathrm{m/s^2}
$$

$$
a_{\max} \approx 31.58\ \mathrm{m/s^2}
$$

The period is

$$
T = \frac{1}{f} = \frac{1}{2} = 0.5\ \mathrm{s}
$$

## Final Result

$$
T = \frac{2 \pi}{\omega},
\qquad
f = \frac{\omega}{2 \pi}
$$

$$
v_{\max} = A \omega,
\qquad
a_{\max} = A \omega^2
$$

For $A = 0.2\ \mathrm{m}$ and $f = 2\ \mathrm{Hz}$,

$$
\omega = 4 \pi\ \mathrm{rad/s} \approx 12.57\ \mathrm{rad/s}
$$

$$
v_{\max} = 0.8 \pi\ \mathrm{m/s} \approx 2.51\ \mathrm{m/s}
$$

$$
a_{\max} = 3.2 \pi^2\ \mathrm{m/s^2} \approx 31.58\ \mathrm{m/s^2}
$$

## Interpretation

The maximum velocity grows linearly with frequency, while the maximum acceleration grows quadratically with frequency. This explains why fast oscillations can produce large accelerations even for small amplitudes.

---

# Task 02 – Energy of a Harmonic Oscillator

## Problem Statement

Given

- $m = 1\ \mathrm{kg}$
- $k = 100\ \mathrm{N/m}$
- $x(0) = 2\ \mathrm{m}$
- $v(0) = 1\ \mathrm{m/s}$

determine the natural frequency, the total energy, and the displacement for which the kinetic energy is equal to $50\%$ of the total energy.

## Theory

For the ideal mass–spring oscillator,

$$
m \ddot{x} + kx = 0
$$

The natural angular frequency is

$$
\omega_0 = \sqrt{\frac{k}{m}}
$$

The total mechanical energy is conserved:

$$
E = \frac{1}{2} m v^2 + \frac{1}{2} k x^2
$$

## Step-by-Step Solution

The natural angular frequency is

$$
\omega_0 = \sqrt{\frac{100}{1}} = 10\ \mathrm{rad/s}
$$

The ordinary frequency is

$$
f_0 = \frac{\omega_0}{2 \pi} = \frac{10}{2 \pi} \approx 1.59\ \mathrm{Hz}
$$

At $t = 0$ the energy is

$$
E = \frac{1}{2} m v(0)^2 + \frac{1}{2} k x(0)^2
$$

Substituting the numbers gives

$$
E = \frac{1}{2} \cdot 1 \cdot 1^2 + \frac{1}{2} \cdot 100 \cdot 2^2
$$

$$
E = 0.5 + 200 = 200.5\ \mathrm{J}
$$

For the kinetic energy to be $50\%$ of the total energy,

$$
K = \frac{1}{2} E
$$

Therefore the potential energy must also be

$$
U = \frac{1}{2} E
$$

Using

$$
U = \frac{1}{2} k x^2
$$

one gets

$$
\frac{1}{2} k x^2 = \frac{E}{2}
$$

Hence

$$
k x^2 = E
$$

and

$$
x^2 = \frac{E}{k} = \frac{200.5}{100} = 2.005
$$

Thus

$$
x = \pm \sqrt{2.005}\ \mathrm{m}
$$

$$
x \approx \pm 1.416\ \mathrm{m}
$$

## Final Result

$$
\omega_0 = 10\ \mathrm{rad/s},
\qquad
f_0 \approx 1.59\ \mathrm{Hz}
$$

$$
E = 200.5\ \mathrm{J}
$$

The kinetic energy is $50\%$ of the total energy at

$$
x \approx \pm 1.416\ \mathrm{m}
$$

## Interpretation

At these positions, the oscillator has exactly the same amount of kinetic and potential energy. The total energy remains constant, but its partition between motion and deformation changes continuously.

---

# Task 03 – Harmonic Wave

## Problem Statement

The wave is

$$
y(x,t) = A \sin(kx - \omega t)
$$

Determine the wavelength, phase velocity, and evaluate the phase velocity for $k = 4 \pi$ and $\omega = 20 \pi$. Determine whether the points $x = \lambda$ and $x = 0$ oscillate in phase.

## Theory

For a harmonic wave,

$$
k = \frac{2 \pi}{\lambda}
$$

and the phase velocity is

$$
v = \frac{\omega}{k}
$$

## Step-by-Step Solution

From the definition of the wave number,

$$
\lambda = \frac{2 \pi}{k}
$$

The phase condition is

$$
kx - \omega t = \mathrm{const.}
$$

Differentiating with respect to time gives

$$
k \frac{dx}{dt} - \omega = 0
$$

Therefore,

$$
v = \frac{dx}{dt} = \frac{\omega}{k}
$$

For $k = 4 \pi$ and $\omega = 20 \pi$,

$$
\lambda = \frac{2 \pi}{4 \pi} = \frac{1}{2}\ \mathrm{m}
$$

and

$$
v = \frac{20 \pi}{4 \pi} = 5\ \mathrm{m/s}
$$

Now compare the phase at $x = 0$ and $x = \lambda$.

At $x = 0$,

$$
y(0,t) = A \sin(-\omega t)
$$

At $x = \lambda$,

$$
y(\lambda,t) = A \sin(k \lambda - \omega t)
$$

Since

$$
k \lambda = \frac{2 \pi}{\lambda} \lambda = 2 \pi
$$

it follows that

$$
y(\lambda,t) = A \sin(2 \pi - \omega t) = A \sin(-\omega t)
$$

Therefore the two points oscillate in phase.

## Final Result

$$
\lambda = \frac{2 \pi}{k}
$$

$$
v = \frac{\omega}{k}
$$

For $k = 4 \pi$ and $\omega = 20 \pi$,

$$
\lambda = 0.5\ \mathrm{m}
$$

$$
v = 5\ \mathrm{m/s}
$$

The points $x = 0$ and $x = \lambda$ oscillate in phase.

## Interpretation

Points separated by one wavelength differ in phase by $2 \pi$, which corresponds to the same oscillatory state. This is the spatial periodicity of the wave.

---

# Task 04 – Wave Equation

## Problem Statement

Verify that

$$
y(x,t) = A \cos(kx - \omega t)
$$

satisfies

$$
\frac{\partial^2 y}{\partial t^2} = v^2 \frac{\partial^2 y}{\partial x^2}
$$

and determine the relation between $v$, $k$, and $\omega$.

## Theory

A sinusoidal traveling wave is a standard solution of the one-dimensional wave equation if its temporal and spatial derivatives differ only by a constant factor.

## Step-by-Step Solution

Let

$$
\Phi = kx - \omega t
$$

Then

$$
y(x,t) = A \cos \Phi
$$

The first derivative with respect to time is

$$
\frac{\partial y}{\partial t} = - A \sin \Phi \cdot \frac{\partial \Phi}{\partial t}
$$

Since

$$
\frac{\partial \Phi}{\partial t} = - \omega
$$

one gets

$$
\frac{\partial y}{\partial t} = A \omega \sin \Phi
$$

Differentiating once more,

$$
\frac{\partial^2 y}{\partial t^2} = A \omega \cos \Phi \cdot \frac{\partial \Phi}{\partial t}
$$

Thus,

$$
\frac{\partial^2 y}{\partial t^2} = - A \omega^2 \cos \Phi
$$

Now differentiate with respect to $x$:

$$
\frac{\partial y}{\partial x} = - A \sin \Phi \cdot \frac{\partial \Phi}{\partial x}
$$

Since

$$
\frac{\partial \Phi}{\partial x} = k
$$

it follows that

$$
\frac{\partial y}{\partial x} = - A k \sin \Phi
$$

and therefore

$$
\frac{\partial^2 y}{\partial x^2} = - A k^2 \cos \Phi
$$

Substitute both expressions into the wave equation:

$$
- A \omega^2 \cos \Phi = v^2 (- A k^2 \cos \Phi)
$$

For nontrivial waves this implies

$$
\omega^2 = v^2 k^2
$$

Hence,

$$
v = \frac{\omega}{k}
$$

## Final Result

The function

$$
y(x,t) = A \cos(kx - \omega t)
$$

satisfies the wave equation provided that

$$
\omega^2 = v^2 k^2
$$

or equivalently

$$
v = \frac{\omega}{k}
$$

## Interpretation

The wave equation constrains the temporal and spatial oscillation scales so that the disturbance propagates with a definite speed.

---

# Task 05 – Superposition of Waves, Beats, and Group Velocity

## Problem Statement

Two waves are given:

$$
y_1(x,t) = A \sin(kx - \omega t)
$$

$$
y_2(x,t) = A \sin(kx - (\omega + \Delta \omega)t)
$$

Determine the resultant wave, the beat frequency, the beat period at $x = 0$, and the physical interpretation of the carrier and envelope.

## Theory

The trigonometric identity

$$
\sin \alpha + \sin \beta = 2 \sin \left( \frac{\alpha + \beta}{2} \right) \cos \left( \frac{\alpha - \beta}{2} \right)
$$

transforms the sum into product form.

## Step-by-Step Solution

Let

$$
\alpha = kx - \omega t
$$

and

$$
\beta = kx - (\omega + \Delta \omega)t
$$

Then

$$
y = y_1 + y_2 = A (\sin \alpha + \sin \beta)
$$

Using the identity above,

$$
y = 2A \sin \left( \frac{\alpha + \beta}{2} \right) \cos \left( \frac{\alpha - \beta}{2} \right)
$$

Now compute the combinations:

$$
\frac{\alpha + \beta}{2}
= \frac{2kx - (2\omega + \Delta \omega)t}{2}
= kx - \left( \omega + \frac{\Delta \omega}{2} \right)t
$$

and

$$
\frac{\alpha - \beta}{2}
= \frac{\Delta \omega t}{2}
$$

Thus the resultant wave is

$$
y(x,t) = 2A \sin \left( kx - \left( \omega + \frac{\Delta \omega}{2} \right)t \right)
\cos \left( \frac{\Delta \omega}{2} t \right)
$$

At fixed position $x = 0$,

$$
y(0,t) = - 2A \sin \left( \left( \omega + \frac{\Delta \omega}{2} \right)t \right)
\cos \left( \frac{\Delta \omega}{2} t \right)
$$

The slowly varying amplitude factor is

$$
A_{\mathrm{env}}(t) = 2A \cos \left( \frac{\Delta \omega}{2} t \right)
$$

The envelope repeats when the absolute value of this factor repeats, so the beat angular frequency is

$$
\omega_{\mathrm{beat}} = \Delta \omega
$$

Therefore the beat frequency is

$$
f_{\mathrm{beat}} = \frac{\Delta \omega}{2 \pi}
$$

and the beat period is

$$
T_{\mathrm{beat}} = \frac{2 \pi}{\Delta \omega}
$$

## Final Result

$$
y(x,t) = 2A \sin \left( kx - \left( \omega + \frac{\Delta \omega}{2} \right)t \right)
\cos \left( \frac{\Delta \omega}{2} t \right)
$$

Carrier wave:

$$
\sin \left( kx - \left( \omega + \frac{\Delta \omega}{2} \right)t \right)
$$

Envelope:

$$
2A \cos \left( \frac{\Delta \omega}{2} t \right)
$$

Beat frequency:

$$
f_{\mathrm{beat}} = \frac{\Delta \omega}{2 \pi}
$$

Beat period:

$$
T_{\mathrm{beat}} = \frac{2 \pi}{\Delta \omega}
$$

## Interpretation

The carrier describes the rapid oscillation, while the envelope describes the slow modulation of amplitude. Beats arise from interference between nearby frequencies. The visualization file is `problem_set_04_vis_problem_05_beats.html`.

---

# Task 06 – Damped Oscillator

## Problem Statement

Consider

$$
m \ddot{x} + b \dot{x} + kx = 0
$$

Derive the general solutions for the underdamped, critically damped, and overdamped cases, classify the regimes, and discuss the numerical solution and the influence of $b$.

## Theory

Assume an exponential solution

$$
x(t) = e^{rt}
$$

Substitution yields the characteristic equation

$$
m r^2 + b r + k = 0
$$

with roots

$$
r_{1,2} = \frac{-b \pm \sqrt{b^2 - 4mk}}{2m}
$$

The discriminant determines the character of the motion.

## Step-by-Step Solution

### Classification

The discriminant is

$$
\Delta = b^2 - 4mk
$$

Three regimes appear.

### Underdamped case

If

$$
b^2 < 4mk
$$

the roots are complex:

$$
r = - \frac{b}{2m} \pm i \omega_d
$$

where

$$
\omega_d = \sqrt{\frac{k}{m} - \frac{b^2}{4m^2}}
$$

The solution is

$$
x(t) = e^{-bt/(2m)} \left( C_1 \cos(\omega_d t) + C_2 \sin(\omega_d t) \right)
$$

### Critically damped case

If

$$
b^2 = 4mk
$$

there is a repeated root

$$
r = - \frac{b}{2m}
$$

and the solution is

$$
x(t) = (C_1 + C_2 t) e^{-bt/(2m)}
$$

### Overdamped case

If

$$
b^2 > 4mk
$$

the roots are real and distinct:

$$
r_{1,2} = \frac{-b \pm \sqrt{b^2 - 4mk}}{2m}
$$

Hence,

$$
x(t) = C_1 e^{r_1 t} + C_2 e^{r_2 t}
$$

### Numerical formulation

Introduce the state variables

$$
x_1 = x,
\qquad
x_2 = \dot{x}
$$

Then

$$
\dot{x}_1 = x_2
$$

$$
\dot{x}_2 = - \frac{b}{m} x_2 - \frac{k}{m} x_1
$$

This system is suitable for RK4 integration.

### Effect of $b$

Increasing $b$ produces the following changes:

- weaker oscillatory behavior,
- stronger decay of amplitude,
- eventual disappearance of oscillations,
- a phase portrait that contracts more rapidly toward the origin.

## Final Result

The characteristic equation is

$$
m r^2 + b r + k = 0
$$

with three regimes:

### Underdamped

$$
b^2 < 4mk
$$

$$
x(t) = e^{-bt/(2m)} \left( C_1 \cos(\omega_d t) + C_2 \sin(\omega_d t) \right)
$$

### Critically damped

$$
b^2 = 4mk
$$

$$
x(t) = (C_1 + C_2 t) e^{-bt/(2m)}
$$

### Overdamped

$$
b^2 > 4mk
$$

$$
x(t) = C_1 e^{r_1 t} + C_2 e^{r_2 t}
$$

The visualization file is `problem_set_04_vis_problem_06_damped_oscillator.html`.

## Interpretation

Damping controls the competition between inertia, restoring force, and dissipation. The critically damped case returns to equilibrium fastest without oscillating. The underdamped case is most similar to ordinary oscillatory motion but with exponentially decaying amplitude.

---

# Task 07 – Forced Oscillator and Resonance

## Problem Statement

Consider the forced damped oscillator

$$
m \ddot{x} + b \dot{x} + kx = F_0 \cos(\Omega t)
$$

Determine the steady-state amplitude as a function of $\Omega$, discuss the phase shift, and interpret resonance.

## Theory

The solution is the sum of a transient part and a steady-state part. After a sufficiently long time, only the steady-state oscillation remains.

Seek a particular solution of the form

$$
x_p(t) = X \cos(\Omega t - \delta)
$$

## Step-by-Step Solution

Using the complex representation or direct substitution leads to the steady-state amplitude

$$
X(\Omega) =
\frac{F_0}{\sqrt{(k - m \Omega^2)^2 + (b \Omega)^2}}
$$

The phase shift satisfies

$$
\tan \delta = \frac{b \Omega}{k - m \Omega^2}
$$

The full solution is

$$
x(t) = x_{\mathrm{tr}}(t) + X(\Omega) \cos(\Omega t - \delta)
$$

where $x_{\mathrm{tr}}(t)$ is the damped transient contribution.

For weak damping, the resonance peak occurs near

$$
\Omega \approx \omega_0 = \sqrt{\frac{k}{m}}
$$

More precisely, for finite damping the amplitude maximum occurs at

$$
\Omega_{\mathrm{res}} = \sqrt{\frac{k}{m} - \frac{b^2}{2m^2}}
$$

provided the expression under the square root is positive.

## Final Result

Steady-state amplitude:

$$
X(\Omega) =
\frac{F_0}{\sqrt{(k - m \Omega^2)^2 + (b \Omega)^2}}
$$

Phase shift:

$$
\tan \delta = \frac{b \Omega}{k - m \Omega^2}
$$

The resonance curve is the graph of $X(\Omega)$ versus $\Omega$. The visualization file is `problem_set_04_vis_problem_07_resonance.html`.

## Interpretation

At low frequency the motion is nearly in phase with the external force. Near resonance the response becomes maximal. At high frequency the displacement lags and the amplitude decreases because the mass cannot follow the fast forcing effectively.

---

# Task 08 – Two Coupled Springs (Two Degrees of Freedom)

## Problem Statement

Two masses are connected in series to walls by three springs with constants $k_1$, $k_2$, and $k_3$.

## Theory

Let $x_1$ and $x_2$ be the displacements from equilibrium. The restoring forces are determined by the elongations of the springs.

## Step-by-Step Solution

For mass $m_1$,

$$
m_1 \ddot{x}_1 = -k_1 x_1 - k_2 (x_1 - x_2)
$$

For mass $m_2$,

$$
m_2 \ddot{x}_2 = -k_3 x_2 - k_2 (x_2 - x_1)
$$

Thus,

$$
m_1 \ddot{x}_1 + (k_1 + k_2)x_1 - k_2 x_2 = 0
$$

$$
m_2 \ddot{x}_2 + (k_2 + k_3)x_2 - k_2 x_1 = 0
$$

In matrix form,

$$
M \ddot{\mathbf{x}} + K \mathbf{x} = 0
$$

with

$$
M =
\begin{pmatrix}
m_1 & 0 \\
0 & m_2
\end{pmatrix}
$$

and

$$
K =
\begin{pmatrix}
k_1 + k_2 & -k_2 \\
-k_2 & k_2 + k_3
\end{pmatrix}
$$

Seek normal-mode solutions of the form

$$
\mathbf{x}(t) = \mathbf{a} e^{i \omega t}
$$

Then

$$
(K - \omega^2 M)\mathbf{a} = 0
$$

For nontrivial amplitudes,

$$
\det(K - \omega^2 M) = 0
$$

This determinant yields the two natural frequencies. Each eigenvalue $\omega^2$ has a corresponding eigenvector $\mathbf{a}$, which gives the normal mode.

## Final Result

Equations of motion:

$$
m_1 \ddot{x}_1 + (k_1 + k_2)x_1 - k_2 x_2 = 0
$$

$$
m_2 \ddot{x}_2 + (k_2 + k_3)x_2 - k_2 x_1 = 0
$$

Natural frequencies are obtained from

$$
\det(K - \omega^2 M) = 0
$$

Normal modes are given by the eigenvectors of $M^{-1}K$. The visualization file is `problem_set_04_vis_problem_08_coupled_springs.html`.

## Interpretation

The motion decomposes into collective patterns. In one mode the masses move approximately together, and in the other they move oppositely. For generic initial conditions the two modes mix, producing visible energy exchange between the masses.

---

# Task 09 – Chain of $N$ Springs (Discrete Wave Model)

## Problem Statement

A chain of $N$ masses connected by identical springs models a discrete medium supporting wave propagation.

## Theory

Let $x_n(t)$ be the displacement of the $n$-th mass. For an interior mass, the net force comes from its neighbors.

## Step-by-Step Solution

For interior sites,

$$
m \ddot{x}_n = k(x_{n+1} - x_n) - k(x_n - x_{n-1})
$$

Therefore,

$$
m \ddot{x}_n = k(x_{n+1} - 2x_n + x_{n-1})
$$

for

$$
n = 2, 3, \dots, N-1
$$

The endpoint equations depend on the boundary conditions. For fixed ends one may take

$$
x_0 = 0,
\qquad
x_{N+1} = 0
$$

which gives

$$
m \ddot{x}_1 = k(x_2 - 2x_1)
$$

$$
m \ddot{x}_N = k(x_{N-1} - 2x_N)
$$

A local initial disturbance can be imposed by displacing one mass or a small group of masses near the center. Numerical integration shows the propagation of the pulse through the chain.

The characteristic speed scale increases with the spring stiffness and decreases with the mass. Dimensional reasoning gives

$$
v_{\mathrm{eff}} \propto \sqrt{\frac{k}{m}}
$$

## Final Result

Discrete equations of motion:

$$
m \ddot{x}_n = k(x_{n+1} - 2x_n + x_{n-1})
$$

for interior masses, with boundary conditions added at the ends. The visualization file is `problem_set_04_vis_problem_09_chain_of_springs.html`.

## Interpretation

This system is the discrete analogue of a continuous elastic medium. A local disturbance spreads because each mass communicates motion to its neighbors through the springs.

---

# Task 10 – Double Pendulum and Deterministic Chaos

## Problem Statement

Perform a numerical analysis of a double pendulum and visualize sensitivity to initial conditions using an ensemble of 50 nearby trajectories.

## Theory

The double pendulum is a nonlinear coupled system. For sufficiently energetic motion, nearby initial conditions diverge noticeably in time, which is a signature of deterministic chaos.

## Step-by-Step Solution

### Coordinates for animation

Let the pivot be at the origin. Then the first mass has coordinates

$$
x_1 = l_1 \sin \theta_1
$$

$$
y_1 = - l_1 \cos \theta_1
$$

The second mass has coordinates

$$
x_2 = x_1 + l_2 \sin \theta_2
$$

$$
y_2 = y_1 - l_2 \cos \theta_2
$$

### Standard numerical model

Introduce the variables

$$
\theta_1,
\qquad
\theta_2,
\qquad
\omega_1 = \dot{\theta}_1,
\qquad
\omega_2 = \dot{\theta}_2
$$

and integrate the standard double-pendulum equations numerically with RK4.

For the standardized parameters,

$$
m_1 = m_2 = 1,
\qquad
l_1 = l_2 = 1,
\qquad
g = 9.81
$$

a safe step is

$$
\Delta t \le 0.01\ \mathrm{s}
$$

### Stability check

The numerical solution should be checked by monitoring the total energy. If the time step is too large, the energy drift becomes clearly visible.

### Sensitivity to initial conditions

Use 50 systems with almost identical initial data, for example

$$
\theta_1(0) = \theta_{1,0},
\qquad
\theta_2(0) = \theta_{2,0} + \varepsilon_j
$$

where $\varepsilon_j$ spans a small interval such as

$$
10^{-4}\ \mathrm{rad} \le |\varepsilon_j| \le 10^{-2}\ \mathrm{rad}
$$

Initially, all trajectories remain close. After some time, they separate strongly even though the equations are deterministic.

## Final Result

Animation coordinates:

$$
x_1 = l_1 \sin \theta_1,
\qquad
y_1 = - l_1 \cos \theta_1
$$

$$
x_2 = l_1 \sin \theta_1 + l_2 \sin \theta_2
$$

$$
y_2 = - l_1 \cos \theta_1 - l_2 \cos \theta_2
$$

The system must be integrated numerically. The visualization file is `problem_set_04_vis_problem_10_double_pendulum_ensemble.html`.

## Interpretation

Chaos does not mean randomness of the equations. The evolution is fully deterministic, but extreme sensitivity to initial conditions makes long-term prediction effectively difficult. The 50-pendulum ensemble displays this divergence directly.