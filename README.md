# Object-detector-embedded

This is an embedded Arduino-based project that uses an ultrasonic sensor to detect objects and control a gate system. When an object is detected within a certain distance, the gate opens, a blue LED turns on, and a buzzer sounds. When no object is detected, the gate closes, a red LED is on, and the system remains idle.

## 🧠 Features

- Ultrasonic distance measurement using HC-SR04
- Servo motor-controlled gate mechanism
- Visual indicators:
  - 🔴 Red LED: No object detected (gate closed)
  - 🔵 Blue LED: Object detected (gate open)
- Piezo buzzer that sounds when gate is open
- Serial monitor output showing the distance when an object is detected

## 🔧 Components Used

- Arduino UNO (or compatible board)
- HC-SR04 Ultrasonic Sensor
- Servo Motor (SG90 or similar)
- Red LED
- Blue LED
- Piezo Buzzer
- Jumper wires
- Breadboard

## 🪛 Pin Connections

| Component       | Arduino Pin |
|----------------|-------------|
| Trig (Ultrasonic) | D2          |
| Echo (Ultrasonic) | D3          |
| Red LED         | D4          |
| Blue LED        | D5          |
| Servo Motor     | D6 (PWM)    |
| GND Pins        | D7, D8 (set to LOW) |
| Buzzer          | D12         |

## 🧾 How It Works

1. The ultrasonic sensor continuously measures the distance.
2. If an object is detected within 15 cm:
   - The servo rotates to open the gate.
   - The red LED turns off, and the blue LED turns on.
   - The buzzer starts beeping.
   - Distance is printed to the serial monitor.
3. After 5 seconds, the gate closes automatically:
   - The blue LED turns off, red LED turns back on.
   - The buzzer stops.
   - A message is printed in the serial monitor.

## 💻 How to Upload

1. Open `object_detector.ino` in the Arduino IDE.
2. Connect your Arduino board via USB.
3. Select the correct port and board under **Tools**.
4. Click **Upload**.

## 📷 Demo

*(Add images or GIFs here if available showing the setup and working device)*

## 📜 License

This project is open-source and free to use for educational and personal purposes.

---

