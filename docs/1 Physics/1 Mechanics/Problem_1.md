# Problem 1

# Mechanics

# Task 1
# Theoretical Foundation:

Begin by deriving the governing equations of motion from fundamental principles. This involves solving a basic differential equation to establish the general form of the motion.

Highlight how variations in initial conditions lead to a family of solutions.

## Solution
Define the Forces Acting on the Projectile
A projectile is subject to only one force (neglecting air resistance):

Gravitational force acting downward:

$$
F=mg
$$

$$
24=m6
$$

$$
m=24/6
$$

$$
m=4
$$

$$
24=4*6
$$

## Phyton Code Solution


# Analysis of the Range:
Investigate how the horizontal range depends on the angle of projection.

Discuss how changes in other parameters, such as initial velocity and gravitational acceleration, influence the relationship.

## Explanation
The horizontal range of a projectile depends on the projection angle in a predictable way, governed by the equation:

![alt text](<Screenshot 2025-03-13 092850.png>)

1. Sinusoidal Relationship:

The range is proportional to sin(2θ), which means it varies in a sinusoidal pattern with the angle.

Sin(2θ) reaches its maximum value of 1 when 2θ = 90°, or θ = 45°

At 45°, the projectile travels the farthest.

As 𝜃 increases beyond 45°, sin(2𝜃) decreases, causing the range to shorten.

2. Symmetry
The range for angles that add up to 90° is the same. For example:

R(30°) = R(60°)

R(10°) = R(80°)

This is because sin(20) = sin(180° - 2θ)

![alt text](image.png)

Here’s the graph showing the horizontal range as a function of the projection angle! You can see the symmetric curve peaking at 45°, with key points marked at 30°, 45°, and 60° to highlight the symmetry.


## Example

$$
R=(20)^2sin(2*45°) / 9.8
$$

$$
R=400 * sin(90°) / 9.8
$$

$$
R=400 * 1 / 9.8
$$

$$
R≈40.82
$$
The projectile travels about 40.82 meters.

![alt text](image-1.png)

