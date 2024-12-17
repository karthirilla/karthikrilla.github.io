# 3 Phase Energy Meter Testing System

## Overview
The **3 Phase Energy Meter Testing System** is a custom-built solution to test and validate the performance of 3-phase energy meters. The system uses specialized energy measurement ICs to measure critical electrical parameters, including current, voltage, power factor, and phase angle. An **ESP32 microcontroller** acts as the central processing unit with isolation to prevent interference.
# Three Phase Energy Meter Testing

## Images

### First Grid (Images 1, 2, and 3)
![Three Phase Energy Meter Test 1](https://github.com/karthirilla/karthikrilla.github.io/blob/main/PROJECTS/THREE%20PHASE%20ENERGY%20METER%20TESTING/THREE_PHASE_ENERGY_METER_TEST_1.jpg)
![Three Phase Energy Meter Test 2](https://github.com/karthirilla/karthikrilla.github.io/blob/main/PROJECTS/THREE%20PHASE%20ENERGY%20METER%20TESTING/THREE_PHASE_ENERGY_METER_TEST_2.jpg)
![Three Phase Energy Meter Test 3](https://github.com/karthirilla/karthikrilla.github.io/blob/main/PROJECTS/THREE%20PHASE%20ENERGY%20METER%20TESTING/THREE_PHASE_ENERGY_METER_TEST_3.jpg)

### Second Grid (Images 4, 5, and 6)
![Three Phase Energy Meter Test 4](https://github.com/karthirilla/karthikrilla.github.io/blob/main/PROJECTS/THREE%20PHASE%20ENERGY%20METER%20TESTING/THREE_PHASE_ENERGY_METER_TEST_4.jpg)
![Three Phase Energy Meter Test 5](https://github.com/karthirilla/karthikrilla.github.io/blob/main/PROJECTS/THREE%20PHASE%20ENERGY%20METER%20TESTING/THREE_PHASE_ENERGY_METER_TEST_5.jpg)
![Three Phase Energy Meter Test 6](https://github.com/karthirilla/karthikrilla.github.io/blob/main/PROJECTS/THREE%20PHASE%20ENERGY%20METER%20TESTING/THREE_PHASE_ENERGY_METER_TEST_6.jpg)

### Separate Image (Image 7)
![Three Phase Energy Meter Test 7](https://github.com/karthirilla/karthikrilla.github.io/blob/main/PROJECTS/THREE%20PHASE%20ENERGY%20METER%20TESTING/THREE_PHASE_ENERGY_METER_TEST_7.jpg)

---

## Features

1. **3-Phase Energy Measurement**  
   - Measures **current**, **voltage**, **power factor**, and **phase angle**.  
   - Supports 3-phase power supply systems.

2. **Energy Monitoring ICs**  
   - **ADE7758**: Analog Devices' 3-phase energy measurement IC.  
   - **ATM90E36A**: Advanced metering IC for power measurement and monitoring.

3. **Isolated Communication**  
   - **Isolated I2C and SPI converters** are used to ensure safe and interference-free communication between measurement ICs and the ESP32 microcontroller.

4. **Custom PCB**  
   - Designed a custom PCB for 3-phase system testing and measurement.  
   - Isolated design to protect the ESP32 from high voltages.

5. **Power Supply**  
   - Isolated 3-phase power supply ensures stable and safe operation.

---

## Hardware Components

1. **ADE7758**:  
   - IC for 3-phase energy measurement.  
   - Measures voltage, current, active/reactive power, and energy.

2. **ATM90E36A**:  
   - High-precision IC for 3-phase metering applications.  
   - Provides accurate current, voltage, and power factor readings.

3. **Isolated I2C/SPI Converters**:  
   - Prevents interference and protects the microcontroller.

4. **ESP32 Microcontroller**:  
   - Central unit for processing measured data.  
   - Handles communication with the energy ICs and displays results.

5. **Custom PCB Design**:  
   - PCB designed using **EasyEDA** for testing purposes.  
   - Ensures proper isolation and robust hardware layout.

6. **3-Phase Power Supply**:  
   - Isolated power supply system for safe operation and testing.

---

## Software Features

- **Measurement Capabilities**:  
   - Reads voltage, current, power factor, phase angle, and other electrical parameters.  

- **IC Integration**:  
   - Communicates with **ADE7758** and **ATM90E36A** using isolated SPI/I2C protocols.

- **Microcontroller Processing**:  
   - Processes measured data using the ESP32 microcontroller.  

- **Display and Output**:  
   - Displays the measured parameters (current, voltage, power factor, phase angle) on a connected interface.

- **Isolation Logic**:  
   - Ensures safe operation and prevents electrical noise interference.

- **Development Environment**:  
   - Software developed using **Arduino IDE** and **Espressif IDE**.

---

## Workflow

1. **Sensor Measurement**:  
   - **ADE7758** and **ATM90E36A** measure voltage, current, power factor, and phase angle from the 3-phase input.  

2. **Isolated Communication**:  
   - Data is sent to the ESP32 microcontroller via isolated I2C and SPI communication.

3. **Data Processing**:  
   - The ESP32 processes the data and calculates the required electrical parameters.

4. **Display and Testing**:  
   - Outputs the measured values for testing and validation of 3-phase energy meters.

5. **Isolation Safety**:  
   - Isolated power supply and communication ensure safe testing and operation.

---

## Applications

- **Energy Meter Testing**: Testing and validation of 3-phase energy meters.  
- **Power System Monitoring**: Measuring voltage, current, and power factor for 3-phase systems.  
- **Electrical Labs**: Used for research, testing, and educational purposes.  

---

## Hardware Design

- **Custom PCB**: Designed using **EasyEDA**.  
- **Components**:  
   - ADE7758 and ATM90E36A ICs.  
   - ESP32 microcontroller.  
   - Isolated SPI/I2C modules.  
   - 3-phase isolated power supply system.  

---

## Software Tools

- **Arduino IDE**: Development and programming for the ESP32.  
- **Espressif IDE**: For advanced firmware development.  

---

## Future Enhancements

- **Wireless Integration**: Add WiFi/BLE features for remote data monitoring.  
- **Cloud Storage**: Send measured data to the cloud for further analysis.  
- **Display Interface**: Integrate an LCD/LED display for real-time parameter monitoring.  
- **Mobile App Support**: Develop an app to monitor 3-phase energy data wirelessly.

---

## License

This project is open-source and licensed under the **MIT License**.

---

## Author

- **Hardware Design**: Developed using EasyEDA.  
- **Software Development**: Arduino IDE and Espressif IDE.  
- **Testing and Validation**: Conducted in a controlled environment for accuracy.

---

