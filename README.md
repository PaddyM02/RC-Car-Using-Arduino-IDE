# RC-Car Using Arduino IDE

A remote-controlled car built using an ESP32 and coded in the Arduino IDE.  
The ESP32 hosts a Wi-Fi web dashboard to control motors, LEDs, a buzzer, and monitor temperature in real time.

---

## Features

- Wi-Fi web control interface  
- Motor control: Forward, Reverse, Left, Right, Stop  
- Dashboard LEDs:  
  - Headlights  
  - Left indicator  
  - Right indicator  
- Buzzer (horn)  
- Live temperature monitoring using a thermistor  
- Mobile-friendly web dashboard  
- Fully runs on ESP32 (no external server required)  

---

## Hardware Requirements

- ESP32 development board  
- Dual DC motors + motor driver (e.g., L298N / L293D)  
- LEDs (headlights, left indicator, right indicator)  
- Buzzer  
- 10kΩ NTC thermistor  
- Resistors (for voltage divider)  
- Jumper wires  
- Power supply / battery pack  

---

## Pin Configuration

### Motors
| Component    | ESP32 Pin |
|-------------|-----------|
| Motor 1 Pin A | GPIO 27 |
| Motor 1 Pin B | GPIO 26 |
| Motor 2 Pin A | GPIO 33 |
| Motor 2 Pin B | GPIO 25 |

### LEDs
| LED             | ESP32 Pin |
|-----------------|-----------|
| Headlights      | GPIO 14   |
| Left Indicator  | GPIO 12   |
| Right Indicator | GPIO 13   |

### Other
| Component       | ESP32 Pin |
|-----------------|-----------|
| Buzzer          | GPIO 15   |
| Thermistor (ADC)| GPIO 34   |

---

## Wi-Fi Setup

Update the Wi-Fi credentials in your code:

```cpp
const char* ssid     = "Paddys Iphone";     
const char* password = "12345678"; 
