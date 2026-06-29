# Self-Balancing Robot

## Overview

This project presents the design and implementation of a two-wheeled self-balancing robot capable of maintaining an upright position autonomously. The robot continuously measures its tilt angle using an Inertial Measurement Unit (IMU) and applies a feedback control algorithm to stabilize itself.

The balancing process is achieved through a closed-loop control system where sensor data is processed in real time and the motors are adjusted to counteract any deviation from the vertical position.

---

## Objectives

- Design a two-wheeled self-balancing robot.
- Measure the robot's tilt angle using an IMU.
- Implement real-time feedback control.
- Stabilize the robot using PID control.
- Improve balancing performance through controller tuning.

---

## Working Principle

The robot behaves like an inverted pendulum. Since the center of gravity lies above the wheel axis, the robot becomes unstable whenever it tilts.

The IMU continuously measures the pitch angle of the robot. The controller compares the measured angle with the desired upright position (0°) and computes an error.

The PID controller generates the appropriate motor control signal based on this error. The motors rotate in the required direction to move the wheels beneath the center of gravity, restoring balance.

This process repeats continuously at high speed, allowing the robot to remain balanced.

---

## System Components

- Microcontroller
- IMU Sensor (Accelerometer + Gyroscope)
- DC Geared Motors
- Motor Driver
- Battery Pack
- Chassis
- Wheels

---

## Control Algorithm

The robot uses a Proportional–Integral–Derivative (PID) controller.

The control signal is computed as

\[
u(t)=K_p e(t)+K_i\int e(t)dt+K_d\frac{de(t)}{dt}
\]

where

- \(e(t)\) is the tilt angle error
- \(K_p\) is the proportional gain
- \(K_i\) is the integral gain
- \(K_d\) is the derivative gain

Proper tuning of these gains enables smooth and stable balancing.

---

## Features

- Real-time balancing
- Closed-loop feedback control
- PID-based stabilization
- Continuous IMU angle estimation
- Differential motor control
- Modular hardware design

---

## Applications

- Mobile robotics
- Autonomous platforms
- Control system education
- Embedded systems learning
- Inverted pendulum experiments
- Robotics research

---

## Repository Structure

```
Self-Balancing-Robot/
│
├── Arduino_Code/
├── Hardware/
├── Circuit_Diagram/
├── Images/
├── Videos/
├── Documentation/
└── README.md
```

---

## Future Improvements

- Bluetooth control
- Wi-Fi monitoring
- LQR control
- Kalman Filter implementation
- ROS integration
- Autonomous navigation
- Obstacle avoidance

---

## Conclusion

This project demonstrates the practical implementation of a self-balancing robot using feedback control principles. By combining real-time sensor measurements with PID control, the robot is able to maintain stability and recover from disturbances, making it an excellent platform for studying control systems, embedded programming, and robotics.
