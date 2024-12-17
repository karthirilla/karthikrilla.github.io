# ESP32 BLE Mesh Testing System

## Overview
The **ESP32 BLE Mesh Testing System** is designed for testing the BLE Mesh concept with custom input/output configurations. It uses the **ESP32-S3 microcontroller** and integrates a **1.3-inch I2C OLED display** and an **SD card** for data storage. The system supports **BLE Mesh** networking for communication between nodes and implements client-server models, vendor models, and custom data transmission.

![ESP32 BLE Mesh Testing 1](https://github.com/karthirilla/karthikrilla.github.io/blob/main/PROJECTS/ESP32%20BLE%20MESH%20TESTING/ESP32_BLE_MESH_TESTING_1.jpg)
![ESP32 BLE Mesh Testing 2](https://github.com/karthirilla/karthikrilla.github.io/blob/main/PROJECTS/ESP32%20BLE%20MESH%20TESTING/ESP32_BLE_MESH_TESTING_2.jpg)
![ESP32 BLE Mesh Testing 3](https://github.com/karthirilla/karthikrilla.github.io/blob/main/PROJECTS/ESP32%20BLE%20MESH%20TESTING/ESP32_BLE_MESH_TESTING_3.jpg)


---

## Features

1. **BLE Mesh Networking**  
   - Supports **BLE Mesh** networking for communication between nodes.  
   - Implements **client-server models**, **vendor models**, and custom data sending.

2. **Custom I/O Configuration**  
   - 4 input pins and 4 output pins for controlling external devices or sensors.

3. **Display & Data Storage**  
   - **1.3-inch I2C OLED display** for real-time data visualization.  
   - **SD card** module for storing test data for later analysis.

4. **Microcontroller**  
   - **ESP32-S3**: The main microcontroller for handling BLE Mesh communication, I/O, display, and data storage.

5. **Firmware**  
   - Firmware developed using **Espressif IDE** with a focus on BLE Mesh implementation.

---

## Hardware Components

1. **ESP32-S3 Microcontroller**  
   - Handles BLE Mesh communication, I/O operations, display control, and data storage.

2. **1.3-inch I2C OLED Display**  
   - Used for displaying real-time information, such as node status and BLE Mesh connectivity.

3. **SD Card Module**  
   - Stores data such as received messages or other metrics for later retrieval and analysis.

4. **4 Input Pins**  
   - Configurable for digital or analog inputs to control or monitor external devices.

5. **4 Output Pins**  
   - Used to control actuators or other external components.

6. **BLE Mesh**  
   - Implements the BLE Mesh protocol to allow communication between multiple nodes.

---

## Software Features

- **BLE Mesh Communication**:  
   - Supports **client-server models**, **vendor models**, and custom data transmission.  
   - Allows nodes to send and receive data in a mesh network.

- **Data Storage**:  
   - Logs and stores data from BLE Mesh communication on the **SD card**.

- **Real-Time Display**:  
   - Displays the current status of BLE Mesh communication on the **OLED display**.

- **Input/Output Control**:  
   - Configurable inputs for sensing and outputs for controlling external devices.

- **Development Environment**:  
   - Firmware developed using **Espressif IDE** with ESP32 SDK.  
   - Uses **BLE Mesh library** and other components from the ESP32 ecosystem.

---

## Workflow

1. **Initialization**:  
   - The **ESP32-S3** initializes the **BLE Mesh network** and connects to other nodes.

2. **Data Transmission**:  
   - **Client nodes** send data, and **server nodes** receive it.  
   - Vendor models and custom data can be sent as per the project requirements.

3. **Real-Time Monitoring**:  
   - The **OLED display** shows the current network status, including node connections and data being sent/received.

4. **Data Storage**:  
   - All relevant data is stored on the **SD card** for later analysis.

5. **Input/Output Operations**:  
   - Inputs are read, and outputs are controlled based on the BLE Mesh data or external interactions.

---

## Applications

- **Testing BLE Mesh**:  
   - Used for testing BLE Mesh networks in different configurations (client-server, vendor models, custom data).

- **Remote Control Systems**:  
   - Can be used in applications that require remote control over a BLE Mesh network.

- **Data Logging**:  
   - Stores data from BLE Mesh communication for future analysis or troubleshooting.

- **Real-Time Monitoring**:  
   - Visualizes data on an OLED display for quick diagnostics.

---

## Hardware Design

- **Custom PCB Design**:  
   - The hardware was designed with a focus on BLE Mesh communication, real-time monitoring, and flexible I/O control.  
   - Components were selected to ensure efficient data transfer and storage.

---

## Software Tools

- **Espressif IDE**: Development environment for ESP32, used to develop the firmware.  
- **ESP32 SDK**: Includes libraries for BLE Mesh communication and I/O management.

---

## Future Enhancements

- **Wireless Data Sync**:  
   - Implement features to sync data across a cloud platform for remote monitoring.

- **Mesh Network Expansion**:  
   - Add support for more nodes in the BLE Mesh network for wider coverage.

- **Mobile App Integration**:  
   - Develop a mobile application to control and monitor the BLE Mesh network remotely.

- **Advanced Data Logging**:  
   - Implement more advanced logging features like time-stamped logs or periodic data dumps.

---

## License

This project is open-source and licensed under the **MIT License**.

---

## Author

- **Hardware Design**: Developed using EasyEDA for the custom PCB design.  
- **Software Development**: Arduino IDE and Espressif IDE for the ESP32 firmware.  
- **Testing and Validation**: Performed to ensure BLE Mesh functionality and reliable data storage.

---

