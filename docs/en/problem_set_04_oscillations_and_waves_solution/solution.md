# Problem Set 4 – Solutions: Oscillations and Waves

## Task 1 – Harmonic motion: motion parameters

### Problem Statement

A function describing harmonic motion is given:

$$
x(t) = A \cos(\omega t + \varphi)
$$

1. Determine the period $T$ and the frequency $f$.
2. Determine the maximum velocity and the maximum acceleration.
3. For $A = 0.2$ m, $f = 2$ Hz: calculate $\omega$, $v_{\max}$, and $a_{\max}$.

### Theory

Simple Harmonic Motion (SHM) is a type of periodic motion where the restoring force is directly proportional to the displacement. The kinematic parameters are derived by taking time derivatives of the position function $x(t)$.

### Step-by-Step Solution

**1. Period and Frequency**

The argument of the cosine function completes one full cycle ($2\pi$ radians) in one period $T$. Therefore:

$$
\omega T = 2\pi \implies T = \frac{2\pi}{\omega}
$$

Frequency $f$ is the reciprocal of the period:

$$
f = \frac{1}{T} = \frac{\omega}{2\pi}
$$

**2. Maximum Velocity and Acceleration**

Velocity is the first derivative of position with respect to time:

$$
v(t) = \frac{dx}{dt} = -A\omega \sin(\omega t + \varphi)
$$

The maximum velocity occurs when $|\sin(\omega t + \varphi)| = 1$:

$$
v_{\max} = A\omega
$$

Acceleration is the second derivative of position:

$$
a(t) = \frac{dv}{dt} = -A\omega^2 \cos(\omega t + \varphi)
$$

The maximum acceleration occurs when $|\cos(\omega t + \varphi)| = 1$:

$$
a_{\max} = A\omega^2
$$

**3. Numerical Calculations**

Given $A = 0.2$ m and $f = 2$ Hz:

$$
\omega = 2\pi f = 2\pi(2) = 4\pi \approx 12.57\ \text{rad/s}
$$

$$
v_{\max} = A\omega = 0.2 \cdot 4\pi = 0.8\pi \approx 2.51\ \text{m/s}
$$

$$
a_{\max} = A\omega^2 = 0.2 \cdot (4\pi)^2 = 0.2 \cdot 16\pi^2 = 3.2\pi^2 \approx 31.58\ \text{m/s}^2
$$

### Final Result

* $T = 2\pi/\omega$
* $f = \omega/2\pi$
* $v_{\max} = A\omega$
* $a_{\max} = A\omega^2$
* For the given values: $\omega \approx 12.57\ \text{rad/s}$, $v_{\max} \approx 2.51\ \text{m/s}$, $a_{\max} \approx 31.58\ \text{m/s}^2$.

### Interpretation

The maximum velocity occurs as the object passes through the equilibrium position ($x=0$), while the maximum acceleration occurs at the turning points ($x = \pm A$), where the restoring force is greatest.

---

## Task 2 – Energy of a harmonic oscillator

### Problem Statement

A system with $m = 1\ \text{kg}$, $k = 100\ \text{N/m}$, $x(0) = 2\ \text{m}$, and $v(0) = 1\ \text{m/s}$ is given.

1. Determine the natural frequency.
2. Calculate the total energy of the system.
3. For what displacement does the kinetic energy account for 50% of the total energy?

### Theory

The total mechanical energy $E$ of a harmonic oscillator is the sum of its kinetic energy $K$ and potential energy $U$:

$$
E = K + U = \frac{1}{2}mv^2 + \frac{1}{2}kx^2
$$

In a closed system, $E$ remains constant.

### Step-by-Step Solution

**1. Natural Frequency**

The angular frequency $\omega$ for a mass-spring system is:

$$
\omega = \sqrt{\frac{k}{m}} = \sqrt{\frac{100}{1}} = 10\ \text{rad/s}
$$

The natural frequency $f$ is:

$$
f = \frac{\omega}{2\pi} = \frac{10}{2\pi} \approx 1.59\ \text{Hz}
$$

**2. Total Energy**

Using the initial conditions:

$$
E = \frac{1}{2}(1)(1)^2 + \frac{1}{2}(100)(2)^2 = 0.5 + 200 = 200.5\ \text{J}
$$

**3. Displacement for 50% Kinetic Energy**

If $K = 0.5E$, then $U = 0.5E$ because $K + U = E$.

$$
\frac{1}{2}kx^2 = 0.5 E
$$

$$
x = \sqrt{\frac{E}{k}} = \sqrt{\frac{200.5}{100}} = \sqrt{2.005} \approx 1.416\ \text{m}
$$

### Final Result

* $\omega = 10\ \text{rad/s}$
* $E = 200.5\ \text{J}$
* $x \approx 1.416\ \text{m}$

### Interpretation

The total energy is defined by the initial state. When the energy is split equally between kinetic and potential forms, the displacement is $1/\sqrt{2}$ of the maximum amplitude $A$, since $E = \frac{1}{2}kA^2$.

---

## Task 3 – Harmonic wave

### Problem Statement

Wave equation: $y(x,t) = A \sin(kx - \omega t)$.

1. Determine the wavelength.
2. Determine the phase velocity.
3. Calculate $v$ for $k = 4\pi$, $\omega = 20\pi$.
4. Does the point $x = \lambda$ oscillate in phase with $x = 0$?

### Step-by-Step Solution

**1. Wavelength**

The wave number $k$ is defined as:

$$
k = \frac{2\pi}{\lambda} \implies \lambda = \frac{2\pi}{k}
$$

**2. Phase Velocity**

The velocity $v$ at which a point of constant phase moves is:

$$
v = \frac{\omega}{k}
$$

**3. Numerical Calculation**

$$
v = \frac{20\pi}{4\pi} = 5\ \text{units/s}
$$

**4. Phase Comparison**

The phase is $\Phi(x,t) = kx - \omega t$.
At $x = 0$: $\Phi_0 = -\omega t$.
At $x = \lambda$: $\Phi_\lambda = k\lambda - \omega t = \frac{2\pi}{\lambda}\lambda - \omega t = 2\pi - \omega t$.

Since the phase difference is exactly $2\pi$, the points oscillate in phase.

### Final Result

* $\lambda = 2\pi/k$
* $v = \omega/k = 5$
* Yes, they are in phase.

---

## Task 4 – Wave equation

### Problem Statement

Verify $y(x,t) = A \cos(kx - \omega t)$ satisfies $\frac{\partial^2 y}{\partial t^2} = v^2 \frac{\partial^2 y}{\partial x^2}$.

### Step-by-Step Solution

Calculate second derivatives:

$$
\frac{\partial y}{\partial t} = A\omega \sin(kx - \omega t) \implies \frac{\partial^2 y}{\partial t^2} = -A\omega^2 \cos(kx - \omega t)
$$

$$
\frac{\partial y}{\partial x} = -Ak \sin(kx - \omega t) \implies \frac{\partial^2 y}{\partial x^2} = -Ak^2 \cos(kx - \omega t)
$$

Substitute into the wave equation:

$$
-A\omega^2 \cos(kx - \omega t) = v^2 (-Ak^2 \cos(kx - \omega t))
$$

Dividing by the common terms:

$$
\omega^2 = v^2 k^2
$$

### Final Result

The relation is $v = \frac{\omega}{k}$.

---

## Task 5 – Superposition of waves, beats, and group velocity

### Problem Statement

Two harmonic waves are given:
$y_1(x,t)=A\sin(kx-\omega t)$
$y_2(x,t)=A\sin(kx-(\omega+\Delta\omega)t)$

1. Determine the resultant wave $y=y_1+y_2$ in product form.
2. Identify the beat frequency and beat period at $x=0$.
3. Interpret the envelope and carrier wave.

### Theory

The superposition principle states that the resultant displacement is the algebraic sum of individual wave displacements. When two waves of slightly different frequencies interfere, they produce "beats."

### Step-by-Step Solution

**1. Resultant Wave**

Using the trigonometric identity $\sin \alpha + \sin \beta = 2 \sin\left(\frac{\alpha + \beta}{2}\right) \cos\left(\frac{\alpha - \beta}{2}\right)$:

Let $\alpha = kx - \omega t$ and $\beta = kx - (\omega + \Delta\omega)t$.

$$
y = 2A \sin\left(\frac{2kx - (2\omega + \Delta\omega)t}{2}\right) \cos\left(\frac{\Delta\omega t}{2}\right)
$$

Assuming $\Delta\omega \ll \omega$, we can approximate the result as:

$$
y(x,t) = \left[ 2A \cos\left(\frac{\Delta\omega}{2}t\right) \right] \sin(kx - \omega t)
$$

**2. Beats at $x=0$**

At $x=0$, $y(0,t) = 2A \cos\left(\frac{\Delta\omega}{2}t\right) \sin(-\omega t)$. The intensity (amplitude squared) varies with the term $\cos^2(\frac{\Delta\omega}{2}t)$.
The beat frequency $f_{beat}$ is the difference between the two frequencies:

$$
f_{beat} = \frac{\Delta\omega}{2\pi}
$$

The beat period is:

$$
T_{beat} = \frac{1}{f_{beat}} = \frac{2\pi}{\Delta\omega}
$$

### Interpretation

* **Envelope:** The term $2A \cos(\frac{\Delta\omega}{2}t)$ describes the slow-moving "envelope" that modulates the amplitude.
* **Carrier:** The $\sin(kx - \omega t)$ term is the "carrier wave," representing the rapid oscillations within the envelope.

---

## Task 6 – Damped oscillator

### Problem Statement

Equation: $m \frac{d^2 x}{dt^2} + b \frac{dx}{dt} + k x = 0$.

1. Derive the general solution.
2. Classify the cases.

### Theory

This is a second-order linear homogeneous differential equation. We assume a solution of the form $x(t) = e^{rt}$.

### Step-by-Step Solution

Substituting $x = e^{rt}$ into the equation:

$$
mr^2 + br + k = 0 \implies r = \frac{-b \pm \sqrt{b^2 - 4mk}}{2m}
$$

Let $\gamma = \frac{b}{2m}$ and $\omega_0 = \sqrt{\frac{k}{m}}$. Then $r = -\gamma \pm \sqrt{\gamma^2 - \omega_0^2}$.

**Classification:**

1.  **Underdamped ($\gamma < \omega_0$):** $b^2 < 4mk$. The roots are complex.
    $x(t) = e^{-\gamma t}(C_1 \cos(\omega_d t) + C_2 \sin(\omega_d t))$, where $\omega_d = \sqrt{\omega_0^2 - \gamma^2}$.
2.  **Critically Damped ($\gamma = \omega_0$):** $b^2 = 4mk$. Real, repeated roots.
    $x(t) = (C_1 + C_2 t)e^{-\gamma t}$.
3.  **Overdamped ($\gamma > \omega_0$):** $b^2 > 4mk$. Real, distinct roots.
    $x(t) = C_1 e^{r_1 t} + C_2 e^{r_2 t}$.

---

## Task 7 – Forced oscillator and resonance

### Problem Statement

Equation: $m \ddot{x} + b \dot{x} + kx = F_0 \cos(\Omega t)$.

1. Solve for steady-state amplitude $A(\Omega)$.
2. Interpret resonance.

### Step-by-Step Solution

The steady-state solution is $x(t) = A \cos(\Omega t - \delta)$. Substituting this into the differential equation and solving for $A$:

$$
A(\Omega) = \frac{F_0}{\sqrt{(k - m\Omega^2)^2 + (b\Omega)^2}}
$$

To find the resonance frequency $\Omega_r$, we minimize the denominator:

$$
\Omega_r = \sqrt{\omega_0^2 - 2\gamma^2}
$$

### Interpretation

Resonance occurs when the driving frequency $\Omega$ is close to the natural frequency $\omega_0$, leading to a massive increase in oscillation amplitude.

---

## Task 8 – Two coupled springs

### Equations of Motion

For two masses $m_1, m_2$ and three springs $k_1, k_2, k_3$:

$$
\begin{pmatrix} 
m_1 & 0 \\ 
0 & m_2 
\end{pmatrix} 
\begin{pmatrix} 
\ddot{x}_1 \\ 
\ddot{x}_2 
\end{pmatrix} +
\begin{pmatrix} 
k_1 + k_2 & -k_2 \\ 
-k_2 & k_2 + k_3 
\end{pmatrix} 
\begin{pmatrix} 
x_1 \\ 
x_2 
\end{pmatrix} = 
\begin{pmatrix} 
0 \\ 
0 
\end{pmatrix}
$$

The natural frequencies are found by solving $\det(K - \omega^2 M) = 0$.

---

## Task 9 – Chain of $N$ springs (discrete wave model)

### Problem Statement

A system of $N$ masses connected by springs.
1. Write the equations of motion.
2. Observe pulse propagation and the effect of $k$ and $m$.

### Theory

A discrete chain of masses and springs serves as a model for a solid lattice. In the limit where the number of masses $N \to \infty$ and the spacing $a \to 0$, the discrete equations of motion transition into the continuous wave equation.

### Step-by-Step Solution

**1. Equations of Motion**

For the $i$-th mass $m$ in a chain where each mass is connected to its neighbors by springs of constant $k$, the force depends on the relative displacement of the neighbors $x_{i-1}$ and $x_{i+1}$:

$$
m \frac{d^2 x_i}{dt^2} = k(x_{i+1} - x_i) - k(x_i - x_{i-1})
$$

Rearranging for acceleration:

$$
\ddot{x}_i = \frac{k}{m} (x_{i+1} - 2x_i + x_{i-1})
$$

**2. Propagation Speed**

The speed of a disturbance (wave) in this lattice is proportional to the coupling strength. Analytically, the longitudinal wave speed $v$ is given by:

$$
v = a \sqrt{\frac{k}{m}}
$$

where $a$ is the equilibrium separation between masses.

### Interpretation

Increasing the spring constant $k$ (stiffening the "bonds") increases the propagation speed. Increasing the mass $m$ (increasing inertia) slows down the propagation.

---

## Task 10 – Double pendulum and deterministic chaos

### Problem Statement

Numerical analysis of a double pendulum system with 50 simultaneous copies to observe sensitivity to initial conditions.

### Theory

The double pendulum is a classic example of a simple Hamiltonian system that exhibits **deterministic chaos**. While the equations are deterministic, the motion becomes highly sensitive to initial conditions at high energy levels. This sensitivity is characterized by the **Lyapunov exponent**, which describes the rate at which two trajectories in phase space diverge.

### Numerical Implementation (RK4)

To solve the system, the two second-order differential equations are broken into four first-order equations:

$$
\frac{d}{dt} \begin{pmatrix} \theta_1 \\ \theta_2 \\ \omega_1 \\ \omega_2 \end{pmatrix} = \mathbf{f}(\theta_1, \theta_2, \omega_1, \omega_2)
$$

The Runge-Kutta 4th Order (RK4) method is used to ensure energy conservation and numerical stability over long integration times.

### Interpretation of Chaos

In the "ensemble" simulation, 50 pendulums start with a difference in $\theta_2$ of only $10^{-4}$ rad. Initially, they appear as a single rod. However, as time progresses, the small differences are amplified exponentially. Eventually, the pendulums spread across the entire available phase space, demonstrating that long-term prediction of the state is impossible despite knowing the exact laws of motion.