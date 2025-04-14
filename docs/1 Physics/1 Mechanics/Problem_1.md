# Problem 1

## Mechanics

### Investigating the Range as a Function of the Angle of Projection

## 1 Theoretical Foundation:

Projectile motion is a form of motion where an object moves in a bilaterally symmetrical, parabolic path. The path that the object follows is called its trajectory. Projectile motion only occurs when there is one force applied at the beginning on the trajectory, after which the only interference is from gravity.

In physics, projectile motion describes the motion of an object that is launched into the air and moves under the influence of gravity alone, with air resistance neglected. In this idealized model, the object follows a parabolic path determined by its initial velocity and the constant acceleration due to gravity.

## Key Equations to Derive:

1. **Horizontal Motion:**  
   $$ x = v_0 \cos(\theta) t $$  

2. **Vertical Motion:**  
   $$ y = v_0 \sin(\theta) t - \frac{1}{2} g t^2 $$  

3. **Time of Flight:**  
   $$ t = \frac{2 v_0 \sin(\theta)}{g} $$  

4. **Range Formula:**  
   $$ R = \frac{v_0^2 \sin(2\theta)}{g} $$  

5. **Maximum Range Condition:**  
   $$ \theta_{\text{optimum}} = 45^\circ $$  




## 2 Analysis of the Range

### Regular (Periodic) Motion
In a system exhibiting regular motion, the behavior of the system repeats at regular intervals. For example, a simple harmonic oscillator or a damped pendulum with a weak external force may exhibit periodic motion where the oscillations occur at a constant amplitude and frequency. This type of motion can be easily described by a mathematical model and is typically stable and predictable.

Physical Interpretation of Regular Motion:
In energy harvesting systems, periodic motion (such as a resonant vibration) is desirable because it ensures a steady flow of energy.

Mechanical systems like shock absorbers rely on regular oscillations for smooth, controlled motion without excessive damping or instability.

### Chaotic Motion
Chaotic motion occurs when a system's behavior becomes highly sensitive to initial conditions. A small change in the system's starting point can lead to vastly different outcomes over time. This type of motion is non-periodic and unpredictable, even though the underlying system is deterministic (meaning the equations governing the system are known).

In the context of a forced damped pendulum, chaotic motion can emerge when the system is driven by an external force (like a periodic driving force) with the right combination of amplitude and frequency. Initially, the system may exhibit periodic behavior, but as the driving force's amplitude or frequency increases, the system may transition into chaotic behavior.

Physical Interpretation of Chaotic Motion:
Energy Harvesting Devices: In chaotic systems, energy extraction can become inefficient or erratic, making it challenging to design energy harvesters that depend on predictable oscillations. Chaotic behavior might be detrimental to systems that require a constant, regular input or output of energy.

Mechanical Systems and Vibration: In structures like bridges, buildings, or mechanical systems, chaotic motion could represent resonance effects caused by external forces (like wind or traffic), leading to dangerous vibrations. For instance, chaotic behavior could result in structural fatigue, as unpredictable oscillations might cause stress beyond safe levels.

Here are a few steps to visualize this transition:

Regular Motion: For a small driving force amplitude, the pendulum will show periodic motion.

Chaotic Motion: As the driving force amplitude increases, the pendulum will transition to chaotic motion, showing unpredictable oscillations.

![alt text](image-7.png)

The graph illustrates the relationship between the launch angle (°) of a projectile and its horizontal range (m), assuming ideal projectile motion without air resistance.

### Key Observations:
The range increases as the angle increases from 0° to 45°.

The maximum range occurs at 45°, which aligns with theoretical predictions that show the optimal angle for maximum distance in a vacuum is 45°.

As the angle exceeds 45°, the range decreases symmetrically, showing that an angle of 60° produces the same range as 30°, and 70° as 20°.

At 0° and 90°, the range is zero, because:
At 0°, the projectile moves horizontally and immediately touches the ground.

At 90°, the projectile moves straight up and falls back down without horizontal displacement.

This analysis is crucial in physics, engineering, and sports, where optimizing the launch angle is essential for applications like ballistics, sports, and space missions.

## 3 Practical Applications:

### Projectile Trajectory for Different Angles.

Graph plots the trajectory of a projectile for three different angles (30°, 45°, and 60°) to show how the launch angle affects the path.

![alt text](image-10.png)

This graph illustrates the trajectories of a projectile launched at three different angles: 30°, 45°, and 60°.

### Key Observations:

### 1 Peak Height:

The 60° trajectory reaches the highest peak but has a shorter range.
The 45° trajectory has a moderate peak and the longest range.

The 30° trajectory has the lowest peak but still a decent range.

### 2 Horizontal Distance (Range):

The 45° trajectory results in the longest range because, in ideal conditions (without air resistance), the maximum range occurs at 45°.

The 30° and 60° trajectories have the same range, but the 60° path stays in the air longer due to its higher vertical component.

### 3 Effect of Angle on Flight Time:

The projectile launched at 60° stays in the air longer than the one launched at 30° because it has a larger vertical component.

The 30° projectile reaches the ground faster because it has a lower initial vertical velocity.

## Animation 1

![alt text](Untitledvideo-MadewithClipchamp3-ezgif.com-video-to-gif-converter-1.gif)

This animation demonstrates the motion of a projectile under the influence of **linear air drag**, comparing two scenarios:

- **Blue**: No air resistance, \( K = 0 \)
- **Red**: With linear air drag, \( K = 0.2 \)

### Key Concepts

- The motion follows a **parabolic trajectory** in the absence of air drag.
- When linear air drag is introduced, the projectile:
  - Travels **a shorter horizontal distance**
  - Reaches a **lower maximum height**
  - Returns to the ground **sooner**

### Equations of Motion

For projectile motion with **linear air drag** coefficient \( K \), the equations are more complex than the simple case.

Assuming motion starts at the origin with initial velocity \( v_0 \) and angle \( \theta \):

### Without Air Drag (\( K = 0 \)):

- Horizontal motion:
  $$
  x(t) = v_0 \cos(\theta) t
  $$
- Vertical motion:
  $$
  y(t) = v_0 \sin(\theta) t - \frac{1}{2} g t^2
  $$

### With Linear Air Drag (\( K > 0 \)):

- The drag force is proportional to velocity:
  $$
  \vec{F}_\text{drag} = -K \vec{v}
  $$
- The differential equations become:
  $$
  m \frac{d\vec{v}}{dt} = -K \vec{v} + \vec{F}_\text{gravity}
  $$
  which leads to exponential decay in both velocity components.

As a result, the path deviates significantly from the ideal parabolic curve, showing reduced **range** and **height**.

## Visualization

- The **blue trajectory** (\( K = 0 \)) follows a longer, symmetric arc.
- The **red trajectory** (\( K = 0.2 \)) is dampened, demonstrating the real-world effect of air resistance on projectile motion.




## 4 Implementation: Animation 2

<video controls src="videoplayback (1).mp4" title="Title"></video>


## 1. Horizontal Motion (x-axis)  
- The object moves with **constant velocity** since no external force (ignoring air resistance) acts in the horizontal direction.  
- The horizontal displacement is given by:  

  $$ x = v_0 \cos(\theta) \cdot t $$  

## 2. Vertical Motion (y-axis)  
- The object moves under the influence of **gravity**, experiencing **acceleration downward**.  
- The vertical position is given by:  

  $$ y = v_0 \sin(\theta) \cdot t - \frac{1}{2} g t^2 $$  

## 3. Key Equations in Projectile Motion  

- **Time of Flight:**  

  $$ T = \frac{2 v_0 \sin(\theta)}{g} $$  

- **Maximum Height:**  

  $$ H = \frac{v_0^2 \sin^2(\theta)}{2g} $$  

- **Range (Maximum Horizontal Distance):**  

  $$ R = \frac{v_0^2 \sin(2\theta)}{g} $$  

## 4. Understanding the Parabolic Path  
The projectile follows a **parabolic trajectory** because:  
- The **horizontal component** remains constant.  
- The **vertical component** is affected by gravity, making the object accelerate downward.

## 5. Real-World Applications  
Projectile motion is commonly observed in:  
- **Sports** (basketball, football, archery)  
- **Engineering** (missile trajectories, ballistics)  
- **Space Science** (rocket launches, satellite motion)