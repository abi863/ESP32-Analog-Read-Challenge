# ESP32 Analog Read – Potentiometer

## Objective

Read the analog value from a potentiometer using ESP32 and display the reading on the Serial Monitor every 500 ms.

## Components Used

- ESP32 DevKit
- Potentiometer

## Pin Connections

| Potentiometer | ESP32 |
|---|---|
| VCC | 3.3V |
| GND | GND |
| SIG | GPIO 34 |

## Working

The ESP32 reads the analog voltage from the potentiometer using its ADC input on GPIO 34.

The analog value is displayed on the Serial Monitor every 500 ms.

The potentiometer value changes when the knob is rotated.

## Code

```cpp
const int potPin = 34;

void setup() {
  Serial.begin(115200);
}

void loop() {
  int value = analogRead(potPin);

  Serial.println(value);

  delay(500);
}
