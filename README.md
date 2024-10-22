# -Smart-Home-Automation

# Smart Home Automation System Using ESP32

This project demonstrates a **Smart Home Automation System** using the **ESP32** microcontroller. It allows users to control home appliances, such as lights and fans, via Wi-Fi. The system can be integrated with a mobile app for remote access and control, making it convenient for users to automate their home environment from anywhere.

## Features

- **Wi-Fi Connectivity**: Control home appliances using the ESP32's Wi-Fi capabilities.
- **Mobile App Integration**: Interface with mobile apps (e.g., Blynk) for remote access and monitoring.
- **Real-Time Control**: Instant control of appliances like lights, fans, and other devices.
- **Scheduling**: Set up timers and schedules for automatic control of devices.
- **Voice Assistant Integration**: Compatible with voice assistants like Amazon Alexa or Google Assistant for voice-controlled automation.
- **Energy Efficiency**: Reduce energy consumption by automating appliances based on time or environmental conditions.

## System Components

### 1. **ESP32 Microcontroller**
   - The core controller for managing inputs (from sensors) and outputs (to relays and appliances).
   - Provides Wi-Fi connectivity to control the system remotely via mobile or web interfaces.

### 2. **Relays**
   - Used to switch on/off high-voltage appliances such as lights and fans.
   - Controlled by the ESP32 to manage the flow of electricity to connected devices.

### 3. **Sensors**
   - **DHT11/DHT22**: Temperature and humidity sensors for climate control.
   - **PIR Sensor**: Detects motion and can automate lighting in response to presence.
   - **Light Sensors**: Adjust lighting based on ambient light levels.
  
### 4. **Mobile App (Blynk or Custom App)**
   - Provides an easy-to-use interface for controlling appliances.
   - Displays real-time sensor data (e.g., temperature, humidity).
   - Allows remote access to control and monitor the system from anywhere in the world.

## Setup Instructions

### Hardware Setup
1. **ESP32 Wiring**:
   - Connect the ESP32's digital pins to the control pins of relays.
   - Relays should be connected to the appliances (e.g., lights, fans).
   - Optionally, connect sensors like DHT11 for temperature and humidity readings.

2. **Relays**:
   - Use a 5V relay module for each appliance you wish to control.
   - Ensure proper wiring to handle the voltage and current of the appliances safely.

3. **Sensors**:
   - Connect the DHT11 sensor to the ESP32 for environmental monitoring.
   - Optionally, connect PIR motion sensors or light sensors to enhance automation.

### Software Setup

1. **Install Arduino IDE**:
   - Download and install the [Arduino IDE](https://www.arduino.cc/en/software) to program the ESP32.

2. **Install ESP32 Board**:
   - Add ESP32 board support to the Arduino IDE by following the [ESP32 installation guide](https://github.com/espressif/arduino-esp32).

3. **Install Required Libraries**:
   - Install the following libraries from the Arduino IDE Library Manager:
     - `Blynk` (for mobile app integration)
     - `DHT Sensor Library` (for temperature and humidity readings)
     - `Adafruit Unified Sensor` (for sensor integration)
  
4. **Blynk Setup**:
   - Create a new project in the Blynk mobile app and select **ESP32** as the device.
   - Add widgets for controlling the appliances (buttons, sliders) and monitoring sensor data.
   - Obtain the **Authentication Token** from the Blynk app and add it to your Arduino code.

5. **Upload Code to ESP32**:
   - Connect your ESP32 to your computer via USB.
   - Upload the provided Arduino code to the ESP32 using the Arduino IDE.
   - Ensure that the Blynk Authentication Token, Wi-Fi credentials, and relay pin numbers are correctly set in the code.

6. **Control and Monitor**:
   - Use the Blynk mobile app to control appliances and monitor real-time sensor data.
   - Set up timers and schedules within the app for automatic control based on time or conditions.

