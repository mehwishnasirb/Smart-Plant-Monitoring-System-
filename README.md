# 🌱 Smart Plant Monitoring System (IoT-Based)

This project is a real-time **Smart Plant Monitoring System** built using **ESP32 microcontrollers**, **MicroPython**, and a **Flask-based server**. It automates plant care by monitoring environmental parameters and controlling actuators like fans, pumps, and heaters.

---

## 🧠 Overview

The system collects data from multiple sensors (gas, humidity, temperature, rain, water level, and soil moisture) and sends it to a Flask server over Wi-Fi. Based on predefined thresholds, the system takes automatic actions to maintain an ideal environment for plant growth.

---

## ⚙️ Components

### 🔍 Sensors
- **MQ-2 Gas Sensor** – Detects smoke, propane, methane, and combustible gases.
- **MQ-135 Gas Sensor** – Measures air quality (CO₂, ammonia, benzene).
- **DHT11** – Temperature and humidity monitoring.
- **Soil Moisture Sensor** – Detects soil dryness for irrigation.
- **Water Level Sensor** – Monitors tank water levels.
- **YL-83 Rain Sensor** – Detects rainfall to prevent overwatering.

### 🔧 Actuators
- **Air Circulation Fan (5V)** – Activates on high humidity or gas levels.
- **Exhaust Fan** – Expels harmful gases from the environment.
- **Water Pump (5V)** – Waters the plant when the soil is dry and no rain is detected.
- **Heater (12V)** – Turns on if the temperature drops.
- **Relay Modules** – Used for controlling high-power devices.
- **LCD Display** – Shows real-time sensor values and system status.
- **Buzzer** – Alerts users about critical conditions.
- **MOSFET Motor Driver** – Controls the speed of fans and pumps using PWM.

---

## 🔄 Working Mechanism

### 1. 📡 Data Collection
- ESP32 collects environmental data in real-time.
- Sensors read temperature, humidity, air quality, soil moisture, and rain detection.

### 2. 🌐 Communication
- Data is sent to the **Flask server** over Wi-Fi.
- The server analyzes conditions and makes decisions based on thresholds.

### 3. ⚡ Action Execution
- Turns ON/OFF actuators based on logic:
  - Gas leak → Exhaust fan + buzzer.
  - Low temperature → Heater ON.
  - Dry soil + no rain → Water pump ON.
  - High humidity → Air circulation fan ON.
  - Low water level → Buzzer alert.

### 4. 🖥️ User Interface
- **LCD** displays system status.
- **Flask** provides a web interface (monitor/control remotely).

---

## 🛠️ Technologies Used

| Tool/Tech            | Purpose                                |
|----------------------|----------------------------------------|
| **ESP32-WROOM**      | Main microcontroller (IoT brain)       |
| **MicroPython**      | Code for ESP32                         |
| **Python + Flask**   | Server-side control logic              |
| **Thonny IDE**       | MicroPython development                |
| **Wi-Fi**            | ESP32 to Flask communication           |

---

## 🏁 Conclusion

This system provides a scalable, cost-effective, and real-time solution to plant care using IoT. It automates watering, air circulation, heating, and alerting, making it ideal for indoor gardening, greenhouse automation, or precision agriculture.

---

## 🔮 Future Enhancements

- Add mobile notifications via SMS/email.
- Integrate with cloud platforms (Firebase, ThingSpeak).
- Add camera and plant disease detection.
- Create a mobile app for better control and UI.


