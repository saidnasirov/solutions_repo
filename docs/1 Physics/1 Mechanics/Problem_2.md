# Problem 2

## Investigating the Dynamics of a Forced Damped Pendulum

## 1. Theoretical Foundation: 

### Governing Equation

The motion of a **forced damped pendulum** is governed by the following second-order differential equation:

$$ 
\frac{d^2 \theta}{dt^2} + b \frac{d\theta}{dt} + \frac{g}{L} \sin \theta = A \cos(\omega t) 
$$


For small-angle approximations $$ \theta \approx \sin\theta $$the equation simplifies to:

$$ 
\frac{d^2 \theta}{dt^2} + b \frac{d\theta}{dt} + \frac{g}{L} \theta = A \cos(\omega t) 
$$

This is a **linear non-homogeneous differential equation** that describes **oscillatory motion with damping and external forcing**.

---

### **Example: Solving for Small-Angle Oscillations**



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

---

## 2. Analysis of Dynamics:

### **Investigation of Key Parameters in Forced Damped Pendulum Motion**

### Influence of Damping Coefficient $$ b $$

The damping coefficient affects the system's energy dissipation. The equation of motion is:

$$ 
\frac{d^2 \theta}{dt^2} + b \frac{d\theta}{dt} + \frac{g}{L} \sin \theta = A \cos(\omega t) 
$$

---

## **Transition Between Regular and Chaotic Motion**

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

## Practical Applications:

```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.integrate import solve_ivp
import ipywidgets as widgets
from IPython.display import display

# Define the system parameters
g = 9.8  # Gravity (m/s^2)
L = 1.0  # Length of the pendulum (m)
b_default = 0.2  # Default damping coefficient
A_default = 1.0  # Default forcing amplitude
omega_default = 2.0  # Default driving frequency

# Define the differential equation system
def forced_damped_pendulum(t, y, b, A, omega):
    theta, omega_theta = y  # Unpack angular displacement & velocity
    dtheta_dt = omega_theta
    domega_dt = -b * omega_theta - (g / L) * np.sin(theta) + A * np.cos(omega * t)
    return [dtheta_dt, domega_dt]

# Function to solve and plot the pendulum motion
def plot_pendulum(b, A, omega):
    theta_0 = 0.1  # Initial angle (radians)
    omega_0 = 0.0  # Initial angular velocity

    # Time span for simulation
    t_span = (0, 50)  # 50 seconds
    t_eval = np.linspace(t_span[0], t_span[1], 2000)  # 2000 time points

    # Solve the differential equation
    sol = solve_ivp(forced_damped_pendulum, t_span, [theta_0, omega_0],
                     t_eval=t_eval, args=(b, A, omega), method='RK45')

    # Extract results
    t_values = sol.t
    theta_values = sol.y[0]

    # Plot the results
    plt.figure(figsize=(10, 5))
    plt.plot(t_values, theta_values, label=r'$\theta(t)$', color='b')
    plt.xlabel("Time (s)")
    plt.ylabel("Angular Displacement (radians)")
    plt.title(f"Forced Damped Pendulum Motion (b={b}, A={A}, ω={omega})")
    plt.legend()
    plt.grid()
    plt.show()

# Create interactive sliders
b_slider = widgets.FloatSlider(value=b_default, min=0.0, max=2.0, step=0.05, description='Damping (b)')
A_slider = widgets.FloatSlider(value=A_default, min=0.0, max=5.0, step=0.1, description='Amplitude (A)')
omega_slider = widgets.FloatSlider(value=omega_default, min=0.5, max=5.0, step=0.1, description='Frequency (ω)')

# Display interactive plot
interactive_plot = widgets.interactive(plot_pendulum, b=b_slider, A=A_slider, omega=omega_slider)
display(interactive_plot)

```

![alt text](image.png)

<video controls src="Motion animation using Matlab_ Damped vs underdamped vs critically damped vs overdamped free vib (1).mp4" title="Title"></video>

# Meaning of Terms

## 1. Under-dumped  
- Something that hasn't been discarded or removed enough.  
- **Example (Waste Management):** Not enough waste has been dumped.  
- **Example (Relationships):** Someone hasn't fully "moved on" after a breakup.  

## 2. Undumped  
- Something that hasn't been dumped or discarded at all.  
- **Example (Relationships):** Someone who hasn't been broken up with.  

## 3. Critically Dumbed  
- Likely derived from **"critically dumb"**, meaning extremely foolish.  
- If referring to **"dumbed down"**, it means oversimplified to an extreme level.  
- **Example:** A complex topic explained in a way that removes important details.  

## 4. Over-dumped  
- Something has been discarded or removed too much.  
- **Example (Waste Management):** Excessive material dumped in one place.  
- **Example (Relationships):** Someone who has been broken up with too many times.  


## Forced Damped Pendulum Motion

The equation governing the motion of a forced damped pendulum is:

$$ \frac{d^2\theta}{dt^2} + b \frac{d\theta}{dt} + \sin\theta = A \cos(\omega t) $$


The plot shows the angular displacement over time for given parameters:

- $$ b = 0.2 $$
- $$ A = 1.0 $$
- $$ \omega = 2.0 $$

The oscillations exhibit a transient phase followed by steady-state behavior due to the external forcing.

## Damped Pendulum Motion – Four Scenarios

![alt text](image-1.png)

This simulation shows how a pendulum behaves under different damping conditions. The general equation governing a damped pendulum is:

$$
\frac{d^2\theta}{dt^2} + b\frac{d\theta}{dt} + \frac{g}{L} \sin(\theta) = 0
$$



$$
\begin{aligned}
Where: 
\theta(t) &: \text{Angular displacement (radians)} \\
b &: \text{Damping coefficient} \\
g &= 9.81 \, \text{m/s}^2 \quad \text{(acceleration due to gravity)} \\
L &= 1.0 \, \text{m} \quad \text{(length of the pendulum)}
\end{aligned}
$$

---

## Summary Table

$$
\begin{array}{|c|c|c|}
\hline
\textbf{Damping Type} & \textbf{Condition} & \textbf{Behavior} \\
\hline
\text{Undamped} & b = 0 & \text{Constant amplitude oscillation} \\
\hline
\text{Under-damped} & 0 < b < 2\sqrt{\frac{g}{L}} & \text{Decaying oscillations} \\
\hline
\text{Critically damped} & b = 2\sqrt{\frac{g}{L}} & \text{Fastest non-oscillatory return} \\
\hline
\text{Over-damped} & b > 2\sqrt{\frac{g}{L}} & \text{Slow non-oscillatory return} \\
\hline
\end{array}
$$

---


## Implemention / Bonus:

<video controls src="Animated Poincare section for the damped driven pendulum.mp4" title="Title"></video>