
# IoT-Based Autonomous Precision Irrigation System
<p align="center">

<img src="https://img.shields.io/badge/💡_INNOVATION-6C63FF?style=for-the-badge"/>
<img src="https://img.shields.io/badge/🏆_HACKSAGON_2026-4A4A4A?style=for-the-badge"/>
<img src="https://img.shields.io/badge/🥇_TOP_PERFORMERS-FFD700?style=for-the-badge&logoColor=black"/>
<img src="https://img.shields.io/badge/🌐_IOT-555555?style=for-the-badge"/>
<img src="https://img.shields.io/badge/⚡_ELECTRONICS-1565C0?style=for-the-badge"/>
<img src="https://img.shields.io/badge/🔧_EMBEDDED_SYSTEMS-00897B?style=for-the-badge"/>
<img src="https://img.shields.io/badge/ESP32-00ACC1?style=for-the-badge"/>
<img src="https://img.shields.io/badge/🔥_FIREBASE-616161?style=for-the-badge&logo=firebase&logoColor=FFCA28"/>
<img src="https://img.shields.io/badge/⚡_REALTIME-FF3D00?style=for-the-badge"/>
<img src="https://img.shields.io/badge/🤖_ML-5E35B1?style=for-the-badge"/>
<img src="https://img.shields.io/badge/⚙️_POWERED-4285F4?style=for-the-badge"/>
<img src="https://img.shields.io/badge/🌐_HTML-E34F26?style=for-the-badge&logo=html5&logoColor=white"/>
<img src="https://img.shields.io/badge/🎨_CSS-1572B6?style=for-the-badge&logo=css3&logoColor=white"/>
<img src="https://img.shields.io/badge/✨_JAVASCRIPT-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"/>
<img src="https://img.shields.io/badge/🛠️_BACKEND-37474F?style=for-the-badge"/>
<img src="https://img.shields.io/badge/💻_HARDWARE+SOFTWARE-2E7D32?style=for-the-badge"/>
<img src="https://img.shields.io/badge/🤖_AUTOMATION-8E24AA?style=for-the-badge"/>
<img src="https://img.shields.io/badge/🏅_HACKATHON_ACHIEVEMENT-C62828?style=for-the-badge"/>
<img src="https://img.shields.io/badge/🌱_IRRIGO-43A047?style=for-the-badge"/>
<img src="https://img.shields.io/badge/📡_SENSORS-00838F?style=for-the-badge"/>

</p>
## 🎯 Problem Statement
Agricultural water management faces two critical challenges: **over-irrigation** leading to water waste and root diseases, and **under-irrigation** causing crop stress and reduced yield. Traditional irrigation methods lack the precision to address the micro-variability of soil conditions across different zones of a farm.

## 💡 Our Solution
A fully autonomous IoT-based smart irrigation system that divides farmland into micro-zones and deploys a custom-built four-wheeled robotic rover to collect precise soil health data *in-situ*. The system automatically triggers zone-specific sprinkler irrigation only when and where it is needed, optimizing water usage to the exact requirements of the specific crop being grown.

The project integrates three core subsystems working in harmony:

1.  **🤖 Autonomous Soil Sampling Rover**: A custom 4WD robot with a rack-and-pinion sensor deployment mechanism.
2.  **🖥️ Intelligent Web Dashboard**: A real-time monitoring interface with ML-driven irrigation logic.
3.  **🚿 Automatic Valve Actuation System**: A network of solenoid valves controlled wirelessly for granular irrigation.

####
![Project Images](https://res.cloudinary.com/dfll8qs0d/image/upload/v1783240902/project_images_gl9zah.png)

## 🏆 Hackathon Achievement
### Hacksagon 2026
**Top Performers Certificate** 

*Agriculture Track | Hardware & Software Domain*

Our team's innovative integration of robotics, embedded systems, and machine learning for tangible agricultural impact was recognized among the top projects in the hackathon.

## 🔧 System Architecture & Workflow

The platform operates as a closed-loop automated system divided into three primary components:

### 1. Autonomous Bot
* **Mobility:** Built on a robust 4-wheeled chassis capable of navigating uneven farm terrain.
* **Mechanism:** Equipped with a custom-engineered **rack and pinion mechanical actuator** driven by a high-torque motor to mechanically insert and extract a heavy-duty probe into the ground safely.
* **Sensing:** Integrates an industrial-grade **7-in-1 Soil NPK Sensor** that gathers:
  * Nitrogen (N), Phosphorus (P), Potassium (K) levels
  * Soil Moisture content
  * Temperature
  * Electrical Conductivity (EC)
  * pH levels
* **Core Processing:** Powered by an **ESP32 Microcontroller** which samples the sensor values via RS485/Modbus protocol and transmits the geo-tagged zone metrics directly to the cloud.

### 2. Live Analytics Dashboard
* **Backend Pipeline:** Written in Python/Node, hosting a specialized **Machine Learning Model**. The model intakes the specific crop type cultivated in a zone alongside historic environmental variables to output dynamic, highly optimized **soil moisture thresholds**.
* **Frontend UI:** A responsive, real-time web interface mapping data node-by-node. Farmers can remotely monitor live chemical/moisture levels per zone without manual field testing.
* **Decision Core:** The backend constantly cross-references the live sensor data stored in Firebase against the dynamic ML threshold markers.

### 3. Smart Valve Network
* **Actuation:** Distributed physical automated valves coupled with localized sprinkler arrays.
* **Control Unit:** Individual **ESP32 units** act as node-controllers listening natively to specific Firebase paths.
* **Workflow Loop:** If a zone's moisture drops below the ML-defined optimal threshold, the backend flags that zone in Firebase. The respective node ESP32 instantly intercepts this flag, triggers a relay to open the physical water valve, and closes it autonomously once the moisture level reaches its optimal upper limit.

## 🛠️ Tech Stack & Hardware Components

### Software Ecosystem
* **Frontend:** HTML5, CSS3, JavaScript (Dashboard Layout)
* **Backend:** Python (Flask/FastAPI) / Node.js
* **Machine Learning:** Scikit-Learn / Pandas (Dynamic Crop Thresholding)
* **Cloud Database:** Firebase Realtime Database (RTDB)
* **Firmware Environment:** Arduino IDE (C++)

### Hardware Components
* **Microcontrollers:** ESP32 Development Boards (NodeMCU compatible)
* **Sensors:** Industrial 7-in-1 Soil NPK Meter (RS485 Modbus)
* **Actuators:** High-torque DC motors / Steppers (for Rack & Pinion), Solenoid Water Valves (12V/24V)
* **Relays:** Optocoupler Isolated 5V/12V Relay Modules
* **Communication Interface:** MAX485 TTL to RS485 converter (for reading the NPK sensor)
* **Chassis:** 4WD Robotic Platform with high-ground-clearance off-road wheels

## 👥 Contributors & Acknowledgements
* **Aditya Pratap Singh**
* **Piyush Sharma**
* **Aryan Kumar**
* **Indrani Rabha**

![Team Photo](https://res.cloudinary.com/dfll8qs0d/image/upload/v1783240441/irrigo_team_photo_vzfyn7.jpg)

We are the Team IRRIGO, passionate about leveraging technology for sustainable agriculture. Our collective expertise in IoT, software development, and hardware engineering enabled us to bring this project to life during Hacksagon 2026.

Special thanks to the Hacksagon 2026 organizers and judges for their insightful feedback and recognition.

