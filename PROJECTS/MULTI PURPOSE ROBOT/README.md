# Multi-Purpose Robot

## Overview

The **Multi-Purpose Robot** is a versatile robotics platform that integrates multiple control modes and features into a single design. It combines **IR sensor-based line following**, **ultrasonic-based obstacle avoidance**, and **Bluetooth-based voice and gyroscope control** capabilities. This project is built using an **ATmega328P microcontroller**, custom **pulley-based PCB design**, and modular motor control using the **L293D motor driver**.

# Multi Purpose Robot

<div style="display: flex; justify-content: space-between;">
    <img src="https://github.com/karthirilla/karthikrilla.github.io/blob/main/PROJECTS/MULTI%20PURPOSE%20ROBOT/MULTI_PURPOSE_ROBOT_1.jpg" width="30%" />
    <img src="https://github.com/karthirilla/karthikrilla.github.io/blob/main/PROJECTS/MULTI%20PURPOSE%20ROBOT/MULTI_PURPOSE_ROBOT_2.jpg" width="30%" />
    <img src="https://github.com/karthirilla/karthikrilla.github.io/blob/main/PROJECTS/MULTI%20PURPOSE%20ROBOT/MULTI_PURPOSE_ROBOT_3.jpg" width="30%" />
</div>


---

## Key Features

1. **IR Sensor-Based Line Follower**:
   - Uses **LM358 operational amplifier** as a comparator for IR sensor signals.
   - Adjustable sensitivity using a **trim pot** for threshold tuning.

2. **Ultrasonic-Based Obstacle Avoidance**:
   - Detects obstacles using an **ultrasonic distance sensor** and reroutes the robot to avoid collisions.

3. **Bluetooth-Based Voice and Gyroscope Control**:
   - Enables remote control of the robot using:
     - **Voice Commands** (via a mobile app with Bluetooth connectivity).
     - **Gyroscope Movement** for tilt-based direction control.

4. **Motor Driver**:
   - **L293D H-Bridge motor driver** controls the robot's motors for smooth and reliable movement.

5. **Custom Pulley-Based PCB Design**:
   - Compact and modular design to accommodate all components.

6. **Power Supply**:
   - Runs on a **rechargeable battery** to ensure portability and extended use.

7. **Microcontroller**:
   - **ATmega328P** programmed via **Arduino IDE**.

---

## System Components

### 1. **Sensors**
- **IR Sensors** (Line Follower):
   - Detects black and white surfaces for line tracking.
   - Connected to **LM358 op-amp** for signal comparison.

- **Ultrasonic Sensor** (Obstacle Avoidance):
   - Measures distance to detect obstacles in front of the robot.
   - Common module: **HC-SR04**.

### 2. **Motor Driver**
- **L293D H-Bridge**:
   - Drives the motors forward, backward, left, and right.
   - Can handle up to two DC motors simultaneously.

### 3. **Bluetooth Module**
- **HC-05/HC-06** Bluetooth Module:
   - Enables wireless communication for voice and gyroscope-based control.

### 4. **Microcontroller**
- **ATmega328P**:
   - Acts as the central processing unit for sensor data and motor control.
   - Programmed using **Arduino IDE**.

### 5. **Trim Pot**
- Used for threshold adjustments of IR sensors for accurate line following.

### 6. **Power Supply**
- Rechargeable Li-Po or Li-Ion battery for portable and efficient power.

---

## Working Modes

1. **Line Follower Mode**:
   - The robot uses **IR sensors** to detect a line and follows it.
   - The **LM358 op-amp** acts as a comparator to process IR sensor signals.
   - The threshold is adjustable via a **trim pot**.

2. **Obstacle Avoidance Mode**:
   - The **ultrasonic sensor** detects obstacles within a set range.
   - If an obstacle is detected, the robot stops and changes direction to avoid the object.

3. **Bluetooth-Controlled Mode**:
   - The robot connects to a mobile phone or controller via **Bluetooth**.
   - Supported control methods:
     - **Voice Commands**: Move forward, backward, left, right, and stop.
     - **Gyroscope Control**: Tilting the phone controls the robot's movement direction.

---

## Block Diagram

IR Sensors --> LM358 Op-Amp --> ATmega328P --> L293D Motor Driver --> DC Motors Ultrasonic Sensor --> ATmega328P --> Obstacle Avoidance Logic Bluetooth Module --> ATmega328P --> Command Interpretation


---

## Circuit Design

### Key Connections:
1. **IR Sensors**:
   - Output connected to **LM358** op-amp.
   - LM358 output connected to ATmega328P digital pins.

2. **Ultrasonic Sensor**:
   - Trigger and Echo pins connected to ATmega328P.

3. **Bluetooth Module**:
   - TX and RX pins connected to ATmega328P UART pins (e.g., **Pin 0 and Pin 1**).

4. **L293D Motor Driver**:
   - Input pins connected to ATmega328P PWM pins for motor control.
   - Output pins connected to DC motors.

5. **Power Supply**:
   - 5V regulated power supply for the microcontroller and sensors.
   - Motor driver powered directly by the battery.

---

## Components List

| **Component**                | **Quantity** |
|------------------------------|--------------|
| ATmega328P Microcontroller   | 1            |
| IR Sensors                   | 2            |
| LM358 Op-Amp                 | 1            |
| Ultrasonic Sensor (HC-SR04)  | 1            |
| Bluetooth Module (HC-05/06)  | 1            |
| L293D Motor Driver IC        | 1            |
| Trim Potentiometer           | 1            |
| DC Motors                    | 2            |
| Rechargeable Battery         | 1            |
| Custom PCB                   | 1            |
| Resistors, Capacitors        | As needed    |
| Chassis and Wheels           | 1 Set        |

---

## Software Implementation

- **Programming Environment**: **Arduino IDE**.
- **Control Logic**:
   - **Line Following**: Reads IR sensor inputs, processes them through LM358, and adjusts motor speed accordingly.
   - **Obstacle Avoidance**: Continuously measures distance from the ultrasonic sensor. If the distance is below the threshold, the robot stops and reroutes.
   - **Bluetooth Control**: Parses Bluetooth commands to control motor movements.

---

### Sample Code Snippet


#include <AFMotor.h> // Motor Library
#include <SoftwareSerial.h>

SoftwareSerial BT(10, 11); // RX, TX for Bluetooth Module

AF_DCMotor motor1(1);
AF_DCMotor motor2(2);

const int trigPin = 6;
const int echoPin = 7;

void setup() {
  Serial.begin(9600);
  BT.begin(9600);
  pinMode(trigPin, OUTPUT);
  pinMode(echoPin, INPUT);
}

void loop() {
  if (BT.available()) {
    char command = BT.read();
    controlRobot(command);
  }
}

void controlRobot(char cmd) {
  switch (cmd) {
    case 'F': moveForward(); break;
    case 'B': moveBackward(); break;
    case 'L': turnLeft(); break;
    case 'R': turnRight(); break;
    case 'S': stopRobot(); break;
  }
}

void moveForward() {
  motor1.setSpeed(200); motor1.run(FORWARD);
  motor2.setSpeed(200); motor2.run(FORWARD);
}

void moveBackward() {
  motor1.setSpeed(200); motor1.run(BACKWARD);
  motor2.setSpeed(200); motor2.run(BACKWARD);
}

void turnLeft() {
  motor1.setSpeed(200); motor1.run(BACKWARD);
  motor2.setSpeed(200); motor2.run(FORWARD);
}

void turnRight() {
  motor1.setSpeed(200); motor1.run(FORWARD);
  motor2.setSpeed(200); motor2.run(BACKWARD);
}

void stopRobot() {
  motor1.run(RELEASE);
  motor2.run(RELEASE);
}

Advantages
Multi-Functional: Combines multiple control modes in one robot.
Customizable: Threshold adjustments via trim pot for IR sensors.
Remote Control: Bluetooth voice and gyroscope control for added versatility.
Cost-Effective: Built using readily available components.
Tools Used
PCB Design: EasyEDA
Programming: Arduino IDE
Testing and Prototyping: Breadboard setup before final PCB assembly.
Conclusion
The Multi-Purpose Robot is a flexible and compact solution for robotics applications. It combines autonomous line following, obstacle avoidance, and Bluetooth remote control into a single design. This project showcases expertise in analog electronics, motor control, sensor integration, and embedded programming.

Future Enhancements
Add PID control for smoother line following.
Integrate IMU sensors for precise motion tracking.
Implement voice feedback for status updates.
Upgrade to a Li-Po battery for extended runtime.


---

### Key Highlights:
- Multi-functional: **Line following**, **obstacle avoidance**, and **Bluetooth control**.
- Components include **IR sensors**, **ultrasonic sensor**, and **L293D motor driver**.
- Programmed using **Arduino IDE** for the **ATmega328P**.

Let me know if you'd like me to refine any section further! 🚀
