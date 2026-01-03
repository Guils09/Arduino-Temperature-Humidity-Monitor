## Overview:
This project uses an Arduino to measure temperature and humidity with a DHT11 sensor and a 10kΩ NTC thermistor. Readings are displayed on a 16x2 LCD. Four LEDs indicate environmental conditions: green for safe, red for out-of-range. A blue LED lights up only when both green LEDs are on, using two 2N3904 transistors as a hardware AND gate.
---
LCD Line 1: DHT11 Temperature & Humidity
---
LCD Line 2: NTC Temperature
---
## LEDs:

Humidity ≤20% → Green, >20% → Red

Temperature 20–30°C → Green, <20°C or >30°C → Red

Blue LED → ON only if both green LEDs are on
---
## Components: 
- Arduino Uno
- DHT11, NTC 10kΩ
- LCD 16x2
- 4 LEDs (2 green, 2 red)
- 1 blue LED, 2 × 2N3904
- resistors
 only doing the gate in hardware because my teatcher told me to tinker with gates fisicly

![g2](https://github.com/user-attachments/assets/b65de2ce-cb0f-49df-9808-f0bc038ac460)
![g1](https://github.com/user-attachments/assets/c309e9c9-e15d-41f9-9fbc-bcd5c53765dd)

Made by guils :)(:
