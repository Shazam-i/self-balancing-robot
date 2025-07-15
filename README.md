 Self-Balancing Two-Wheel Robot

A compact, Arduino-based self-balancing robot using an MPU6050 sensor, motor driver, and PID control. This project demonstrates embedded control systems, sensor fusion, and real-time motor feedback for dynamic stability.

---


---

## 🧠 Features

- Self-balancing using PID control
- Real-time angle estimation using MPU6050 with DMP
- Dual DC motors with L298N or similar driver
- Tunable PID values for better stability
- Forward/backward motion handling

---

## 🧰 Components Used

| Component            | Description                      |
|----------------------|----------------------------------|
| Arduino Uno / Nano   | Microcontroller                  |
| MPU6050              | Gyroscope + Accelerometer        |
| L298N / L9110        | Dual H-Bridge Motor Driver       |
| DC Motors            | With wheels                      |
| Battery Pack         | 7.4V or 11.1V Li-ion/LiPo        |
| Chassis              | Custom or acrylic                |

---

## 🔌 Circuit Diagram

```

MPU6050    -> Arduino
VCC        -> 3.3V
GND        -> GND
SDA        -> A4 (Uno)
SCL        -> A5 (Uno)

Motor Driver -> Arduino
IN1, IN2     -> D4, D5
EN1 (PWM)    -> D6
IN3, IN4     -> D7, D8
EN2 (PWM)    -> D9

````

---

## 🧪 PID Tuning

- Start with all values at `0`
- Gradually increase **Kp** until the robot starts correcting itself
- Add **Kd** to dampen oscillations
- Fine-tune with **Ki** if necessary

```cpp
double Kp = 60;
double Ki = 2.5;
double Kd = 270;
````

---

## 📁 File Structure

```
/Self-Balancing-Robot
│
├── Arduino_Code/
│   └── self_balance.ino
│
├── Images/
│   └── robot_front.jpg
│
├── Videos/
│   └── demo.mp4
│
└── README.md
```

---

## 🚀 How to Run

1. Clone this repo:
   `git clone https://github.com/yourusername/self-balancing-robot.git`

2. Open the `.ino` file in Arduino IDE

3. Install necessary libraries:

   * `Wire.h`
   * `I2Cdevlib` for MPU6050
   * `PID_v1.h`
   * `LMotorController.h` (if used)

4. Upload to your Arduino board

5. Power up and test!

---


---

## 🧑‍💻 Author

Shazam Riaz
BS Computer Engineering Student
📧 Email: [shazamriaz53@gmail.com)

---

## ⭐ Contribute

Pull requests, ideas, and forks are welcome!

---

## 📜 License

This project is licensed under the MIT License.

```

---

Let me know if you want to:

- Add a **GitHub Actions badge**
- Include a more technical **explanation of the control algorithm**
- Write it in **Urdu or bilingual (English + Urdu)**
- Include **Fritzing circuit diagram**

I'll help accordingly.
```

