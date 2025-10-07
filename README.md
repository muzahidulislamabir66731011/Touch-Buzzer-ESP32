# 👆 Touch-Buzzer-ESP32-Template

![](https://img.shields.io/badge/ESP32-DevKit-C00E4?style=flat-square&logo=espressif&logoColor=white)
![](https://img.shields.io/badge/Code-25_Lines-00ff00?style=flat-square)
![](https://img.shields.io/badge/License-MIT-97CA00?style=flat-square&logo=opensourceinitiative)


![](https://img.shields.io/badge/Arduino-IDE-blue?style=for-the-badge&logo=arduino)
![](https://img.shields.io/badge/ESP32-Compatible-ff0000?style=for-the-badge&logo=espressif)
![](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![](https://img.shields.io/badge/Code-20_Lines-00ff00?style=for-the-badge)

[![Live Serial Plot](https://img.shields.io/badge/Serial-Monitor-Live-ff6600?style=flat-square&logo=serial)](/)

&gt; Click badge for wiring gif & real-time demo video.

## ⚡ What you get
- Pin defines already done  
- Empty `setup()` & `loop()` – drop in your touch-logic  
- Hardware map below for copy-paste wiring  

## 🔌 30-Second Wiring
| TTP223 | ESP32 Pin | Wire colour hint |
|--------|-----------|------------------|
| Vcc    | 3V3       | red              |
| GND    | GND       | black            |
| OUT    | GPIO 23   | yellow           |
| Buzzer +| GPIO 22  | blue             |
| Buzzer –| GND      | black            |

## 🚀 Next steps (copy / paste)
```cpp
void setup() {
  pinMode(TOUCH_PIN, INPUT);
  pinMode(BUZZER_PIN, OUTPUT);
  Serial.begin(115200);
}

void loop() {
  bool touched = digitalRead(TOUCH_PIN);
  digitalWrite(BUZZER_PIN, touched ? HIGH : LOW);
  Serial.println(touched ? "Touched" : "Clear");
  delay(100);
}
