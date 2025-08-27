This repository contains three IoT projects using the *ESP32* microcontroller.  
Each project demonstrates reading sensor values or generating test data and uploading them to *ThingSpeak Cloud* (or showing them in Serial Monitor).  

---

## 📂 Projects Overview

### 1️⃣ ESP32 Temperature/Water Level Detector
- Uses an *analog temperature sensor (LM35/TMP36 or similar)* as a probe to detect water level.  
- When the sensor is dipped in water, the ESP32 reads a high ADC value (e.g., ~1032).  
- Can be used as a *basic water presence / level detection system*.  

*Key Features*  
- Reads ADC values (0–4095) from ESP32.  
- Threshold-based water detection logic.  
- Displays output in Serial Monitor.  

---

### 2️⃣ ESP32 Soil Moisture Sensor + ThingSpeak
- Uses a *Soil Moisture sensor* connected to ESP32.  
- Sends live soil moisture values to *ThingSpeak Cloud* for visualization.  
- LED blinks during WiFi search, then ESP32 uploads data.  

*Key Features*  
- Reads soil sensor values (0–4095 ADC range).  
- Optional inversion (dry → high value, wet → low).  
- Updates *Field 1* on ThingSpeak every 15 seconds.  
- Serial monitor shows sensor readings and update status.  

---

### 3️⃣ ESP32 ThingSpeak Counter Test
- A simple program to test *WiFi + ThingSpeak connectivity*.  
- Sends an *incrementing counter value (a = 0, 1, 2, ...)* to Field 1.  
- Useful for checking if your ESP32 setup works before adding sensors.  

*Key Features*  
- Blinking LED while searching for WiFi.  
- Sends data every 15 seconds to ThingSpeak.  
- Serial monitor shows DATA UPDATED.  

---

## 🛠️ Hardware Required
- ESP32 Dev Module  
- Soil Moisture Sensor (analog)  
- LM35 / TMP36 (Temperature sensor, used as a probe)  
- Breadboard + Jumper Wires  
- WiFi with Internet Access
