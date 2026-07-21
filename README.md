# 🔥 FireGuard IoT

A simple IoT-based fire detection system built using an **ESP32**, **Flame Sensor**, and **DHT11 Temperature Sensor**. The system continuously monitors the environment and activates an alarm whenever a fire or abnormal temperature is detected.

---

## 📖 Overview
**FireGuard** is a beginner-friendly IoT project that demonstrates how embedded systems can be used for fire safety.  
The ESP32 collects data from sensors, processes it in real time, and alerts users through a buzzer and LED when hazardous conditions are detected.

---

## ✨ Features
- 🔥 Flame detection  
- 🌡️ Temperature monitoring  
- 🚨 Buzzer alarm  
- 💡 LED warning indicator  
- ⚡ ESP32-based system  
- 📟 Real-time monitoring using Serial Monitor  
- 🛠️ Easy to expand with Wi-Fi, cloud storage, and mobile notifications  

---

## 🛠️ Components Required

| Component               | Quantity |
|--------------------------|----------|
| ESP32 Development Board | 1        |
| Flame Sensor            | 1        |
| DHT11 Temperature Sensor| 1        |
| Active Buzzer           | 1        |
| Red LED                 | 1        |
| 220Ω Resistor           | 1        |
| Breadboard              | 1        |
| Jumper Wires            | As Required |
| USB Cable               | 1        |

---

## 🔌 Circuit Connections

**Flame Sensor**
| Flame Sensor | ESP32 |
|--------------|-------|
| VCC          | 3.3V  |
| GND          | GND   |
| OUT          | GPIO 27 |

**DHT11**
| DHT11 | ESP32 |
|-------|-------|
| VCC   | 3.3V  |
| DATA  | GPIO 4|
| GND   | GND   |

**Buzzer**
| Buzzer | ESP32 |
|--------|-------|
| +      | GPIO 26 |
| -      | GND   |

**LED**
| LED    | ESP32 |
|--------|-------|
| Anode (+) | GPIO 25 (through 220Ω resistor) |
| Cathode (-)| GND |

---

## ⚙️ Working Principle
1. ESP32 initializes all sensors.  
2. Reads the flame sensor continuously.  
3. Reads the room temperature using the DHT11.  
4. Checks whether:  
   - A flame is detected, or  
   - Temperature exceeds the threshold.  
5. If either condition is true:  
   - Turns ON the buzzer.  
   - Turns ON the LED.  
   - Displays **"FIRE DETECTED!"** in the Serial Monitor.  
6. Otherwise:  
   - Keeps the buzzer OFF.  
   - Keeps the LED OFF.  
   - Displays **"SAFE"** in the Serial Monitor.  

---

📂 Project Structure
FireGuard-IoT/
│
├── README.md
├── LICENSE
├── code/
│   └── FireGuard.ino
├── hardware/
│   ├── circuit_connections.md
│   └── components_list.md
├── images/
│   ├── block_diagram.png
│   ├── circuit_diagram.png
│   ├── flowchart.png
│   └── prototype.jpg
├── docs/
│   └── project_report.pdf
└── videos/
└── demo.mp4


---

## 🚀 Getting Started

### Prerequisites
- Arduino IDE  
- ESP32 Board Package  
- DHT Sensor Library  

### Installation
```bash
git clone https://github.com/your-username/FireGuard-IoT.git

Open FireGuard.ino using Arduino IDE.

Select your ESP32 board and COM port.

Upload the code.

Open the Serial Monitor (115200 baud) to monitor the system.

EXPECTED OUTPUT
NORMAL CONDITION

Code
Temperature : 29°C
Flame       : Not Detected
Status      : SAFE

FIRE DETECTED

Code
Temperature : 62°C
Flame       : Detected
Status      : FIRE DETECTED!
Buzzer      : ON
LED         : ON

🔮 Future Enhancements
Wi-Fi Alerts
Firebase Integration
Mobile App
OLED Display
Relay-Controlled Sprinkler
Data Logging
Email & SMS Notifications

💻 Technologies Used
ESP32
Arduino IDE
Embedded C++
Git
GitHub
Markdown
