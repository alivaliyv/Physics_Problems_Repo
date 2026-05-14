# Task 01 – Lorentz force

## Problem Statement

Given data: $\vec{B} = (0,0,1)\ \mathrm{T}$, $\vec{v} = (2,3,0)\ \mathrm{m/s}$, and $q = 1\ \mathrm{mC}$.
1. Determine the Lorentz force $\vec{F}$.
2. Solve the equation of motion assuming $\vec{r}(0) = (0,0,0)$.
3. Calculate the magnitude $|\vec{F}|$.
4. Does the magnetic force do work?
5. Determine the radius of the trajectory for $m = 0.01\ \mathrm{kg}$.
6. How will $r$ change when $B$ is doubled?

## Theory

The magnetic part of the Lorentz force is given by:

$$
\vec{F} = q(\vec{v} \times \vec{B})
$$

Newton's second law $\vec{F} = m\vec{a}$ describes the motion. Since $\vec{F}$ is always perpendicular to $\vec{v}$, the magnetic field changes the direction of velocity but not its magnitude. For a charge moving perpendicular to a uniform $\vec{B}$ field, the motion is circular with a centripetal force:

$$
F_c = \frac{mv^2}{r} = qvB
$$

## Step-by-Step Solution

**1. Force Vector**

$$
\vec{F} = (10^{-3}) \begin{pmatrix} 2 \\ 3 \\ 0 \end{pmatrix} \times \begin{pmatrix} 0 \\ 0 \\ 1 \end{pmatrix} = 10^{-3} \begin{pmatrix} 3(1) - 0(0) \\ 0(0) - 2(1) \\ 2(0) - 3(0) \end{pmatrix} = \begin{pmatrix} 0.003 \\ -0.002 \\ 0 \end{pmatrix}\ \mathrm{N}
$$

**2. Equation of Motion**

The acceleration is $\vec{a} = \vec{F}/m$. Since $\vec{v}$ is in the $xy$-plane and $\vec{B}$ is along $z$, the particle undergoes circular motion in the $xy$-plane.
The cyclotron frequency is $\omega = \frac{qB}{m} = \frac{10^{-3} \cdot 1}{0.01} = 0.1\ \mathrm{rad/s}$.

**3. Magnitude of Force**

$$
|\vec{F}| = \sqrt{0.003^2 + (-0.002)^2} = \sqrt{1.3 \times 10^{-5}} \approx 3.61 \times 10^{-3}\ \mathrm{N}
$$

**4. Work Done**

The work done $W$ by a force is $W = \int \vec{F} \cdot d\vec{l}$. Since $\vec{F} \perp \vec{v}$, the dot product $\vec{F} \cdot \vec{v} = 0$. Thus, the magnetic force does **zero work**.

**5. Radius of Trajectory**

Initial speed $v = \sqrt{2^2 + 3^2} = \sqrt{13} \approx 3.606\ \mathrm{m/s}$.

$$
r = \frac{mv}{qB} = \frac{0.01 \cdot \sqrt{13}}{10^{-3} \cdot 1} = 10\sqrt{13} \approx 36.06\ \mathrm{m}
$$

**6. Effect of Doubling B**

Since $r \propto 1/B$, if $B$ is doubled, the radius is halved ($r' = r/2$).

## Final Result

$\vec{F} = (3, -2, 0)\ \mathrm{mN}$. The particle moves in a circle of radius $36.06\ \mathrm{m}$. Doubling $B$ reduces the radius to $18.03\ \mathrm{m}$.

## Interpretation

The magnetic field acts as a steering force. It cannot speed up or slow down a particle (no work), which is a fundamental property distinguishing it from the electric field.
# Task 02 – Velocity selection (crossed fields)

## Problem Statement

Given crossed fields $\vec{E} = (0,E,0)$ and $\vec{B} = (0,0,B)$.
1. Derive the condition for rectilinear motion.
2. Calculate $v_d$ for $E = 400\ \mathrm{V/m}$, $B = 0.8\ \mathrm{T}$.
3. Does kinetic energy change?
4. Interpret the operating principle.

## Theory

A particle with charge $q$ and velocity $\vec{v} = (v, 0, 0)$ experiences two forces:
Electric force: $\vec{F}_e = q\vec{E} = (0, qE, 0)$.
Magnetic force: $\vec{F}_m = q(\vec{v} \times \vec{B}) = q(v\hat{i} \times B\hat{k}) = (0, -qvB, 0)$.

## Step-by-Step Solution

**1. Rectilinear Motion Condition**

For the particle to move in a straight line, the net force must be zero:

$$
\sum F_y = qE - qvB = 0
$$

$$
v = \frac{E}{B}
$$

**2. Calculation**

$$
v_d = \frac{400}{0.8} = 500\ \mathrm{m/s}
$$

**3. Kinetic Energy**

In steady motion (rectilinear), $\vec{v}$ is constant. Therefore, $\Delta E_k = 0$. The work done by the electric field is exactly cancelled by the fact that the particle does not deviate in the direction of the electric force.

## Final Result

The selection velocity is $v = E/B = 500\ \mathrm{m/s}$.

## Interpretation

This device acts as a filter. Only particles with the specific velocity $v = E/B$ experience zero net force and pass through the exit slit. All other particles are deflected by either the dominant electric or magnetic force.
# Task 03 – Magnetic moment of a loop

## Problem Statement

A loop with $N$ turns, area $S$, and current $I$ is in a uniform $\vec{B}$ field.
1. Define magnetic moment $\vec{\mu}$.
2. Determine torque $\vec{M}$.
3. Find angle for maximum torque.
4. Determine potential energy $U$.
5. Indicate stable/unstable positions.

## Theory

The magnetic moment $\vec{\mu}$ represents the strength and orientation of a magnetic source.

## Step-by-Step Solution

**1. Magnetic Moment**

$$
\vec{\mu} = N I S \hat{n}
$$

where $\hat{n}$ is the unit vector perpendicular to the loop area (right-hand rule).

**2. Torque**

$$
\vec{M} = \vec{\mu} \times \vec{B}
$$

Magnitude: $M = \mu B \sin \theta$.

**3. Maximum Torque**

The torque is maximum when $\sin \theta = 1$, which occurs at $\theta = 90^\circ$ (the loop plane is parallel to $\vec{B}$).

**4. Potential Energy**

$$
U = -\vec{\mu} \cdot \vec{B} = -\mu B \cos \theta
$$

**5. Stability**

*   **Stable Equilibrium:** $\theta = 0^\circ$. $U$ is at a minimum ($-\mu B$). $\vec{\mu}$ is parallel to $\vec{B}$.
*   **Unstable Equilibrium:** $\theta = 180^\circ$. $U$ is at a maximum ($+\mu B$). $\vec{\mu}$ is anti-parallel to $\vec{B}$.

## Final Result

Torque is $\vec{\mu} \times \vec{B}$ and energy is $-\vec{\mu} \cdot \vec{B}$.
# Task 04 – Rotating loop (induction)

## Interpretation

The loop behaves like a compass needle, always attempting to align its magnetic moment with the external magnetic field to reach the lowest energy state.'# Task 04 – Rotating loop (induction)

## Problem Statement

Loop (area $S$, $N$ turns) rotates with $\omega$ around an axis perpendicular to $\vec{B}$.
1. Determine $\Phi(t)$.
2. Determine $\mathcal{E}(t)$.
3. Calculate amplitude $\mathcal{E}_0$.
4. Dependence on $\omega$.
5. Interpret the mechanism.

## Theory

Faraday's Law of Induction states:

$$
\mathcal{E} = -N \frac{d\Phi}{dt}
$$

## Step-by-Step Solution

**1. Magnetic Flux**

Assuming the angle $\theta(t) = \omega t$:

$$
\Phi(t) = \vec{B} \cdot \vec{S} = B S \cos(\omega t)
$$

**2. Induced EMF**

$$
\mathcal{E}(t) = -N \frac{d}{dt}(BS \cos(\omega t)) = -N BS (-\omega \sin(\omega t))
$$

$$
\mathcal{E}(t) = NBS\omega \sin(\omega t)
$$

**3. Amplitude**

The maximum value is reached when $\sin(\omega t) = 1$:

$$
\mathcal{E}_0 = NBS\omega
$$

**4. Dependence on $\omega$**

The amplitude is directly proportional to the angular velocity ($\mathcal{E}_0 \propto \omega$). Doubling the rotation speed doubles the peak voltage.

## Final Result

$\mathcal{E}(t) = \mathcal{E}_0 \sin(\omega t)$ where $\mathcal{E}_0 = NBS\omega$.

## Interpretation

This is the fundamental principle of an AC generator. Mechanical energy used to rotate the loop is converted into electrical energy via the change in magnetic flux through the rotating area.
# Task 05 – Induction in a moving rod

## Problem Statement

Rod length $L=0.25\ \mathrm{m}$, $v=4\ \mathrm{m/s}$, $\vec{B}=0.6\ \mathrm{T}$ (perpendicular).
1. Determine $\mathcal{E}$.
2. Potential difference.
3. Non-perpendicular motion.
4. Dependence on $L$.
5. Source of energy.

## Theory

Motional EMF is generated when a conductor moves through a magnetic field, causing the Lorentz force to separate charges.

## Step-by-Step Solution

**1. Induced EMF**

For perpendicular motion:

$$
\mathcal{E} = B L v = (0.6)(0.25)(4) = 0.6\ \mathrm{V}
$$

**2. Potential Difference**

The potential difference $U$ between the ends of the rod is equal to the induced EMF, $U = 0.6\ \mathrm{V}$.

**3. Non-perpendicular Motion**

If the velocity $\vec{v}$ makes an angle $\theta$ with $\vec{B}$:

$$
\mathcal{E} = B L v \sin \theta
$$

If $\vec{v} \parallel \vec{B}$, $\mathcal{E} = 0$.

**4. Dependence on $L$**

EMF is linearly proportional to $L$. A longer rod "sweeps" more field lines per unit time.

## Final Result

$\mathcal{E} = 0.6\ \mathrm{V}$.

## Interpretation

The energy comes from the **mechanical work** done by the external agent moving the rod. If the rod were part of a closed circuit, a current would flow, creating a magnetic braking force that the agent must overcome.
# Task 06 – Rod on metal rails

## Problem Statement

Rod $m=0.20\ \mathrm{kg}$ on rails $L=0.30\ \mathrm{m}$, $\alpha=25^\circ$, $B=0.80\ \mathrm{T}$, $R=0.50\ \Omega$.
1. Determine $\mathcal{E}(v)$ and $I(v)$.
2. Show braking force exists.
3. Write equation of motion.
4. Determine $v_\infty$.
5. Power balance.

## Theory

As the rod slides down, it generates EMF. The resulting current interacts with the $B$-field to create a force opposing the motion (Lenz's Law).

## Step-by-Step Solution

**1. EMF and Current**

$$
\mathcal{E} = BLv, \quad I = \frac{\mathcal{E}}{R} = \frac{BLv}{R}
$$

**2. Magnetic Braking Force**

The force on a current-carrying wire is $F_m = ILB$. Substituting $I$:

$$
F_m = \left( \frac{BLv}{R} \right) LB = \frac{B^2 L^2}{R} v
$$

By the right-hand rule, this force opposes $v$.

**3. Equation of Motion**

Summing forces along the incline:

$$
m \frac{dv}{dt} = mg \sin \alpha - \frac{B^2 L^2}{R} v
$$

**4. Terminal Velocity**

At $v_\infty$, acceleration is zero ($dv/dt = 0$):

$$
mg \sin \alpha = \frac{B^2 L^2}{R} v_\infty \implies v_\infty = \frac{mg R \sin \alpha}{B^2 L^2}
$$

$$
v_\infty = \frac{0.2 \cdot 9.81 \cdot 0.5 \cdot \sin 25^\circ}{0.8^2 \cdot 0.3^2} \approx \frac{0.4146}{0.0576} \approx 7.20\ \mathrm{m/s}
$$

**5. Power Balance**

Mechanical power input: $P_{mech} = F_{grav} \cdot v = (mg \sin \alpha) v$.
Electrical power dissipation: $P_{heat} = I^2 R = (\frac{BLv}{R})^2 R = \frac{B^2 L^2 v^2}{R}$.
In steady state, $mg \sin \alpha = \frac{B^2 L^2 v}{R}$, so $P_{mech} = P_{heat}$.

## Final Result

$v_\infty \approx 7.20\ \mathrm{m/s}$. Power balance is confirmed as $P = I^2 R$.

## Interpretation

This system is a linear generator. Gravity does work, which is converted into electrical energy and then dissipated as heat in the resistor.
# Task 07 – Loop pulled into a B field

## Problem Statement

Rectangular loop ($a \times b$) enters $B$ field with velocity $v$.
1. Flux $\Phi(t)$.
2. $\mathcal{E}$ and $I$.
3. Braking force $F(v)$.
4. Power balance.
5. Current when fully inside.

## Step-by-Step Solution

**1. Flux**

Let $x$ be the distance the loop has entered the field ($x = vt$):

$$
\Phi(t) = B \cdot (x \cdot b) = B b v t
$$

**2. EMF and Current**

$$
\mathcal{E} = \frac{d\Phi}{dt} = Bbv, \quad I = \frac{Bbv}{R}
$$

**3. Braking Force**

Only the leading edge (length $b$) experiences a force $F = IlB$ because the trailing edge is outside:

$$
F = \left( \frac{Bbv}{R} \right) b B = \frac{B^2 b^2 v}{R}
$$

**4. Power**

$P_{mech} = F v = \frac{B^2 b^2 v^2}{R}$.
$P_{elec} = I^2 R = (\frac{Bbv}{R})^2 R = \frac{B^2 b^2 v^2}{R}$. Equal.

**5. Fully Inside**

When the loop is entirely in the uniform field, $\Phi = B \cdot a \cdot b = \text{const}$. Thus, $d\Phi/dt = 0$ and **$I = 0$**.

## Interpretation

Current only flows when the magnetic flux is *changing*. This happens during the entry and exit phases. Inside the uniform field, the EMFs from the two sides of the loop cancel out.
# Task 08 – Self-induction

## Problem Statement

RL circuit: $L=0.20\ \mathrm{H}, R=5.0\ \Omega, U=12\ \mathrm{V}$.
1. Steady current $I_0$.
2. Derive $I(t)$ after disconnection.
3. Energy $W$.
4. Energy to heat conversion.
5. Overvoltage explanation.

## Step-by-Step Solution

**1. Steady Current**

$$
I_0 = \frac{U}{R} = \frac{12}{5} = 2.4\ \mathrm{A}
$$

**2. Decay Phase**

The loop equation is $L \frac{dI}{dt} + IR = 0$.

$$
I(t) = I_0 e^{-t/\tau}, \quad \tau = \frac{L}{R} = \frac{0.2}{5} = 0.04\ \mathrm{s}
$$

**3. Stored Energy**

$$
W = \frac{1}{2} L I_0^2 = 0.5 \cdot 0.2 \cdot (2.4)^2 = 0.576\ \mathrm{J}
$$

**4. Heat Conversion**

$$
\int_0^\infty I^2 R dt = R I_0^2 \int_0^\infty e^{-2Rt/L} dt = R I_0^2 \left[ -\frac{L}{2R} e^{-2Rt/L} \right]_0^\infty = \frac{1}{2} L I_0^2
$$

**5. Overvoltage**

When the circuit is opened, $dt$ is very small. Since $U_L = -L \frac{dI}{dt}$, a massive change in current over a tiny interval creates a high voltage "spike" (arc).

## Interpretation

Inductors resist changes in current. The stored magnetic energy ensures the current cannot drop to zero instantaneously, forcing it to dissipate through the resistor or an arc.
# Task 09 – Ideal vs. real transformer

## Problem Statement

Explain transformer operation, ideal vs. real properties, losses, and efficiency.

## Theory

A transformer consists of two coils (primary and secondary) linked by a common magnetic flux $\Phi$ in a core.

## Detailed Explanation

**1. Mechanism**

An AC voltage $U_1$ in the primary creates a changing $\Phi$. According to Faraday's law, this induces $U_2$ in the secondary:

$$
U_1 = N_1 \frac{d\Phi}{dt}, \quad U_2 = N_2 \frac{d\Phi}{dt} \implies \frac{U_2}{U_1} = \frac{N_2}{N_1} = \vartheta
$$

**2. Ideal Transformer**

*   Zero resistance in coils.
*   Infinite core permeability (no flux leakage).
*   No energy losses ($P_1 = P_2$).

**3. Real Transformer Losses**

*   **Copper Losses:** Joule heating ($I^2R$) in the windings.
*   **Hysteresis Losses:** Energy to re-magnetize the core each cycle.
*   **Eddy Current Losses:** Currents induced in the core material (minimized by laminating).
*   **Flux Leakage:** Not all flux from primary reaches secondary.

**4. Typical Values**

*   Efficiency: $95\% \text{ to } 99\%$ for large power transformers.
*   Turns ratio: Can vary from $0.01$ (step-down) to $100$ (step-up).

## Interpretation

Transformers are highly efficient but never perfect. Laminated steel cores are essential to reduce heat losses from eddy currents.
# Task 10 – Eddy currents

## Problem Statement

Usage of eddy currents for braking, materials, advantages, and increasing force.

## Detailed Explanation

**1. Mechanism of Braking**

When a solid conductor moves through a non-uniform $B$ field, "whirlpools" of current (eddy currents) are induced. These currents create their own magnetic fields that oppose the motion (Lenz's Law), resulting in a non-contact braking force.

**2. Advantages and Disadvantages**

*   **Pros:** No mechanical wear (no friction), smooth operation, high reliability.
*   **Cons:** Ineffective at low speeds (force $\propto v$), generates significant heat in the conductor.

**3. Materials**

Best materials are those with high electrical conductivity but non-magnetic properties to avoid direct attraction, such as **Copper** or **Aluminum**.

**4. Increasing Braking Force**

*   Increase the external magnetic field strength $B$.
*   Use materials with lower electrical resistance $R$.
*   Increase the velocity of motion $v$.

## Interpretation

Eddy current brakes are ideal for high-speed trains and roller coasters where mechanical brakes would wear out too quickly. They convert kinetic energy directly into thermal energy within the moving part.