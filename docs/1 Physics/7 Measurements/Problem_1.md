# Problem 1

# Measuring Earth's Gravitational Acceleration with a Pendulum

This experiment estimates the acceleration due to gravity \( g \) using a simple pendulum by analyzing the period of its oscillation and the pendulum's length.

---

## Materials

- String (1 or 1.5 meters)
- Small mass (e.g., key chain, bag of coins)
- Stopwatch (or phone timer)
- Ruler or measuring tape

---

## Setup

- Attach the weight to one end of the string and fix the other end securely.
- Measure the length \( L \) from the suspension point to the center of the weight.
- Estimate the uncertainty in length measurement:

$$
\Delta L = \frac{\text{Ruler Resolution}}{2}
$$

---

## Data Collection

1. Displace the pendulum slightly (less than 15°) and release.
2. Measure the time for 10 full oscillations, \( T_{10} \), and repeat 10 times.
3. Calculate the average time:

$$
\overline{T_{10}} = \frac{1}{10} \sum_{i=1}^{10} T_{10,i}
$$

4. Determine the standard deviation \( \sigma_T \), then compute:

$$
\Delta T_{10} = \frac{\sigma_T}{\sqrt{n}} \quad \text{where } n = 10
$$

5. The period of one oscillation is:

$$
T = \frac{\overline{T_{10}}}{10}, \quad \Delta T = \frac{\Delta T_{10}}{10}
$$

---

## Calculations

### 1. Calculate \( g \)

Using the pendulum formula:

$$
g = \frac{4\pi^2 L}{T^2}
$$

### 2. Propagate Uncertainty

Apply uncertainty propagation for functions involving multiplication and powers:

$$
\Delta g = g \cdot \sqrt{ \left( \frac{\Delta L}{L} \right)^2 + \left( 2 \cdot \frac{\Delta T}{T} \right)^2 }
$$

---

## Analysis

1. Compare your measured value of \( g \) with the standard value:

$$
g_{\text{standard}} = 9.81 \, \text{m/s}^2
$$

2. Discuss the following points:
- The effect of measurement resolution on \( \Delta L \)
- Variability in timing and its impact on \( \Delta T \)
- Assumptions and possible sources of experimental error (e.g., angle of displacement, air resistance, human reaction time)

---

## Conclusion

A simple pendulum is an effective tool for estimating gravitational acceleration. Accuracy depends on precise measurements of time and length, and proper treatment of uncertainties provides insight into the reliability of the result.

![alt text](ScreenRecording2025-05-24095705-ezgif.com-video-to-gif-converter.gif)

![alt text](ScreenRecording2025-05-22151607-ezgif.com-video-to-gif-converter.gif)

![alt text](image.png)

![alt text](image-1.png)

![alt text](image-2.png)

## Measuring Gravitational Acceleration with a Pendulum

The experiment visualized above illustrates the process of measuring Earth's gravitational acceleration \( g \) using a simple pendulum.

### Left Panel: Pendulum Swing Simulation

The left side of the figure shows a simulation of a pendulum swinging under the influence of gravity. The pendulum consists of:
- A mass (bob) attached to a string of length \( L \),
- Swinging with an initial angle \( \theta_0 \) (assumed to be small).

Using the small angle approximation, the period of oscillation \( T \) is given by:

$$
T = 2\pi \sqrt{\frac{L}{g}}
$$

Solving for \( g \), we get:

$$
g = \frac{4\pi^2 L}{T^2}
$$

By measuring the period \( T \) and the pendulum length \( L \), we can experimentally determine the value of \( g \).

### Right Panel: Measured \( g \) vs Length

The right side of the figure plots the measured gravitational acceleration values for different pendulum lengths. The data demonstrates that:
- For each length, the period is measured multiple times and used to calculate \( g \).
- The measured values cluster around \( 9.8 \, \text{m/s}^2 \), which is close to the standard gravitational acceleration at Earth's surface.

### Observations:

- Slight deviations are visible, possibly due to human error in timing, measurement of length, or assuming small-angle approximation for larger amplitudes.
- The plot validates that even simple tools like a stopwatch and ruler can yield accurate physical constants through careful measurement and analysis.

This experiment highlights the importance of uncertainty quantification and repeated measurements in experimental physics.



![alt text](Untitledvideo-MadewithClipchamp8-ezgif.com-video-to-gif-converter.gif)


![alt text](ScreenRecording2025-05-24100306-ezgif.com-video-to-gif-converter.gif)