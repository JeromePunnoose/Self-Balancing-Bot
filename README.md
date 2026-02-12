# Self-Balancing-Bot
🤖 Self Balancing Robot
A two-wheel self-balancing robot based on the inverted pendulum principle using PID control.


🔧 Hardware Used
Arduino UNO / ESP32
MPU6050 (Gyro + Accelerometer)
L298N Motor Driver
2 × 18650 Li-ion batteries (7.4V)
DC Gear Motors

⚙️ Features
Complementary filter for angle estimation
PID control for stability
Real-time balancing
Adjustable PID tuning

📐 Working Principle
The robot continuously measures tilt angle using MPU6050 and applies PID control to adjust motor speed and maintain upright balance.

🔋 Power Architecture
2S Li-ion battery powers motors directly.
Buck converter supplies 5V to MCU and sensors.

🎯 Future Improvements
Bluetooth control
Better motor driver (TB6612FNG)
Kalman filter implementation
Autonomous navigation
