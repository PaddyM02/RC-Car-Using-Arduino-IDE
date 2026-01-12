# RC-Car-Using-Arduino-IDE
A remote controlled Rc car Coded from Arduino IDE


- ESP32 Wi-Fi Controlled Car (Arduino IDE) -

This project is an ESP32-based Wi-Fi controlled car built using the Arduino IDE.
The ESP32 hosts a web dashboard that allows you to control motor movement, dashboard LEDs, a buzzer, and monitor temperature in real time using a thermistor.
All controls are accessed through a browser on a phone, tablet, or computer connected to the same Wi-Fi network.

- Features -
- Wi-Fi Web Control Interface
- Motor control: Forward, Reverse, Left, Right, Stop
- Dashboard LEDs
- Headlights
- Left indicator
- Right indicator
- Buzzer (horn)
- Live temperature monitoring using a thermistor
- Mobile-friendly web dashboard
- Runs entirely on an ESP32 (no external server required)
- Hardware Requirements

- ESP32 development board -
Dual DC motors + motor driver (e.g. L298N / L293D)
LEDs (headlights, left indicator, right indicator)
Buzzer
NTC thermistor (10kΩ recommended)
Resistors (for voltage divider)
Jumper wires
Power supply / battery pack

- Pin Configuration -
Motors
Component	ESP32 Pin
Motor 1 Pin A	GPIO 27
Motor 1 Pin B	GPIO 26
Motor 2 Pin A	GPIO 33
Motor 2 Pin B	GPIO 25
LEDs
LED	ESP32 Pin
Headlights	GPIO 14
Left Indicator	GPIO 12
Right Indicator	GPIO 13
Other
Component	ESP32 Pin
Buzzer	GPIO 15
Thermistor (ADC)	GPIO 34
- Wi-Fi Setup

Update the Wi-Fi credentials in the code:

const char* ssid     = "YOUR_WIFI_NAME"; I used my personal hotspot details for these.
const char* password = "YOUR_WIFI_PASSWORD";


- The ESP32 can connect to -
A home Wi-Fi network
A mobile phone hotspot
- Web Interface

-Once connected to Wi-Fi-
Open the Serial Monitor
Copy the ESP32’s IP address
Paste it into a browser (e.g. http://192.168.1.100)
Web Dashboard Features:
Directional control buttons
LED toggle buttons
Live temperature display (updates every second)

- Status feedback -
- Temperature Measurement
- Uses a 10kΩ NTC thermistor
Connected via a voltage divider
Temperature calculated using the Steinhart–Hart equation
Displayed in degrees Celsius (°C) on the web page

- How It Works -
The ESP32 runs a WebServer on port 80
Each button sends an HTTP request (e.g. /forward, /stop)
The ESP32 processes requests and controls hardware accordingly
Temperature is read via ADC and sent to the browser every second using JavaScript fetch()

- Software Requirements -
Arduino IDE
ESP32 Board Package installed

- Required Libraries -
WiFi.h
WebServer.h
Arduino.h

- How to Upload -
Open the project in Arduino IDE
Select:
Board: ESP32 Dev Module
Port: Correct COM port
Click Upload
Open the Serial Monitor at 115200 baud
Connect to the displayed IP address

- Future Improvements -
PWM speed control
Camera module support
Indicator blinking
Battery level monitoring
Password-protected web interface
Mobile app control

- Author -
Created as an ESP32 Arduino IDE project for learning:
Embedded systems
Wi-Fi networking
Web-based hardware control
Sensor integration
