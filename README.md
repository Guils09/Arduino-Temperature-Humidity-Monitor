Arduino Temperature & Humidity Monitor with LEDs
Project Overview

This project uses an Arduino to monitor temperature and humidity using a DHT11 sensor and a 10kΩ NTC thermistor. The readings are displayed on a 16x2 LCD, and LED indicators provide visual feedback for environmental conditions. A blue LED lights up only when both green LEDs are on, using two 2N3904 transistors as a hardware AND gate.

Features

LCD Display (16x2):

Line 1: DHT11 Temperature & Humidity

Line 2: NTC Temperature

LED Indicators:

Humidity:

≤ 20% → Green

20% → Red

Temperature (NTC):

20–30°C → Green (good)

< 20°C or > 30°C → Red

Blue LED:

Lights up only when both green LEDs are on (AND logic via 2N3904 transistors)

Components Needed
Component	Quantity
Arduino Uno (or compatible)	1
LCD 16x2 (HD44780)	1
DHT11 Sensor	1
10kΩ NTC Thermistor	1
LEDs (Green)	2
LEDs (Red)	2
LED (Blue)	1
2N3904 Transistors	2
Resistors 220Ω	5
Resistor 10kΩ	1
Resistor 2.2kΩ (LCD contrast)	1
Breadboard & Jumper Wires	—
Wiring Summary
LCD 16x2 (4-bit Mode)
LCD Pin	Function	Arduino Pin
1	VSS	GND
2	VDD	5V
3	V0	2.2kΩ → GND
4	RS	D8
5	RW	GND
6	E	D7
11	D4	D6
12	D5	D5
13	D6	D4
14	D7	D3
15	LED+	5V via 220Ω
16	LED−	GND
DHT11 Sensor
Pin	Function	Arduino Pin
1	VCC	5V
2	DATA	D2 + 10kΩ pull-up to 5V
3	NC	—
4	GND	GND
NTC Thermistor
5V --- NTC --- A0 --- 10kΩ --- GND

LEDs
LED	Color	Arduino Pin	Resistor
Humidity Green	Green	D10	220Ω
Humidity Red	Red	D11	220Ω
Temperature Green	Green	D12	220Ω
Temperature Red	Red	D13	220Ω
Blue LED (AND logic via 2N3904)
D10 (Green Humidity) → Base Q1 via 1kΩ
D12 (Green Temperature) → Base Q2 via 1kΩ

LED Blue + → 220Ω → 5V
LED Blue - → Collector Q2
Emitter Q2 → Collector Q1
Emitter Q1 → GND


LED Blue lights only when both green LEDs are ON

Code

The full Arduino sketch includes:

Reading DHT11 humidity and temperature

Reading NTC thermistor temperature

Displaying values on LCD

Controlling LEDs according to thresholds

Hardware AND for the blue LED

How to Use

Connect all components according to the wiring diagram.

Upload the provided Arduino sketch.

Power the Arduino via USB or 5V supply.

Observe the LCD for temperature/humidity readings and LED indicators:

Green LEDs indicate safe/normal conditions

Red LEDs indicate out-of-range conditions

Blue LED lights up only when both green LEDs are active

Notes

Ensure V0 (LCD contrast) has the correct resistor (2.2kΩ) for readability.

Use resistors for all LEDs to limit current.

Check NTC resistor value matches the thermistor specification (10kΩ recommended).

The blue LED logic is handled externally with 2N3904 transistors, no Arduino pin needed.

I can also make a diagram image for the full project showing all connections and LEDs with transistors, which is very useful for assembly.

Do you want me to make that diagram?

now for guit hub and less ai

Got it! Here's a clean, GitHub-friendly README version—shorter, professional, and written as a human would for a project page.

Arduino Temperature & Humidity Monitor with LEDs
Overview

Arduino project that reads temperature and humidity using a DHT11 and a 10kΩ NTC thermistor.

Values are displayed on a 16x2 LCD.

LED indicators show environmental status: green for safe ranges, red for out-of-range.

A blue LED lights up only when both green LEDs are on, using two 2N3904 transistors as an AND gate.

Features

LCD Display:

Line 1: DHT11 temperature & humidity

Line 2: NTC temperature

LEDs:

Humidity: ≤20% → Green, >20% → Red

Temperature (NTC): 20–30°C → Green, <20°C or >30°C → Red

Blue LED: Lights up only when both green LEDs are on (AND logic via 2N3904)

Components

Arduino Uno

LCD 16x2 (HD44780)

DHT11 Sensor

10kΩ NTC Thermistor

2 Green LEDs, 2 Red LEDs

1 Blue LED

2 × 2N3904 Transistors

Resistors: 220Ω, 10kΩ, 2.2kΩ

Breadboard & Jumper Wires

Wiring Summary

LCD 16x2 (4-bit, pinos 3–8)

RS → D8
E  → D7
D4 → D6
D5 → D5
D6 → D4
D7 → D3
VSS → GND
VDD → 5V
V0 → 2.2kΩ → GND
RW → GND
LED+ → 5V via 220Ω
LED− → GND


DHT11

VCC → 5V
DATA → D2 + 10kΩ pull-up
GND → GND


NTC Thermistor

5V → NTC → A0 → 10kΩ → GND


LEDs

LED	Arduino Pin	Color	Resistor
Humidity Green	D10	Green	220Ω
Humidity Red	D11	Red	220Ω
Temperature Green	D12	Green	220Ω
Temperature Red	D13	Red	220Ω

Blue LED (AND logic via 2N3904)

D10 → Base Q1 via 1kΩ
D12 → Base Q2 via 1kΩ
LED+ → 5V via 220Ω
LED− → Collector Q2
Emitter Q2 → Collector Q1
Emitter Q1 → GND

Usage

Connect all components as above.

Upload the Arduino sketch.

Power the Arduino via USB or 5V supply.

Observe readings on the LCD.

Green LEDs indicate safe conditions; red LEDs indicate warnings.

Blue LED lights only when both green LEDs are on.# Arduino-Temperature-Humidity-Monitor
