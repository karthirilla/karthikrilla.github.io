# Single Phase Energy Meter

## Overview
The **Single Phase Energy Meter** is designed to monitor current consumption and voltage levels in real time using ESP32. It includes a **prepaid/postpaid energy monitoring system** with safety features like over-voltage, under-voltage, and over-current protection. The device is capable of remote control and automation, making it ideal for home energy management.

---

## Features

1. **Energy Monitoring**  
   - Uses **CT Coil** to monitor current consumption.  
   - Voltage monitoring via **step-down transformer** and voltage divider network.  

2. **Voltage Regulation**  
   - Converts **230V AC** to **12V DC** using a **bridge rectifier**.  
   - **78L05 Voltage Regulator** provides stable **5V DC** for the ESP32 and peripherals.

3. **Display**  
   - **16x2 LCD Display** to show real-time voltage, current, and energy consumption data.

4. **Overcurrent and Overvoltage Protection**  
   - Automatic cutoff using a **relay** during over-voltage or over-current conditions.

5. **Prepaid/Postpaid System**  
   - Supports prepaid energy usage monitoring and postpaid billing.  

6. **Remote Control and Automation**  
   - Allows remote monitoring and control via **Wi-Fi** (ESP32).  

---

## Hardware Components

1. **CT Coil**: Current transformer for current measurement.  
2. **Step-Down Transformer**: Converts **230V AC** to **12V AC**.  
3. **Bridge Rectifier**: Converts **12V AC** to **12V DC**.  
4. **78L05 Voltage Regulator**: Provides regulated **5V DC** supply.  
5. **Voltage Divider Network**: Scales down voltage for monitoring.  
6. **ESP32**: Microcontroller for data processing and control.  
7. **Relay**: Provides cutoff protection for over-voltage or over-current.  
8. **16x2 LCD Display**: Displays voltage, current, and energy data.  
9. **Capacitors**: Used for power supply filtering.

---

## Software Features

- **Energy Monitoring Logic**:  
   Measures voltage and current consumption, calculates power usage.

- **Prepaid/Postpaid System**:  
   - Prepaid mode: Shuts off relay when energy balance runs out.  
   - Postpaid mode: Continuous monitoring with alerts for excessive usage.

- **Protection Logic**:  
   - Cuts power during over-voltage, under-voltage, or over-current scenarios.

- **Remote Monitoring and Control**:  
   - Wi-Fi-based control using the **ESP32** for real-time remote monitoring.

---

## How It Works

1. **Power Conversion**:  
   - The step-down transformer converts 230V AC to 12V AC.  
   - The 12V AC is rectified to DC using the bridge rectifier.  
   - The **78L05 regulator** generates a stable **5V DC** supply.  

2. **Signal Measurement**:  
   - The **CT coil** measures current.  
   - A voltage divider is used to measure the scaled-down voltage.  

3. **Processing Data**:  
   - ESP32 reads the current and voltage signals.  
   - Calculates power consumption, voltage levels, and energy usage.  

4. **Display and Control**:  
   - Energy data is displayed on a **16x2 LCD**.  
   - Relay triggers if over-voltage, under-voltage, or over-current conditions are detected.  

5. **Remote Features**:  
   - Prepaid/Postpaid system enables energy balance management.  
   - Wi-Fi allows real-time remote control of appliances.

---

## Applications

- **Home Energy Management**: Monitor and control energy usage in real time.  
- **Prepaid/Postpaid Billing**: Supports energy billing models.  
- **Overload Protection**: Prevents damage from over-current or over-voltage conditions.  
- **Smart Automation**: Remotely control appliances and protect them automatically.

---

## Development Tools

- **Hardware Design**: EasyEDA.  
- **Microcontroller Programming**: Arduino IDE and Espressif IDE.  

---

## Author

- **Hardware Design**: Designed using EasyEDA.  
- **Software Development**: Arduino IDE and Espressif IDE.  
- **Testing and Assembly**: Complete system testing and integration.

---

## Future Enhancements

- Cloud integration for energy monitoring dashboards.  
- SMS or email notifications for energy usage alerts.  
- Integration of solar power monitoring for hybrid energy systems.  

---

## License

This project is open-source and licensed under the MIT License.

---
