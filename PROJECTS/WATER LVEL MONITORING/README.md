# Water Level Monitoring System

## Overview
The **Water Level Monitoring System** is an industrial-grade solution for accurately monitoring water levels using a **4-20mA sensor**. The system processes sensor data, displays the water level, and provides motor control, buzzer alerts, and cutoff features. The system is powered by an **STM32F103** microcontroller and uses a **high-precision ADC** for accurate measurements.

---

## Features

1. **Water Level Measurement**  
   - Uses **4-20mA industrial sensor** to detect water levels based on pressure.  
   - Converts current (4-20mA) to voltage for microcontroller input.

2. **High-Precision ADC**  
   - **ADS1115**: I2C-based 24-bit ADC module for accurate voltage readings.  
   - Buffer amplifier ensures signal stability and precision.

3. **Display**  
   - **TM1638 7-Segment Display Module** to display water level, timer, and cutoff status.

4. **Control Outputs**  
   - **Relay** for motor control based on water level thresholds.  
   - **Buzzer** for audio indication and alerts.

5. **Wide Power Supply Support**  
   - Supports a wide input voltage range for industrial environments.

6. **Cutoff Features**  
   - Motor control logic for automatic cutoff when water levels reach predefined limits.  

---

## Hardware Components

1. **4-20mA Water Level Sensor**: Industrial-grade sensor for water level measurement.  
2. **Current-to-Voltage Conversion**: Converts 4-20mA signal to voltage for microcontroller compatibility.  
3. **Buffer Amplifier**: Ensures accurate and stable signal readings.  
4. **ADS1115**: I2C-based 24-bit ADC for precise analog-to-digital conversion.  
5. **STM32F103**: Microcontroller for processing and control.  
6. **TM1638 7-Segment Display**: Displays water level, timer, and status.  
7. **Relay**: Controls motor operation based on water level.  
8. **Buzzer**: Audio indicator for alerts.  
9. **Power Supply**: Supports a wide input voltage range.

---

## Software Features

- **Water Level Measurement**:  
   Reads the 4-20mA signal, converts it to voltage, and calculates the water level.

- **High-Precision ADC Integration**:  
   The **ADS1115** ADC reads voltage data with 24-bit accuracy over I2C communication.

- **Motor Control Logic**:  
   - Relay triggers to control water pumps when water level reaches thresholds.  
   - Automatic cutoff features to avoid overflow or dry run.

- **Display**:  
   - TM1638 7-Segment Display shows:  
      - Real-time water level.  
      - Timer status.  
      - Motor cutoff status.

- **Alerts and Indications**:  
   - **Buzzer** sounds alerts for critical water levels or faults.  

- **Programming Environment**:  
   - **STM32CubeIDE** for development.  
   - **STM32CubeMX** for hardware configuration.

---

## How It Works

1. **Water Level Detection**:  
   - The 4-20mA sensor generates a current signal proportional to the water level.  
   - Current is converted to voltage for microcontroller compatibility.

2. **Signal Amplification and Conversion**:  
   - The buffer amplifier stabilizes the converted signal.  
   - The **ADS1115** ADC module reads the voltage with high precision and sends it to the STM32 over I2C.

3. **Data Processing**:  
   - The STM32 microcontroller calculates the water level based on ADC data.  
   - It processes motor control logic and triggers relays or alerts.

4. **Display and Alerts**:  
   - Water levels, timer, and cutoff statuses are displayed on the TM1638 module.  
   - A buzzer indicates water level thresholds or errors.

5. **Motor Control**:  
   - The relay controls the water pump based on water level thresholds.  
   - Automatic cutoff ensures motor protection.

---

## Applications

- **Water Tank Monitoring**: Industrial and domestic water level management.  
- **Automatic Pump Control**: Automatically start and stop water pumps.  
- **Industrial Water Systems**: Monitor and control water systems with 4-20mA sensors.  
- **Overfill/Dry Run Protection**: Prevent damage to pumps and water systems.

---

## Development Tools

- **Hardware Design**: EasyEDA for circuit and PCB design.  
- **Microcontroller Programming**: STM32CubeIDE and STM32CubeMX.  

---

## Author

- **Hardware Design**: Designed and tested using EasyEDA.  
- **Software Development**: STM32CubeIDE and STM32CubeMX.  
- **Testing and Assembly**: Complete hardware integration and functional testing.

---

## Future Enhancements

- **IoT Integration**: Connect to cloud platforms for remote water level monitoring.  
- **Wireless Alerts**: SMS or app notifications for critical water levels.  
- **Data Logging**: Store water level data for long-term analysis.  

---

## License

This project is open-source and licensed under the MIT License.

---
