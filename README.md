# 🤖 Self-Balancing Robot

A two-wheel **self-balancing robot** based on the **inverted pendulum principle** using a **PID control algorithm**.

---

## 📌 Project Overview

This robot maintains upright balance by continuously measuring tilt angle using an **MPU6050 IMU sensor** and applying a **PID controller** to adjust motor speed in real time.

The system runs a fast control loop to ensure stability and smooth correction.

---

## 🧠 Control Theory

The robot uses:

- **Proportional (P)** – Reacts to current error  
- **Integral (I)** – Corrects accumulated past error  
- **Derivative (D)** – Predicts future error  

### PID Equation

```
Output = Kp * error + Ki * sum(error) + Kd * rate_of_error
```

Where:

```
error = 0° - measured_angle
```

---

## 🔧 Hardware Components

- **Arduino UNO / ESP (mention your controller)**
- **MPU6050 (Gyroscope + Accelerometer)**
- **L298N Motor Driver**
- **2 × 18650 Li-ion Batteries (7.4V nominal)**
- **DC Gear Motors**
- Buck Converter (for regulated 5V supply)

---

## ⚙️ Working Principle

1. IMU measures tilt angle.
2. Current angle is compared to setpoint (0°).
3. PID controller calculates correction.
4. Motor driver adjusts wheel speed.
5. Process repeats continuously (~200–500 Hz).

---

## 🔋 Power Architecture

```
2S Li-ion Battery (7.4V)
        │
        ├── L298N → Motors
        └── Buck Converter → 5V → MCU + IMU
```

---

## ✨ Features

- Complementary filter for angle estimation
- Adjustable PID parameters
- Real-time balancing control
- Modular hardware design
- Rechargeable Li-ion battery system

---

## 📂 Project Structure

```
Self-Balancing-Robot/
│
├── Code/
│   └── self_balancing_robot.ino
│
├── Hardware/
│   └── circuit_diagram.png
│
├── Images/
│   └── robot.jpg
│
└── README.md
```

---

## 🚀 Future Improvements

- Bluetooth / App control
- Kalman filter implementation
- Upgrade to **TB6612FNG motor driver**
- Autonomous navigation

---

## 📸 Project Demonstration

(Add project images or video link here)

---

## 📜 License

This project is open-source under the **MIT License**.

---

### 👨‍💻 Developed by
Your Name
