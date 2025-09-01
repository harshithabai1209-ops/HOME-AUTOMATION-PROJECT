# HOME-AUTOMATION-PROJECT

🏠 IoT-Based Home Automation System
📌 Overview

This project is a Wi-Fi-enabled smart home automation system built using ESP32/ESP8266, IoT protocols, and a custom PCB designed in KiCad.
It allows users to control home appliances (lights, fans, etc.) remotely through a mobile/web dashboard and integrates sensors (temperature, motion, gas, light) for intelligent automation.

🚀 Features

Remote control of AC appliances (fan, light, etc.)

Wi-Fi-based communication (ESP32/ESP8266)

Cloud / MQTT / Blynk / Local server support

Real-time sensor data monitoring

Relay driver circuit with isolation for AC safety

Custom PCB designed in KiCad with proper AC/DC isolation

🛠️ Hardware Components

ESP32 / ESP8266 NodeMCU – Wi-Fi microcontroller

Relay Module (5V/3.3V) – Switching AC loads

DHT11/DHT22 – Temperature & Humidity sensor

PIR Sensor – Motion detection

LDR – Light sensing

MQ-2 Gas Sensor – Safety monitoring

Power Supply – 5V regulated (AMS1117 or buck converter)

Optocoupler & Fuse – Protection for relay section

📐 PCB Design (KiCad)

Designed using KiCad EDA

Separate AC and DC sections for safety

Minimum 3–6 mm isolation gap between high-voltage and low-voltage traces

Solid ground planes for noise reduction

Gerber files generated for PCB manufacturing

⚙️ Software / Firmware

Developed using Arduino IDE / ESP-IDF

Supports:

MQTT (Mosquitto / Cloud broker)

Blynk / ThingsBoard / Custom Web UI

Example firmware features:

Control appliances via mobile app

Read sensor values & push to dashboard

Automation rules (e.g., auto fan ON if temperature > 30°C)

🔌 Circuit Block Diagram
        +-------------------+       +-------------+
        |   ESP32/ESP8266   |------>|  Relay Unit |----> AC Load (Fan/Light)
        +-------------------+       +-------------+
                 |                          |
            +----------+              +----------+
            |  Sensors |              |  Power   |
            +----------+              +----------+

📂 Project Structure
Home-Automation-IoT/
│── hardware/
│   ├── schematics/        # KiCad schematic files
│   ├── pcb-layout/        # PCB design files
│   └── gerbers/           # Manufacturing files
│
│── firmware/
│   ├── main.ino           # Arduino code
│   └── config.h           # Wi-Fi, MQTT, API keys
│
│── docs/
│   ├── README.md          # Project documentation
│   └── images/            # Circuit & PCB renders

🧩 Applications

Smart home & IoT automation

Energy-efficient lighting & appliances

Remote healthcare monitoring (with sensors)

Industrial automation (extended use case)

⚠️ Safety Note

⚡ Caution: This project involves AC mains (230V/110V). Handle with extreme care.
Use proper isolation, fuses, and enclosures while testing.

📖 Future Enhancements

Voice assistant integration (Alexa, Google Assistant)

Mobile app with Flutter/React Native

AI-based predictive automation

Integration with solar energy systems

✨ Made with ❤️ using Embedded Systems + IoT + KiCad
