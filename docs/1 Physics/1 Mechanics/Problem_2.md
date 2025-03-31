# Problem 2

## Investigating the Dynamics of a Forced Damped Pendulum

## 1. Theoretical Foundation: 

### 1.1 Governing Equation

The motion of a **forced damped pendulum** is governed by the following second-order differential equation:

$$ 
\frac{d^2 \theta}{dt^2} + b \frac{d\theta}{dt} + \frac{g}{L} \sin \theta = A \cos(\omega t) 
$$

where:
- $ \theta $ is the angular displacement,
- $ \ b $ is the damping coefficient,
- $ \ g $ is the gravitational acceleration,
- $ \ L  $ is the length of the pendulum,
- $ \ A $ is the amplitude of the external forcing,
- $ \omega $ is the driving frequency,
- $ \frac{d^2 \theta}{dt^2} $ represents the angular acceleration,
- $ b \frac{d\theta}{dt} $ is the damping term (proportional to velocity),
- $ \frac{g}{L} \sin \theta $ represents the restoring force due to gravity,
- $ A \cos(\omega t) $ is the external periodic driving force.

For small-angle approximations $$ \theta \approx \sin\theta $$the equation simplifies to:

$$ 
\frac{d^2 \theta}{dt^2} + b \frac{d\theta}{dt} + \frac{g}{L} \theta = A \cos(\omega t) 
$$

This is a **linear non-homogeneous differential equation** that describes **oscillatory motion with damping and external forcing**.

---

### **1.2 Example: Solving for Small-Angle Oscillations**



The equation simplifies to:

$$ 
\frac{d^2 \theta}{dt^2} + 0.2 \frac{d\theta}{dt} + 9.8 \theta = \cos(2t) 
$$

A trial solution for the steady-state response is:

$$ 
\theta(t) = C \cos(2t) + D \sin(2t) 
$$

Using the method of **undetermined coefficients**, we find:

$$ 
C = \frac{A}{\sqrt{(g/L - \omega^2)^2 + b^2 \omega^2}} 
$$

$$ 
D = \frac{b \omega A}{\sqrt{(g/L - \omega^2)^2 + b^2 \omega^2}} 
$$

Substituting the given values, we can compute $$ C $$ and $$ D $$ obtaining the particular solution.

---

### **1.3 Resonance Conditions and Energy Implications**

**Resonance** occurs when the **driving frequency** $$ \omega $$ is close to the **natural frequency** $$ \omega_0 $$, given by:

$$ 
\omega_0 = \sqrt{\frac{g}{L}} 
$$

For our example:

$$ 
\omega_0 = \sqrt{\frac{9.8}{1}} = 3.13 \text{ rad/s} 
$$

When $$ \omega \approx \omega_0 $$, the amplitude of oscillations increases significantly, leading to **resonance**. 

### **Effects of Resonance on Energy:**
- When **damping is low**, resonance can cause large oscillations, leading to **mechanical failure**.
- The **total energy** of the system is given by:

  $$ 
  E = \frac{1}{2} I \left( \frac{d\theta}{dt} \right)^2 + mgL(1 - \cos\theta) 
  $$

  where $$ I = mL^2 $$ is the moment of inertia.
- In the presence of **resonance**, the system absorbs **maximum energy** from the external force, increasing **kinetic and potential energy**.
- If **damping is large**, energy dissipation occurs, preventing excessive oscillations.

---

### **1.4 Conclusion**
- The forced damped pendulum exhibits **complex dynamics** depending on damping and external forcing.
- **Resonance** plays a crucial role in energy transfer, influencing oscillation amplitude.
- Understanding these principles helps in **engineering applications**, such as **seismic design**, **vehicle suspension systems**, and **wave energy harvesting**.


## 2. Analysis of Dynamics

### **2. Investigation of Key Parameters in Forced Damped Pendulum Motion**

### **2.1 Influence of Damping Coefficient $$ b $$**

The damping coefficient affects the system's energy dissipation. The equation of motion is:

$$ 
\frac{d^2 \theta}{dt^2} + b \frac{d\theta}{dt} + \frac{g}{L} \sin \theta = A \cos(\omega t) 
$$

where $$ b \frac{d\theta}{dt} $$ represents the **damping force**. Different values of $$ b $$ lead to different behaviors:

- **Small $$ b $$ (Underdamping):** The pendulum oscillates with a slow decrease in amplitude.
- Critical Damping $$ b = 2\sqrt{g/L} $$
The system returns to equilibrium **without oscillating**.
- **Large $$ b $$ (Overdamping):** Motion is slow, and the system returns to equilibrium **without oscillations**.

For **small damping**, under external forcing, the system may exhibit **chaotic behavior**.

---

### **2.2 Influence of Driving Amplitude $$ A $$**

The term $$ A \cos(\omega t) $$ introduces an external force into the system. The response of the pendulum depends on $$ A $$

- **Small $$ A $$** The system oscillates with small, periodic motion.
- **Intermediate $$ A $$** The oscillation amplitude increases, and **resonance** effects appear if $$ \omega \approx \omega_0 $$
- **Large $$ A $$** The pendulum enters a **nonlinear regime**, possibly flipping over and displaying **chaotic motion**.

At **high amplitudes**, energy input overcomes damping, leading to **unpredictable trajectories**.

---

## **2.3 Influence of Driving Frequency $$ \omega $$**

The **driving frequency** $$ \omega $$ determines the system’s response relative to its **natural frequency** $$ \omega_0 $$:

$$ 
\omega_0 = \sqrt{\frac{g}{L}} 
$$

- **If $$ \omega \ll \omega_0 $$** The system does not respond effectively.
- **If $$ \omega \approx \omega_0 $$** **Resonance** occurs, causing large oscillations.
- **If $$ \omega \gg \omega_0 $$** The system cannot follow the rapid forcing, and oscillations remain small.

For certain values of $$ \omega $$ the system transitions from **periodic** to **chaotic motion**.

---

## **2.4 Transition Between Regular and Chaotic Motion**

The pendulum's motion shifts from **regular (periodic) motion** to **chaos** as system parameters change.

- **Regular (Periodic) Motion:** The pendulum follows a repeating trajectory.
- **Quasi-Periodic Motion:** The system remains structured but does not repeat exactly.
- **Chaotic Motion:** Small initial differences lead to drastically different results (**sensitive dependence on initial conditions**).

### **Physical Interpretation of Chaos**
- Chaos emerges due to **nonlinearity** in the system.
- The **phase space trajectory** forms fractal-like structures.
- The system exhibits **aperiodic oscillations**, where no two cycles are identical.
- Chaotic dynamics are observed in **weather systems, celestial mechanics, and turbulence**.

---

## **2.5 Conclusion**
- The damping coefficient $$ b $$ driving amplitude $$ A $$ and frequency $$ \omega $$ dictate whether the system remains **periodic or enters chaos**.
- **Resonance** occurs when $$ \omega \approx \omega_0 $$ amplifying oscillations.
- The transition to **chaotic motion** occurs at certain parameter values, with **important implications** in engineering and physics.

![alt text](image.png)

## Forced Damped Pendulum Motion

The equation governing the motion of a forced damped pendulum is:

$$ \frac{d^2\theta}{dt^2} + b \frac{d\theta}{dt} + \sin\theta = A \cos(\omega t) $$

where:
- $ \theta(t) $ is the angular displacement,
- $ b $ is the damping coefficient,
- $ A $ is the amplitude of the external forcing,
- $ \omega $ is the frequency of the external forcing.

The plot shows the angular displacement $$ \theta(t) $$ over time for given parameters:

- $$ b = 0.2 $$
- $$ A = 1.0 $$
- $$ \omega = 2.0 $$

The oscillations exhibit a transient phase followed by steady-state behavior due to the external forcing.
