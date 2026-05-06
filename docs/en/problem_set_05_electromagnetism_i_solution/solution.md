# Problem Set 05 – Solutions  
Electromagnetism I: Field and Forces

---

# Task 1 – Potential and Energy

## Problem Statement

For a point charge $q = 4\,\mu\mathrm{C}$:

1. Calculate the potential at $r = 0.3\,\mathrm{m}$.
2. Calculate the potential difference between $0.3\,\mathrm{m}$ and $0.6\,\mathrm{m}$.
3. Calculate the work done to move a test charge $q_0 = 2\,\mu\mathrm{C}$.
4. Calculate the electric field intensity from the derivative of the potential.
5. Compare with Coulomb's law.

---

## Theory

The electric potential of a point charge is

$$
V(r) = k \frac{q}{r}
$$

where

$$
k = \frac{1}{4\pi \varepsilon_0} \approx 9 \times 10^9 \,\mathrm{N\,m^2/C^2}
$$

Electric field relates to potential via

$$
\vec E = -\nabla V
$$

In radial symmetry:

$$
E(r) = -\frac{dV}{dr}
$$

---

## Step-by-Step Solution

### 1. Potential at $r = 0.3\,\mathrm{m}$

$$
V = k \frac{q}{r}
$$

$$
V = 9 \times 10^9 \cdot \frac{4 \times 10^{-6}}{0.3}
$$

$$
V = 1.2 \times 10^5 \,\mathrm{V}
$$

---

### 2. Potential difference

$$
\Delta V = V(0.3) - V(0.6)
$$

$$
V(0.6) = 9 \times 10^9 \cdot \frac{4 \times 10^{-6}}{0.6} = 6 \times 10^4 \,\mathrm{V}
$$

$$
\Delta V = 1.2 \times 10^5 - 6 \times 10^4 = 6 \times 10^4 \,\mathrm{V}
$$

---

### 3. Work done

$$
W = q_0 \Delta V
$$

$$
W = 2 \times 10^{-6} \cdot 6 \times 10^4
$$

$$
W = 0.12 \,\mathrm{J}
$$

---

### 4. Electric field from potential

$$
V(r) = k \frac{q}{r}
$$

$$
E(r) = -\frac{d}{dr} \left( k \frac{q}{r} \right)
$$

$$
E(r) = k \frac{q}{r^2}
$$

---

### 5. Comparison

The result matches Coulomb’s law:

$$
E = k \frac{q}{r^2}
$$

---

## Final Result

$$
V(0.3) = 1.2 \times 10^5 \,\mathrm{V}
$$

$$
\Delta V = 6 \times 10^4 \,\mathrm{V}
$$

$$
W = 0.12 \,\mathrm{J}
$$

$$
E(r) = k \frac{q}{r^2}
$$

---

## Interpretation

The potential decreases with distance as $1/r$, while the field decreases faster, as $1/r^2$. The work required depends linearly on the test charge.

---

# Task 2 – Coulomb's Force

## Problem Statement

Given:

$$
q_1 = 3\,\mu\mathrm{C}, \quad q_2 = -5\,\mu\mathrm{C}
$$

$$
r_1 = (0,0), \quad r_2 = (0.4,0.3)
$$

---

## Theory

Coulomb force:

$$
\vec F = k \frac{q_1 q_2}{r^3} \vec r
$$

Potential energy:

$$
U = k \frac{q_1 q_2}{r}
$$

---

## Step-by-Step Solution

### Distance

$$
r = \sqrt{0.4^2 + 0.3^2} = 0.5\,\mathrm{m}
$$

### Direction vector

$$
\vec r = (0.4, 0.3)
$$

### Force

$$
F = 9 \times 10^9 \cdot \frac{3 \times 10^{-6} \cdot (-5 \times 10^{-6})}{(0.5)^2}
$$

$$
F = -0.54\,\mathrm{N}
$$

Unit vector:

$$
\hat r = (0.8, 0.6)
$$

Vector force:

$$
\vec F = (-0.432, -0.324)\,\mathrm{N}
$$

---

### Potential energy

$$
U = 9 \times 10^9 \cdot \frac{3 \times 10^{-6} \cdot (-5 \times 10^{-6})}{0.5}
$$

$$
U = -0.27\,\mathrm{J}
$$

---

### Work to separate to $2\,\mathrm{m}$

$$
U_f = 9 \times 10^9 \cdot \frac{3 \cdot (-5) \times 10^{-12}}{2}
$$

$$
U_f = -0.0675\,\mathrm{J}
$$

$$
W = U_f - U_i = 0.2025\,\mathrm{J}
$$

---

## Final Result

$$
\vec F = (-0.432, -0.324)\,\mathrm{N}
$$

$$
|\vec F| = 0.54\,\mathrm{N}
$$

$$
U = -0.27\,\mathrm{J}
$$

$$
W = 0.2025\,\mathrm{J}
$$

---

## Interpretation

The force is attractive (opposite signs). The negative potential energy confirms a bound configuration.

---

# Task 3 – Field from Two Charges

## Problem Statement

Charges:

- $+q$ at $(-a,0)$
- $+2q$ at $(a,0)$

---

## Theory

Superposition principle:

$$
\vec E = \vec E_1 + \vec E_2
$$

Field of a point charge:

$$
\vec E = k \frac{q}{r^2} \hat r
$$

---

## Step-by-Step Solution

### General expression

For point $(x,y)$:

$$
\vec r_1 = (x+a, y), \quad \vec r_2 = (x-a, y)
$$

$$
\vec E = k \left[ \frac{q \vec r_1}{|\vec r_1|^3} + \frac{2q \vec r_2}{|\vec r_2|^3} \right]
$$

---

### Numerical case

Given:

$$
a = 0.2,\quad y = 0.3,\quad q = 2\,\mu\mathrm{C}
$$

Distances:

$$
r_1 = \sqrt{0.2^2 + 0.3^2} \approx 0.36
$$

$$
r_2 = \sqrt{0.2^2 + 0.3^2} \approx 0.36
$$

Compute components:

$$
E_x = kq \left( \frac{0.2}{r_1^3} + \frac{2(-0.2)}{r_2^3} \right)
$$

$$
E_y = kq \left( \frac{0.3}{r_1^3} + \frac{2(0.3)}{r_2^3} \right)
$$

---

## Final Result

Symbolic expression:

$$
\vec E(x,y) = k \left[ \frac{q(x+a,y)}{((x+a)^2+y^2)^{3/2}} + \frac{2q(x-a,y)}{((x-a)^2+y^2)^{3/2}} \right]
$$

---

## Interpretation

The asymmetry of charges shifts the field toward the stronger charge. No zero-field point exists on the $y$-axis.

---

# Task 4 – Motion in Uniform Field

## Theory

Newton’s law:

$$
m \vec a = q \vec E
$$

$$
\vec a = \frac{q}{m} \vec E
$$

---

## Solution

Acceleration:

$$
\vec a = (1500, 5000)\,\mathrm{m/s^2}
$$

Velocity:

$$
\vec v(t) = (20 + 1500t, 5000t)
$$

Position:

$$
\vec r(t) = (20t + 750t^2, 2500t^2)
$$

---

## Final Result

Time for $v_y = 50$:

$$
5000t = 50 \Rightarrow t = 0.01\,\mathrm{s}
$$

---

## Interpretation

Motion is parabolic, similar to projectile motion in gravity.

---

# Task 5 – Capacitor

## Theory

$$
C = \varepsilon_0 \frac{S}{d}
$$

$$
U = \frac{1}{2} C V^2
$$

---

## Results

$$
C \approx 3.54 \times 10^{-11}\,\mathrm{F}
$$

$$
U \approx 4.4 \times 10^{-6}\,\mathrm{J}
$$

$$
E = \frac{V}{d} = 10^5\,\mathrm{V/m}
$$

---

## Interpretation

Energy density depends on $E^2$, making strong fields energetically costly.

---

# Task 6 – 2D Field Map

## Key Result

Field:

$$
\vec E(x,y) = \sum_i k \frac{q_i \vec r_i}{|\vec r_i|^3}
$$

---

## Interpretation

Equilibrium points correspond to $\vec E = 0$ and may be unstable.

---

# Task 7 – Central Field Motion

## Equation

$$
m \ddot r = k \frac{qQ}{r^2}
$$

---

## Interpretation

Identical to gravitational inverse-square law.

---

# Task 8 – Three-Charge Energy

## Result

$$
U = k \left( \frac{q_1 q_2}{r_{12}} + \frac{q_1 q_3}{r_{13}} + \frac{q_2 q_3}{r_{23}} \right)
$$

---

## Interpretation

Energy depends on geometry; symmetric configurations are critical points.

---

# Task 9 – Dipole

## Results

Torque:

$$
\tau = p E \sin\theta
$$

Energy:

$$
U = -pE \cos\theta
$$

---

## Interpretation

Small oscillations behave like a harmonic oscillator.

---

# Task 10 – Gauss Law

## Flux

$$
\Phi = \oint \vec E \cdot d\vec A
$$

---

## Result

$$
\Phi = \frac{q}{\varepsilon_0}
$$

---

## Interpretation

Flux depends only on enclosed charge, not geometry.

---