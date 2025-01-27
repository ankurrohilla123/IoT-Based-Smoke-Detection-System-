# Smoke Detection System with IoT Integration 🚨🌐  

This project implements a **Smart Smoke Detection System** using the ESP8266 microcontroller. It features real-time gas monitoring, visual and sound alerts, and IoT integration with the **Blynk platform** for remote monitoring and control.

---

## 📌 Features  
- **Real-time Monitoring**: Gas levels are monitored using an MQ Gas Sensor.  
- **OLED Display**: Displays gas levels and system status (Normal/High Alert).  
- **Sound Alerts**: A buzzer provides alerts when gas levels exceed the threshold.  
- **IoT Integration**: Monitor gas levels and control the system via the **Blynk app**.  
- **Manual Buzzer Control**: Control the buzzer manually through the Blynk app.  

---

## 🛠️ Components Required  
- **ESP8266** (NodeMCU or similar): For microcontroller and WiFi connectivity.  
- **MQ Gas Sensor**: Detects gas concentrations.  
- **Buzzer**: Provides audible alerts.  
- **OLED Display (SSD1306)**: Displays gas levels and system status.  
- **Jumper Wires**: For connecting components.  
- **Breadboard**: For prototyping the circuit.  

---

## 📦 Software Libraries Used  
Ensure the following libraries are installed in your Arduino IDE:  
- [Blynk](https://github.com/blynkkk/blynk-library): For IoT integration and app interface.  
- [Adafruit SSD1306](https://github.com/adafruit/Adafruit_SSD1306): For controlling the OLED display.  
- [Adafruit GFX](https://github.com/adafruit/Adafruit-GFX-Library): For graphics handling on the OLED.  
- [ESP8266WiFi](https://arduino-esp8266.readthedocs.io/en/latest/): For WiFi connectivity.  

---

## ⚙️ Project Setup  

### Hardware Connections  
1. **Gas Sensor (MQ Sensor)**  
   - Connect the **A0** pin of the gas sensor to the **A0** pin of the ESP8266.  

2. **Buzzer**  
   - Connect the positive terminal of the buzzer to the **D6** pin of the ESP8266.  

3. **OLED Display (SSD1306)**  
   - Connect the **SCL** and **SDA** pins of the OLED to the corresponding I2C pins on the ESP8266.  

---

### Software Setup  

1. **Install Required Libraries**  
   - Install the libraries mentioned above via the Arduino Library Manager or GitHub.  

2. **Blynk Setup**  
   - Create a new project in the **Blynk app**.  
   - Add a **Button Widget** on **Virtual Pin V1** for manual buzzer control.  
   - Copy the provided **Auth Token** from the app into your code.  

3. **WiFi Configuration**  
   - Add your WiFi credentials in the `ssid[]` and `pass[]` variables in the code.  

4. **Adjust the Threshold**  
   - Modify the `sensorThreshold` variable in the code to suit your sensor's sensitivity.  

---

## 🚀 How It Works  

1. **Initialization**  
   - The ESP8266 connects to your WiFi network.  
   - The OLED initializes to display gas levels and system status.  

2. **Gas Detection**  
   - The gas sensor continuously reads gas concentrations.  
   - If levels exceed the predefined threshold, the system:  
     - Displays **"High Alert"** on the OLED.  
     - Triggers the buzzer for 3 seconds.  

3. **IoT Integration with Blynk**  
   - View gas levels and system status in real-time.  
   - Use the **Virtual Pin V1 Button** to control the buzzer manually.  

---

## 🛠️ Troubleshooting  

| Issue                | Solution                                                                 |
|----------------------|-------------------------------------------------------------------------|
| OLED not displaying  | Ensure correct I2C connections and use the correct address (default: 0x3C). |
| Gas sensor issues    | Calibrate the sensor and adjust the threshold.                         |
| Blynk app not connecting | Verify the **Auth Token** and ensure WiFi credentials are correct.    |

---

## 🚀 Future Improvements  

1. **Push Notifications**: Integrate with services like **IFTTT** for mobile/email alerts.  
2. **Multiple Sensors**: Add smoke or temperature sensors for enhanced detection.  
3. **Web Dashboard**: Develop a remote monitoring interface for web browsers.  

---

## 📜 License  
This project is **open-source**. Feel free to modify and contribute! Let’s make IoT smarter and safer!  

---

## 💡 Contributing  
We welcome contributions! Please fork the repository and submit a pull request with your improvements.  

---  

### ⭐ Let’s build smarter and safer IoT systems together!  

