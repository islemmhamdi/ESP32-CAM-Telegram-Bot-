# ESP32-CAM-Telegram-Bot
# ESP32-CAM Telegram Bot with BME280 Sensor

This project implements a **smart ESP32-CAM system** that can:  

- Capture photos with the ESP32-CAM  
- Send images to Telegram when motion is detected  
- Toggle flash LED via Telegram commands  
- Read temperature and humidity using the BME280 sensor  
- Respond to commands via Telegram bot  

---

## 📦 Features

- Motion detection via PIR sensor  
- Flash LED control  
- Telegram bot integration (`/photo`, `/flash`, `/readings`, `/start`)  
- Real-time sensor readings from BME280 (temperature & humidity)  
- Wi-Fi connection to your local network  

---

## ⚙️ Hardware Required

- ESP32-CAM AI-Thinker module  
- PIR motion sensor (connected to GPIO 13)  
- BME280 temperature & humidity sensor (connected via I2C pins GPIO 14/SDA, GPIO 15/SCL)  
- Optional flash LED (GPIO 4)  

---

## 🔧 Wiring

**ESP32-CAM AI-Thinker GPIOs**

| Function | Pin |
|----------|-----|
| D0       | 5   |
| D1       | 18  |
| D2       | 19  |
| D3       | 21  |
| D4       | 36  |
| D5       | 39  |
| D6       | 34  |
| D7       | 35  |
| XCLK     | 0   |
| PCLK     | 22  |
| VSYNC    | 25  |
| HREF     | 23  |
| SCCB SDA | 26  |
| SCCB SCL | 27  |
| PWDN     | 32  |
| RESET    | -1  |

**Other devices**

- PIR Sensor: GPIO 13  
- BME280: SDA = 14, SCL = 15  
- Flash LED: GPIO 4  

---

## 💻 Software Setup

1. Install **Arduino IDE** or use **PlatformIO** in VSCode.  
2. Install required libraries:  
   - `WiFi.h`  
   - `WiFiClientSecure.h`  
   - `esp_camera.h`  
   - `UniversalTelegramBot`  
   - `ArduinoJson`  
   - `Wire`  
   - `SparkFunBME280`  
3. Replace the following placeholders in `main.cpp` with your credentials:  
   ```cpp
   const char* ssid = "YOUR_WIFI_SSID";
   const char* password = "YOUR_WIFI_PASSWORD";
   String chatId = "YOUR_TELEGRAM_CHAT_ID";
   String BOTtoken = "YOUR_TELEGRAM_BOT_TOKEN";


<img width="854" height="476" alt="image" src="https://github.com/user-attachments/assets/06676379-4483-4eb4-a6fa-99e1954141ad" />
