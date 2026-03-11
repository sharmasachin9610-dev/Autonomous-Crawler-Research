# Autonomous Crawler Research
An Arduino-powered crawler designed for precision movement using sensor-based feedback loops.

## 🛠 Features & Sensors
This research focuses on transitioning from simple time-based movement to high-precision autonomous navigation using real-time sensor feedback.

* **Gyroscope (SK-Gyro):** Utilizes a Voltage Oscillation Gyro Module to monitor angular velocity. This allows the crawler to maintain a perfectly straight heading and execute exact 90-degree turns by integrating rotation data.
* **Photo-Interrupters:** Integrated copier sensors (on Pin 11) acting as wheel encoders. These count physical wheel revolutions to calculate exact distance traveled, independent of motor speed fluctuations.
* **Correction Logic:** The system uses a proportional control loop to compare the current gyro heading against the target heading, dynamically adjusting motor PWM values to stay on track.

## 🕹 Logic Commands
The code is structured with modular functions for easy control:
- `moveForward(distance, speed)`: Uses the Photo-Interrupter to measure distance and the Gyro to stay straight.
- `rotateRight(angle)`: Rotates the chassis until the Gyro sensor confirms the target angle is reached.
- `getGyroHeading()`: Performs the math to convert raw voltage into a readable degree of rotation.

## 📂 Project Structure
- `crawler_main.ino`: The main control script containing sensor integration and movement logic.
- `LICENSE`: MIT Open Source license.

